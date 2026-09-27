# Privacy requirements

**Design requirements, not verified application behavior.** No app exists in this repository and no privacy audit has run.

## Camera and tracking

Planned flow: camera → in-memory frames → Vision features → filtered presence state → scenes/HUD. No frame recording, image encoding, frame files, screen capture, tracking export or remote viewing. Mask mode must show landmarks on black without camera pixels. No multi-face tracking, diagnostic output or attention scoring.

Every pause stops AVCaptureSession rather than merely hiding output. Manual pause, lock, display sleep, full-screen front app, Low Power Mode and battery below 20% must extinguish the camera indicator within one second.

## Permissions

Request Camera only, with NSCameraUsageDescription and the hardened-runtime camera entitlement. No Screen Recording, Accessibility or Input Monitoring. The brief requires disabling Center Stage for this app. Validate full-screen detection and hotkeys without introducing forbidden permissions.

## Network and local state

License activation and Sparkle appcast requests are the brief's intended network exceptions. Update-payload downloads and exact host/redirect policy remain unresolved. No accounts, cloud processing, telemetry, analytics or third-party crash SDKs. Offline use after first activation is required.

Calibration parameters and license state may require local storage; schemas, location, retention and reset controls are undecided. Never persist raw frames or tracking history in these profiles. Do not call the entire product network-free.

## Development fixtures

The brief proposes founder-only consented replay clips, labels and JSON evaluation reports. They are distinct from the shipping app's ban on recording and tracking export. No fixtures have been acquired or generated. Storage, access, retention and Git LFS suitability must be resolved first. Private visibility and Git LFS alone do not settle consent or privacy.

The brief excludes public gaze datasets. Its categorical dataset-license statement is preserved as source material, not independently verified legal guidance. Any future data use needs documented rights.

## Approved copy from the brief

**Camera usage description**

> Vigil uses your camera to see your face and eyes so your desktop can respond to you. Video is processed in memory on this Mac. It is never recorded, saved or sent.

**Pre-permission sheet**

> Your Mac is about to notice you. Vigil looks for one thing: you, at this Mac. It reads where your face is, how your head turns, when you blink, and roughly where you look. Each frame lives in memory for a moment and is gone. The green light is on only while Vigil is looking; pause it and the light goes off.

Buttons: **Allow camera**, **Not now**. This supplied copy requires implementation verification before use as a product claim.

## Evidence required before release

Audit persistence paths, permissions, network destinations, offline behavior, capture shutdown, debug logs and development fixture handling. Perform the specified filesystem and pause tests on actual hardware. Record results before declaring privacy requirements met.
