# AGENTS.md: Vigil v1

## Mission

Build Vigil v1: a macOS menu-bar app for Apple Silicon, macOS 14+, that senses presence, head pose, blinks and region-level gaze from the built-in camera, on-device, and renders reactive Metal scenes on the desktop plus a floating Observation HUD. Nothing is recorded or sent. Build only what this file lists. If a task request conflicts with this file, stop and ask.

## Where you run

- Locally in this repo on the founder's MacBook with Xcode installed, via Codex CLI or the Codex Mac app.
- Not Codex cloud. Its Linux containers cannot build or test AppKit, AVFoundation, Vision or Metal code.
- Your shell runs inside the macOS Seatbelt sandbox. Do not expect live camera access from it. Test perception through the replay harness only.

## Product: the seven v1 features

1. **Presence engine.** AVFoundation capture plus Vision: face rectangles with yaw, pitch and roll; face landmarks with pupils; eye openness for blinks. One Euro filtering. 30 Hz with a face in view, 5 Hz without.
2. **Living desktop.** One borderless, click-through Metal window per display at desktop window level, joining all Spaces. Scenes: Field (a dot matrix that bends toward attention), Iris (a ring that tracks head position and dilates as the user leans in), Tide (a wave lattice that ripples on blinks). 60 fps cap, 30 fps on battery.
3. **Observation HUD.** Non-activating floating panel: 160x120 camera inset, corner brackets, pupil crosshairs, monospace telemetry (yaw, pitch, region, confidence, fps, LOCAL ONLY). Hotkey toggle. Mask mode shows landmarks on black with no camera pixels.
4. **Optional 5-second calibration.** Five points at 1 second each; ridge regression from features to screen position; three validation points choose a 3x3 or 3x2 region grid; one profile per display; a re-sharpen chip when seating position drifts.
5. **Menu bar control and auto-pause.** Pause, scene picker, signal color. Auto-pause on screen lock, display sleep, full-screen front app, Low Power Mode, battery under 20%.
6. **Privacy by construction.** See the rules below.
7. **Licensing and updates.** Free tier (HUD plus Field) and a Pro unlock by license key through the merchant of record's license API, usable offline after first activation. Sparkle 2 with an EdDSA-signed appcast. Notarized DMG.

## Non-goals

- Gaze as pointer, click, dwell or any accessibility control.
- Health, fatigue or diagnostic output; focus or attention scores.
- Multi-face tracking, remote viewing, export of tracking data.
- Recording video, stills or the screen.
- Cloud, accounts, telemetry. Windows, Linux, iPad, web.
- Gaze mapping on external monitors (they get presence-driven scenes only).
- Hand tracking, OSC output, scene editor, Mac App Store build.

## Rules you never break

- Frames live in memory only. No AVAssetWriter, no image encoding, no frame files, no screen capture.
- Request only the Camera permission. No Screen Recording, no Accessibility, no Input Monitoring.
- Network only for license activation and the Sparkle appcast.
- Every pause path stops the AVCaptureSession, so the green camera light goes off.
- Info.plist carries NSCameraUsageDescription, and the hardened-runtime entitlements carry `com.apple.security.device.camera`. Without the entitlement, macOS denies the camera silently with no prompt.
- Disable Center Stage for this app: set `AVCaptureDevice.centerStageControlMode = .app`, then `AVCaptureDevice.isCenterStageEnabled = false`.
- Draw gaze as a soft lens whose radius equals the current error estimate in points. Never a crisp dot.
- UI words: presence, attention, look, noticed. Never subject, target, lock or surveillance.

## Visual rules

- Palette: background #0B0B0C, text #E8E4DA, one user-selectable signal color: #7CFF6B (phosphor) or #FF3B30 (infrared).
- Telemetry font: JetBrains Mono or IBM Plex Mono (both OFL), bundled in Resources. System font everywhere else.
- Every motion is driven by a signal (head, blink, region, distance). Only the idle state breathes on a timer.

## Approved copy

- **NSCameraUsageDescription:** "Vigil uses your camera to see your face and eyes so your desktop can respond to you. Video is processed in memory on this Mac. It is never recorded, saved or sent."
- **Pre-permission sheet:** "Your Mac is about to notice you. Vigil looks for one thing: you, at this Mac. It reads where your face is, how your head turns, when you blink, and roughly where you look. Each frame lives in memory for a moment and is gone. The green light is on only while Vigil is looking; pause it and the light goes off." Buttons: "Allow camera", "Not now".

## Stack (fixed)

Swift 6. SwiftUI for MenuBarExtra, settings and onboarding. AppKit for the desktop windows and the HUD panel. AVFoundation, Vision, Metal via MTKView. Sparkle 2. XcodeGen. Sparkle is the only dependency; ask before adding another. Never hand-edit the .xcodeproj; edit project.yml and run `xcodegen`.

## Repo layout

```
vigil/
  AGENTS.md
  project.yml            XcodeGen spec
  Makefile               gen, build, test, run, replay, bench, dmg
  Vigil/
    App/                 VigilApp (MenuBarExtra), AppState, Onboarding/
    Capture/             CameraSession, FrameSource (live | file replay)
    Perception/          FaceTracker (Vision), Features, OneEuro, Blink,
                         GazeMapper, Calibration, PresenceState
    Scenes/              DesktopWindows, SceneRenderer, Uniforms,
                         Shaders/Field.metal, Iris.metal, Tide.metal
    HUD/                 HUDPanel, HUDView (Mask mode)
    Power/               PauseController
    Licensing/           LicenseClient
    Resources/           Info.plist, Vigil.entitlements, fonts, assets
  VigilTests/            replay-driven perception tests
  Fixtures/              founder-only .mov clips + labels.json (git LFS)
  tools/replay/          CLI: vigil-replay clip.mov --json out.json
  scripts/               bench.sh, notarize.sh, make-dmg.sh, appcast.sh
```

