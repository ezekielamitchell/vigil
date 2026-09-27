# Scope and open decisions

## Repository setup

Personal repository: ezekielamitchell/vigil. Documentation only, with files at root and no application folders, code, build scripts, assets or fixtures. Private visibility was chosen because public publication was not requested. No source-code license or release is included.

## Product baseline

The complete supplied Vigil v1 brief is preserved verbatim in SPECIFICATION.md: seven features, non-goals, visual rules, approved copy, fixed stack, proposed future layout, milestones, manual QA commands and definition of done. It describes intended work and does not establish implementation or validated capabilities.

## Resolve before affected implementation

| Question | Required clarification |
| --- | --- |
| Per-display calibration | Reconcile “one profile per display” with the explicit exclusion of external-monitor gaze mapping. External scenes stay presence-driven. |
| Update network policy | Resolve appcast-only wording versus Sparkle update-payload downloads, redirects and allowed hosts. |
| License provider | Choose merchant, pricing, activation API, offline persistence, recovery and revocation behavior. |
| Full-screen detection and hotkey | Validate a supported approach without Accessibility or Input Monitoring. |
| Fixtures and reports | Define development-only replay data, consent, storage, access, retention and whether clips may enter Git LFS. Keep app recording/export prohibited. |
| Calibration evaluation | Define ground truth, error radius, region-hit calculation, 3×2 fallback and drift thresholds. |
| Power benchmark | Define CPU normalization, device/OS baseline, rendering load and step-down criteria. |
| Toolchain | Pin Xcode/Swift, XcodeGen and Sparkle revisions supporting macOS 14+ before building. |
| App identity and release | Choose real bundle ID, signing team, feed host, key storage and distribution terms. The example bundle ID in the brief is not final. |
| Fonts | Choose telemetry font and preserve its actual license notice before bundling. |
| Source license | Free/Pro product tiers do not select a source-code license; owner decision remains open. |
| Schedule | No implementation start date. Founder Day 10 go/no-go remains a separate decision. |

## Provenance

SPECIFICATION.md is the exact owner-supplied attachment titled “AGENTS.md: Vigil v1”. Commands in it were not executed and proposed folders were not created. Companion documents organize that brief and flag unresolved questions. No external technical or legal assertions were independently validated during setup.

## README visual follow-up

The owner authorized a README concept image after initialization. vigil-concept-v1.png and VISUAL.md are root-level documentation assets; implementation remains unstarted. The image is generated concept art, not an actual product screenshot or measured simulation.

## Visual direction revision — September 26, 2026

The owner rejected the initial green image, fonts and layout and requested an endr-aligned intelligence-interface concept with Thinking Machines-like typography and endr brackets. The README now uses v2: graphite/ivory, restrained amber, clean sans-serif, a single Field scene and a landmark HUD. The original specification and v1 image remain historical sources. This revises visual presentation only; it creates no implementation or expanded product scope. Reverse or refine the artwork on further owner direction.

## Personal project correction and visual refinement — September 26, 2026

The owner clarified that Vigil is a personal project, not an endr project. Earlier references to an endr-style direction were aesthetic references, not company attribution. Current artwork uses Vigil branding only; prior versions remain historical. The mistakenly routed v2 master, raw run and reference originals were moved with byte-for-byte verification to /Users/house/Pictures/Vigil, outside company storage. Company catalogs retain a routing-correction note only.

The owner requested a clearer camera-to-gaze-to-wave display: v3 adds a synthetic camera inset, a matching center-left screen-region map and soft gaze halo, local wave-intensity response, a signal-confidence bar, and scene/Pause/Mask/Calibrate controls. Values are illustrative; the change adds no application code, actual camera capture, gaze accuracy claim, attention score or cursor interaction. Further owner direction may refine the concept.

## Abstract presence and detailed field refinement — September 26, 2026

The owner rejected the photographic-looking synthetic face and requested an abstract human-like digital figure, more field/platform detail and a better gaze-region treatment. v4 uses a point-and-line head/shoulders representation in Mask mode, a richer 3D lattice and height contours, and a broad approximate gaze region integrated into the wave surface. Proposed Response/Smoothing controls refine the concept interface. Prior artwork and original source requirements remain preserved. This is an artistic visualization; native landmark fidelity and these controls are not implemented or validated.

## Browser simulation and README recording — September 26, 2026

The owner explicitly requested building the accepted concept after discussing a live/simulated README preview. A standalone local browser simulation is now implemented separately from this repository. It renders a procedural human presence model and wave field with synthetic or pointer input, scene selection, Pause, Mask, Response/Smoothing and a simulated calibration walkthrough. No camera is accessed. This authorizes selected GIF/MP4/PNG media and documentation here, not native app code, a public interactive deployment or a product release.

Browser interaction checks and deterministic scene rendering passed in Chromium; these checks do not complete native roadmap milestones or establish gaze accuracy. The original specification, prior images and prompts remain unchanged.

Repository readback during this update shows public visibility. Earlier statements that it was private are historical and do not describe its current access. This task does not change repository visibility. The interactive source remains local; only the requested preview media and documentation are added here.

## Slower motion, structured face mesh and useful telemetry

The owner requested a slower animation and a much better face, then refined that direction toward a more forward-facing, less celestial mesh. The current local simulation runs on a 36-second loop and uses generic anatomical geometry with connected triangles, subtle facets and restrained nodes. The single inset label is Face mesh. MediaPipe-derived topology retains Apache-2.0 attribution in THIRD_PARTY_NOTICES.md; no perception runtime or camera is used.

The owner also requested average blinks per minute and a useful grid beside the current region. Blink average is a trailing 60-second count of synthetic events, with a seeded demo timeline. The second grid shows relative dwell over the prior 12 seconds; Pointer mode accumulates its actual simulated path. Pause freezes time and these readouts. These are visual simulation features and do not complete native product milestones.

The field now uses smoother geometry, rounded particles and gentler brightness transitions. The README publishes the v3 WebP, MP4 and PNG; older public media and the original specification remain unchanged. The intermediate v2 preview stays local.
