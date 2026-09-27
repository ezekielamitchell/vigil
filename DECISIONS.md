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