## 30-day milestones

Each milestone ends with its check green. Stop and report if a check fails twice.

1. **Days 1 to 2, scaffold.** Menu-bar agent app (LSUIElement), hardened runtime, camera entitlement, usage string, `make build test run`. Check: launches, asks for the camera, shows raw fps in a debug window.
2. **Days 3 to 6, capture and Vision.** 640x480 at 30 fps, late frames dropped. FaceTracker emits PresenceState: face present, box, yaw, pitch, roll, both pupils, eye openness, confidence, timestamp. FrameSource has a file-replay implementation (AVAssetReader); vigil-replay dumps JSON. Check: replay is deterministic; per-stage latency is logged.
3. **Days 7 to 9, signals.** One Euro filter, blink detection with hysteresis, uncalibrated left, center, right gaze from head plus pupil features. Check on fixtures: presence in at least 98% of good-light frames; blink recall and precision at least 90%; yaw noise at rest under 1 degree SD.
4. **Days 10 to 13, Observation HUD.** Non-activating floating NSPanel with inset, brackets, crosshairs, telemetry, hotkey, Mask mode. Check: HUD at 30 fps; Mask shows landmarks only. **Day 10 is the founder's go/no-go gate; pause for the decision.**
5. **Days 14 to 19, scenes.** Desktop-level windows per display; one Uniforms struct: time, presence, yaw, pitch, distance, gaze x and y, gaze radius, blink impulse, low-light flag. Field, Iris and Tide as shaders. Handle display attach and detach. Check: 60 fps on the built-in display, 30 on battery, no input stolen.
6. **Days 20 to 22, calibration.** Five points, ridge regression, three validation points, per-display profile. Check: at least 80% 3x3 region hits on no-glasses, good-light fixtures.
7. **Days 23 to 25, power and privacy.** PauseController for screen lock, display sleep, full-screen front app, Low Power Mode, battery under 20%, manual pause. Check: green light off within 1 second of any pause; bench meets the targets below or tracking steps down to 15 Hz on its own.
8. **Days 26 to 28, onboarding, license, updates.** Pre-permission sheet with the approved copy; license activation; Sparkle 2. Check: a fresh macOS account reaches first reaction in under 30 seconds.
9. **Days 29 to 30, ship.** Developer ID signing, notarize with notarytool, staple, build the DMG, run the QA matrix: glasses on and off, bright and dim, Center Stage camera, Continuity Camera present, external display attached, clamshell with no camera (graceful message).

## Testing the webcam on macOS

```
# list cameras and device indexes
system_profiler SPCameraDataType
ffmpeg -f avfoundation -list_devices true -i ""

# clean-install permission test (use the real bundle id)
tccutil reset Camera com.example.vigil

# always launch the bundle, never the inner binary from a shell:
# TCC charges camera access to the responsible process, so a binary
# run from Terminal or Codex makes the terminal the app asking
open build/Build/Products/Debug/Vigil.app

# silent denial? confirm the entitlement and watch TCC
codesign -d --entitlements - build/Build/Products/Debug/Vigil.app
log stream --predicate 'subsystem == "com.apple.TCC"'

# founder records fixtures (consented, founder only)
ffmpeg -f avfoundation -framerate 30 -video_size 1280x720 -i "<index>" -t 20 Fixtures/look_left.mov

# energy bench while the app runs with a face in view
sudo powermetrics --samplers cpu_power,gpu_power,ane_power -i 1000 -n 60 > bench.txt
```

`make test` drives every perception test from Fixtures through FrameSource replay. No test touches the live camera; live checks are the founder's manual QA list.

## Definition of done

1. Fresh macOS user account: download, open, allow camera, first reaction in 30 seconds or less, no calibration.
2. `spctl -a -vvv -t install` accepts the DMG as notarized Developer ID; `xcrun stapler validate` passes.
3. Only the Camera permission exists in System Settings for Vigil. It runs with Wi-Fi off after activation.
4. No frame persistence: code search finds no AVAssetWriter or image-destination writes in the app target; a file-system audit after 30 minutes finds no new media files.
5. Fixture report written to Fixtures/report.json and meeting the checks in milestones 3 and 6.
6. Under 5% total CPU and no audible fan in 20 minutes on an M-series Pro chip, or the automatic step-down engages.
7. Two hours continuous with no crash and under 50 MB memory growth, across sleep and wake, lid close, display attach and detach, and Continuity Camera disappearing.
8. Green light off within 1 second of pause or lock.

## Do not build

- Backends, accounts, analytics, third-party crash SDKs.
- Electron, Tauri, web views, Python, MediaPipe, custom Core ML models, or downloaded gaze weights. Public gaze datasets such as ETH-XGaze and MPIIGaze forbid commercial use, including training.
- Gaze-driven cursor, clicks, or any Accessibility API use.
- Multi-face tracking, recording, export of tracking data.
- A scene editor, marketplace, cloud sync, or a cross-platform core.
- More than one settings window or more than 8 settings controls.
- Mac App Store sandbox work beyond keeping entitlements compatible.
