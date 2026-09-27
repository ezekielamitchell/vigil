# Vigil v1 roadmap

**Proposed only. All milestones are unstarted and unverified.** Days are relative to a future implementation start, not calendar commitments. Documentation setup completes no product milestone.

| Days | Milestone | Acceptance target |
| --- | --- | --- |
| 1–2 | Menu-bar scaffold | LSUIElement app, hardened runtime, camera entitlement and usage string; build/test/run; camera prompt and raw-fps display. |
| 3–6 | Capture and Vision | 640×480 at 30 fps, late frames dropped; complete PresenceState; AVAssetReader replay and JSON reporting; deterministic replay and per-stage latency logs. |
| 7–9 | Filtered signals | One Euro filter, hysteresis blink detection and coarse gaze; at least 98% presence in good-light frames, blink precision and recall each at least 90%, resting yaw noise below 1° SD. |
| 10–13 | Observation HUD | Non-activating panel, inset, landmarks, telemetry, hotkey and Mask mode; HUD at 30 fps. Founder go/no-go on Day 10. |
| 14–19 | Scenes | Field, Iris and Tide; shared uniforms; per-display windows and attach/detach handling; 60 fps built-in, 30 fps battery cap; no input stolen. |
| 20–22 | Calibration | Five points, ridge regression, three validation points and supported-display profiles; at least 80% 3×3 region hits on no-glasses, good-light fixtures. |
| 23–25 | Power and privacy | All pause triggers stop capture and extinguish camera light within one second; performance targets met or tracking reduces to 15 Hz. |
| 26–28 | Onboarding, license, updates | Approved permission copy, activation and Sparkle 2; first reaction in under 30 seconds on a fresh account. |
| 29–30 | Release candidate | Developer ID signing, notarization, stapling, DMG and full QA matrix. |

## Execution decisions

Day 10 requires the founder's go/no-go decision; approval is not implied by repository creation. If a milestone check fails twice during future execution, stop progression and report the blocker and evidence. No start date or release date has been assigned.

## Release acceptance

- First reaction within 30 seconds on a fresh macOS account without calibration.
- Notarized Developer ID DMG accepted by spctl, with stapler validation passing.
- Camera is the only requested privacy permission; offline use works after activation.
- Source inspection finds no frame-persistence path in the app; a 30-minute filesystem audit finds no new media.
- Replay report meets signal and calibration targets.
- Under 5% total CPU and no audible fan over 20 minutes on an M-series Pro chip, or automatic step-down engages; measurement definitions remain open.
- Two hours without a crash and less than 50 MB memory growth across sleep/wake, lid close, display changes and Continuity Camera disappearance.
- Camera indicator off within one second of pause or lock.

Manual QA covers glasses on/off, bright/dim lighting, Center Stage camera, Continuity Camera present, external display and clamshell without a usable camera. Exact future commands and acceptance wording are in SPECIFICATION.md. No product tests or checks have run.
