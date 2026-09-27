# Vigil rendered simulation — v4

Final refinement of the accepted v3 platform.

- Preview: [animated WebP](vigil-demo-v4.webp), [MP4](vigil-demo-v4.mp4), [still PNG](vigil-demo-v4.png).
- Identity: the exact owner-selected [Four Horses black-v3 PNG](four-horses-icon-black-v3.png) replaces the V glyph beside Vigil and supplies the browser icon. The toolbar presents its alpha silhouette in ivory; the favicon wraps the unchanged raster in a light tile. This is the official personal-project mark.
- Face: complete lip corners, smoother contour joins without duplicate strokes, attached ear roots, hidden rear geometry, fully closing simulated eyelids, and a clean Face mesh label. The approved pose and graphite/ivory treatment remain.
- Motion and telemetry: the same calm 36-second loop, 12-second gaze-history grid and trailing-60-second synthetic blink count. Pointer-to-Auto handoff eases over 350 ms. A quiet backing keeps the moving gaze label legible.
- Capture: MP4 1600×1000 at 30 fps; animated WebP 960×600 at 24 fps, both 36 seconds. Still preview 1585×992.
- Validation: 19 focused checks pass, including smooth mode handoff, all-scene loop equality, complete blink closure, Mask, Pause/Resume, reduced motion, desktop/narrow layout and exact icon preservation. No runtime errors or external requests were observed in Chromium.
- Scope: synthetic local browser simulation. Source remains separate; selected preview media and the personal icon are published here.

---

# Vigil rendered simulation — v3

The v3 preview incorporates the owner's requests for slower movement, a forward-facing structured face mesh, clearer telemetry and a smoother field.

- Preview: [animated WebP](vigil-demo-v3.webp), [MP4](vigil-demo-v3.mp4), [still PNG](vigil-demo-v3.png).
- Motion: a 36-second cycle, one-third the initial automatic gaze and field speed. Pointer input remains responsive.
- Face: generic anatomical topology with a mostly forward-facing pose, subtle graphite facets, coherent fine triangles, smaller landmark nodes and restrained surface detail. Removed the scattered sparkle and independent sway. One Face mesh label replaces Presence model and Landmark mask.
- Readouts: the current coarse region sits beside a heatmap of the previous 12 seconds of simulated gaze dwell. The blink average counts synthetic events over the trailing 60 seconds and displays blinks/minute. Demo history is seeded; Pointer mode records its live simulated path. Pause freezes both histories and statistics.
- Field: smoother broad waves, rounded subpixel particles, finer brightness transitions, quieter filaments and softer focus falloff. Field, Iris and Tide remain distinct.
- Attribution: the generic face topology derives from [MediaPipe](https://github.com/google-ai-edge/mediapipe), pinned to revision a908d668c730da128dfa8d9f6bd25d519d006692. The transformations and full Apache-2.0 license are in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). No inference runtime is included.
- Capture: a 36-second exact-time recording. MP4 is 1600×1000 at 30 fps; WebP is 960×600 at 15 fps. Static preview: 1585×992.
- Validation: all scenes repeat identically at 0/36 seconds, including canvases, histories and statistics. Blink-rate boundaries were checked independently; Pointer dwell fills the expected heatmap region; Pause, Mask, calibration, reduced motion and 390px/1280px layouts passed. No app errors or external runtime requests were observed.
- Scope: personal browser simulation, synthetic signals only. No camera, captured person, real gaze tracking, native macOS implementation or public interactive deployment. Source remains separate.

The supplied face references, local intermediate previews and source snapshots stay in the personal asset archive. Public v1 media and the original concept history are preserved below.

---

# Vigil rendered simulation — v1

The first rendered README preview was recorded from a working local browser simulation of the accepted v4 concept.

- Preview: [looping GIF](vigil-demo-v1.gif), [MP4](vigil-demo-v1.mp4), [still PNG](vigil-demo-v1.png).
- Capture: 12 seconds, 360 exact-time frames at 30 fps, 1600×1000; the GIF is 800×500 at 12.5 fps with a reduced palette for README display. Static fallback: 1585×992.
- Rendering: local Canvas geometry for the wave field and abstract human figure, with HTML controls and system fonts. No generated image is pasted into the running interface.
- Input: a periodic synthetic gaze path in the recording. The local live version also supports pointer, touch and arrow-key input.
- Controls: distinct Field / Iris / Tide scenes, Pause, Mask, Response, Smoothing and a simulated five-point calibration walkthrough.
- Validation: interactions checked in Chromium at desktop and narrow sizes; reduced-motion starts paused; no app console errors or external requests observed. Field and presence canvases match byte-for-byte at t=0/t=12 and after out-of-order rendering in all three scenes. Whole-page capture has negligible corner antialias variation.
- Fidelity: charcoal/ivory palette, neutral type, framed stage, inset HUD, wave contours and region map follow v4. Auto/Pointer controls and synthetic-input labels clarify how the demo works. Procedural geometry is an interpretation of the generated concept rather than its exact image texture.
- Scope: personal visual simulation only. No camera access, real face, gaze estimator, attention score, native macOS app or public interactive deployment. Browser source is maintained separately from this documentation/media repository.

---

## Accepted static reference and preserved generation history

# Vigil concept preview — v4

Vigil is Ezekiel A. Mitchell’s personal project. This refinement preserves the graphite/ivory platform and replaces the photographic-looking figure with an abstract human presence model.

- Current asset: [vigil-concept-v4.png](vigil-concept-v4.png).
- Method: built-in image generation edit of v3; no CLI fallback.
- Figure: a non-photographic human head and shoulders formed from points and fine contour lines, with Mask visibly active. It is an artistic perception proxy, not a real camera image or demonstrated 3D reconstruction.
- Field: a more detailed point lattice, flowing curves, subtle height contours and a perspective base grid.
- Gaze estimate: a broad contour region integrated into the raised wave surface, labeled Center-left / Approximate, with a matching HUD screen-region map.
- Controls: Field / Iris / Tide, Pause, Mask, Calibrate and proposed Response/Smoothing controls. Signal confidence refers to sensing quality; it is not an attention or health score.
- Status: static concept artwork with illustrative indicators. No camera was accessed and no app, tracking, reconstruction or controls were implemented. The exact native landmark rendering remains a future implementation choice within the original scope.
- Previous images and prompts remain below as version history. v3's photographic-looking synthetic person is superseded by v4; v2's company branding is historical and does not describe project ownership.

## v4 generation prompt

```text
Use case: ui-mockup edit.
Edit the supplied Vigil personal-project image into a much more refined v4. Keep the existing product framing, near-black graphite, warm ivory, desaturated amber, clean GT America-like neutral sans typography, existing high-level layout and personal Vigil branding. A professional, extremely precise perception-interface concept. High-resolution landscape with sharp readable type and fine geometry. The user says the design is close, so refine it, do not create a different brand. No endr, no green.

THREE ESSENTIAL CHANGES:
1. Replace the photographic person with an unmistakably abstract, sentient-looking digital human presence form.
2. Increase the dimensional detail and craft of the 3D wave-field platform.
3. Redesign the ugly hard oval look-region overlay into an elegant spatial uncertainty visualization integrated into the field.

DIGITAL HUMAN FIGURE:
Inside the right Observation HUD, completely REMOVE the photographic face, skin, hair, shirt, chair and webcam background. Replace with a beautiful translucent human-like face and upper neck/shoulders made solely from thousands of very fine warm-white points, layered contour filaments and a sparse delicate wire mesh. It should look awake and human in form, intelligent and calm, like a luminous mathematical human presence; not a real person or a photograph, not a metal robot, mannequin, alien, skull, horror face or armored sci-fi character. Semi-transparent volumetric depth, dark interior, delicate facial structure. A softly defined brow, eyes, nose and lips; eyes are composed of subtle linework, no glowing eyeballs. A faint human shoulder contour dissolves into the black. Turn the head very slightly inward toward the main field. Use a few subtle amber pupil/landmark accents at most. A sophisticated artistic perception proxy, NOT an assertion of conscious AI.
Replace "CAMERA" within that inset with "PRESENCE MODEL". Add tiny quiet sublabel "Landmark mask" below the inset. Highlight the existing "Mask" button to indicate it is active; preserve Calibrate. Everything should make clear that camera input is being abstracted, not that a real face is shown.

WAVE FIELD:
Preserve the large left Field viewport but make it a truly detailed 3D mathematical surface. More orderly submillimeter-looking rows of points, flowing thin silver filaments, graceful intersecting longitudinal/transverse curves and a few very fine height contour traces. Coherent geometry; lines follow the same continuous surface and never become spaghetti. Use restrained perspective, layered relief, alternating valleys and ridges, precise depth falloff. A low-height graphite coordinate base plane with faint tick marks and subdued axes near the lower edge gives dimensional reference without introducing a battle map, numbers, noise or a platform pedestal.
The wave surface rises locally where the user looks, around CENTER-LEFT, while quieter rings and waves fan outward. Preserve ample dark negative space. Detail must stay crisp, not grainy. Brightness increases around the region in a disciplined ivory gradient; no fog, overexposed white blob, bloom or spotlight. Show the mechanism of a reactive field through precise structure.

LOOK REGION — COMPLETE REDESIGN:
Remove the old hard yellow ellipse, single boundary dot, and awkward long diagonal leader entirely.
Instead integrate a broad irregular soft lens of warm ivory/light desaturated amber into the wave surface near center-left. A few fine nested contour fragments follow and bend with the surface, breaking and fading naturally at the edges. It should feel like an estimated area with graded certainty: a softly brightened core, two wider quieter falloff bands, outer boundary dissolving into the mesh. No solid yellow ring or crisp edge. No bullseye, crosshair, cursor, exact point, targeting reticle or concentric perfect circles.
Place one refined compact annotation above the surface with short clean orthogonal leader ending against the AREA without a big dot. Text only: "Gaze estimate" and below in slightly smaller type "Center-left · Approximate".
Inside the HUD, improve the screen-region mini-map: precise 3×3 rectangular screen outline, all nine cells cleanly aligned, faint subdued dividers, middle-left cell softly ivory/amber-filled rather than hard orange. No isolated point. To its right: "Look region" then "Center-left"; small line underneath "Approximate". Ensure the main lens and mini-map agree.

OVERALL PLATFORM POLISH:
Top outside header remains "Vigil", subtitle "A desktop that responds to you." Upper right update to "INTERFACE STUDY / 04". Slightly tighter geometry, crisp hairlines and margins. Within viewport toolbar maintain Vigil on left, Field / Iris / Tide / Pause on right; Field selected.
Right HUD heading "OBSERVATION". Maintain the rows Presence / Detected, Blink / Noticed and Signal confidence / Stable with restrained 5-segment bar (four softly lit; no neon). Add a small restrained pair of controls under that meter: "Response" and "Smoothing", each a fine horizontal slider on its own compact row. These are visualization controls, no numeric score. Then the compact Mask (active) and Calibrate buttons, then LOCAL ONLY. Balance the portrait/model area and rows so everything fits naturally, no cramped typography, no excessive blank space.
Keep the low-to-high "Field intensity" legend in the lower-left of the main viewport; make it a tasteful thin continuous grayscale-to-ivory scale with a tiny amber end tick, no heavy bar glow.
Bottom strip: "Camera input" → "Gaze estimate" → "Field response" → "On-device". Remove the redundant FIELD / IRIS / TIDE words at lower right; use a small tasteful "MASK VIEW" indicator there.
Very bottom caption: "Illustrative concept · Abstract presence model".
Use content as exact text; no invented numerical coordinates, dates, fps, accuracy percentages or charts.
Final image should feel visibly more intricate, high-fidelity and intelligently designed, while remaining coherent and quiet.

Strict negatives: no photographic person of any kind, no realistic skin or hair, no company/endr logo, no military weapons or seals, no real camera capture, no green, no cyberpunk neon, no camera recording buttons, no blue hologram, no threat or attention scores, no precise eye cursor. Preserve project scope and controlled elegance.
```

---

## Historical v3 record — superseded figure and gaze visualization

# Vigil concept preview — v3

Vigil is Ezekiel A. Mitchell’s **personal project**. The previous revision incorrectly turned a style reference into endr branding and company asset routing. That attribution is superseded: the current image has Vigil branding only, and its artwork, generation history and private references are stored in the personal Vigil image library.

- Current asset: [vigil-concept-v3.png](vigil-concept-v3.png).
- Method: built-in image generation, editing v2 while preserving its charcoal/ivory palette and clean sans-serif typography.
- Interaction: synthetic camera preview with facial landmarks → coarse center-left screen region → a matching soft gaze halo → a raised, brighter 3D wave field.
- Indicators: presence, blink, an illustrative signal-confidence bar and a field-intensity legend. Confidence describes the sensing signal; it is not an attention, health or productivity score, a target lock, or a click trigger.
- Controls: Field / Iris / Tide, Pause, Mask and Calibrate.
- Scope: static concept artwork. The person is generated, not an actual camera recording; values and region detection are illustrative. No application or camera access was implemented.
- v1 and v2 remain historical artwork, with their original prompts below. v2's former company branding is not current project attribution.

## Current generation prompt

```text
Use case: ui-mockup edit.
Edit the supplied Vigil concept image. The user likes this design very much and wants a careful functional refinement, not another redesign. Preserve the near-black graphite / warm ivory / restrained amber palette, clean neutral sans typography, meticulous thin rules, single dominant field viewport, understated scientific instrumentation aesthetic and overall proportions. Retain the beautiful 3D point-lattice wave field. No green.

CRITICAL OWNERSHIP CHANGE: this is Vigil, a PERSONAL project. Remove the entire "endr" brand and its adjacent divider from the top-left header. The only product name is "Vigil", a little larger at the original top-left margin. Beneath: "A desktop that responds to you." Keep upper-right "INTERFACE STUDY / 03". Never include endr anywhere. Simple neutral corner marks elsewhere are okay but no company attribution.

Make the image clearly demonstrate THIS causal sequence: one person seen by a camera → approximate location where their eyes are looking on the screen → the 3D wave field rises and brightens in that screen region. This must be instantly understandable, not decorative wallpaper.

MAIN FIELD / GAZE RESPONSE:
Keep the main dark wide viewport. Preserve the ivory mathematical point field, but shape it into a low, readable 3D wave surface with a pronounced raised soft hill of brighter cream points near the CENTER-LEFT of the viewport. The amplitude, dot brightness and density increase smoothly around that location then fall away. The rest of the field is lower and dimmer. It should look like a living wave field responding to the person's gaze, not a mountainous terrain or a spotlight.
Overlay one broad, softly feathered amber/ivory elliptical gaze region around the wave peak with an extremely delicate broken contour and subtle transparent interior. No crisp gaze point, crosshair, cursor or target reticle. A short fine leader points to a small label "Look region / Center-left". This is approximate and uncertain, not pixel accurate. A tiny nearby horizontal legend reads "Field intensity", with a short low-to-high ramp in graphite-to-ivory. This is a visualization setting/response, not attention or health scoring.

RIGHT-SIDE OBSERVATION HUD:
Keep the rectangular right HUD, increase its width very slightly if needed to fit readable content; it must stay compact, never take over the field. Keep "OBSERVATION" as heading.
Replace the wireframe-only face with an unmistakable 4:3 monochrome CAMERA preview showing one completely synthetic adult sitting at a computer, shoulders and face, plain dark background, casual dark shirt, relaxed attentive expression. The face is mostly forward, eyes subtly looking toward their screen. Natural photographic-looking camera inset, not a metal robot, not a real celebrity, no personal likeness. Overlay sparse, restrained warm-ivory facial landmark dots around the eyes/nose/face, tiny pupil marks and fine corner brackets. Clearly feels like a webcam preview with local computer vision. Small inset label "CAMERA". Do not leave the old "MASK" label on the active photo.
Immediately below the camera inset, include a tiny 3-by-3 screen-region minimap. Highlight its MIDDLE-LEFT cell with muted amber and a soft edge; all other cells are quiet charcoal outlines. Beside it two readable lines: "Look region" and "Center-left". This must agree with the main wave peak and label.
Below, compact aligned status rows:
"Presence"   "Detected"
"Blink"      "Noticed"
Then a restrained segmented horizontal status meter, four of five short segments softly lit, labeled "Signal confidence" with "Stable" at the right. NOT target lock, not a progress-to-click bar, not an attention score. No percentages or performance claims.
Then two small secondary buttons in a single row: "Mask" and "Calibrate". Mask is not selected because camera preview is active.
Bottom line "LOCAL ONLY" with a muted amber dot. No recording indicator, no record button.

TOP VIEWPORT TOOLBAR:
On the left show "Vigil". On the right, one quiet segmented scene selector "Field   Iris   Tide" with Field selected, then one thin separator and "Pause". No duplicate scene picker elsewhere. The current Field scene has soft 3D wave deformation; do not switch to a third-party app.

BOTTOM STRIP:
Replace the old generic four-item feature strip with a simple legible left-to-right explanatory strip, four short phrases linked by small thin arrows:
"Camera" → "Look region" → "Wave response" → "On-device"
Use clean regular sans, not giant headings.
At bottom left small but readable "Illustrative concept • Synthetic camera preview".
Preserve the quiet professional research-interface tone and large well-aligned margins.

Constraints: This is still a static product-concept image, not a completed app. No company logos, no endr, no CIA seals, no weapons, no classified markings, no code, no blue or neon green, no extra windows, no hand tracking, no outside surveillance, no cursor control, no precise crosshair. Avoid a cluttered fake military dashboard. All interface text must be crisp and spelled correctly. Keep the original aesthetic that the user liked; add only these specific understandable interaction cues and fitting controls.
```

---

## Historical v2 record — superseded project attribution and preview

# Vigil concept preview — v2

The owner requested a complete visual redesign of the initial phosphor-green preview: a restrained intelligence-systems aesthetic fitting endr, cleaner typography inspired by the supplied Thinking Machines references, a different layout, and signature corner brackets.

- Current asset: [vigil-concept-v2.png](vigil-concept-v2.png).
- Method: built-in image generation with the three owner-supplied images as style/typography references; no CLI fallback.
- Direction: graphite, warm ivory and small muted amber accents; clean neutral sans-serif; exact lowercase 「 endr 」 display branding; one dominant Field scene and one Observation HUD.
- Product scope: presence, head pose, blink and coarse look region. The dense facial landmark illustration is conceptual and does not establish actual perception fidelity.
- Status: illustrative concept, not a running application, measured simulation or verified screenshot. No implementation has been added.
- Typography reference: the [official Thinking Machines stylesheet](https://thinkingmachines.ai/css/fonts.css?v=446f09d40630) names GT America. The generated image approximates the requested visual character; no font files were copied, bundled or represented as licensed assets.
- Source references were used for visual direction only. Their logos, code and hand-tracking features are not reproduced. Reference originals remain privately preserved; they are not committed here.
- v1 remains available as [historical artwork](vigil-concept-v1.png). Its original prompt and description are retained below.

## Current generation prompt

```text
Use case: ui-mockup.
Asset: completely redesigned v2 README hero concept for Vigil, an on-device macOS presence app, in endr's refined intelligence-systems visual language.
Reference image 1 is a STYLE reference only: near-black, warm ivory, finely resolved technical marks and quiet intelligence-lab atmosphere. Do not copy its browser, code, hand tracking, text or layout. Reference images 2 and 3 are TYPOGRAPHY references only: clean GT America-like neutral neo-grotesk sans serif, regular and medium weights. No reference logos or website names in the result.

Make a new exceptionally polished wide landscape image, about 16:10, high resolution, readable in a GitHub README. Art direction: an intelligence research instrument designed by a world-class editorial software studio. Calm, rigorous, authoritative, utilitarian beauty. Rich near-black #0B0B0C, graphite #171819, warm ivory #DDD9CE, taupe gray #8B877C, tiny muted amber #B49866 signal accents. ABSOLUTELY NO GREEN. No phosphor, no neon, no bloom, no fluorescent glow. Grayscale/ivory occupies 98% of the composition. Avoid giant headlines and card-based marketing layouts.

Typography is crucial: use the clean natural sans-serif appearance in references 2 and 3, like GT America, Neue Haas Grotesk or Helvetica Neue. Natural widths, no rounded futuristic letters, no serif, no pixel font, no stretched all-caps sci-fi. Major text uses regular/medium weight, tiny telemetry alone can use restrained neutral mono. No wide letterspacing in sentences. Brand in upper left is EXACTLY "「 endr 」", lowercase, with a space inside each genuine Unicode corner bracket. Beside it, separated by a small rule, title "Vigil" in medium sans serif, modest size. Beneath that only "On-device perception. A responsive desktop." Top right understated "INTERFACE STUDY / 02". Generous margins. Fine hairline dividing header from the visual.

One dominant, believable native macOS desktop surface occupies the entire middle of the composition, around 85% width and 70% height. It is flat, front-facing and very subtly framed, nearly square corners, no perspective laptop, no browser, no macOS Dock full of app icons. Minimal authentic-looking top menu bar in graphite: a small app mark and "Vigil" left; very small "Field" and "Pause" controls on right. No decorative OS traffic lights on every panel.

The wallpaper is the Field scene, not a tactical map. Thousands of exquisitely fine warm-gray dots on near-black form an organic sculpted spatial lattice that bends toward a broad SOFT attention region on the left-center. This shape feels mathematical and responsive: gentle 3D relief contour made from individual cream points, low-amplitude woven folds and subtle depth, spacious black breathing room. Reference 1 inspires sober dot-density rather than a green glowing funnel. A diffuse desaturated ivory haze communicates coarse gaze uncertainty, never a crisp point, cursor or targeting crosshair. No connected route network, world map, topographic combat map or fake code.

ONE compact floating Observation HUD near the right side of the desktop. Narrow, rectangular, dark translucent black, single delicate taupe keyline and tiny corner ticks. It must look like a refined actual instrument over a living wallpaper, not a web card. Title "「 OBSERVATION 」". Its upper inset is large enough to clearly see a single abstract human FACE LANDMARK model on black: anatomical face contour, brows, eye outlines, sparse pupil landmarks, nose bridge and lips, slight three-quarter head turn. Fine ivory points and short delicate lines, believable computer-vision landmarks, not a cartoon alien, not a photographic portrait, not a faceted metal robot. The face visualization fits fully inside a tidy inset with a tiny "MASK" label. No crosshairs beyond tiny pupil marks. Under the face, only these crisp aligned rows:
"Presence" "Detected"
"Head pose" "Slight right"
"Look region" "Center"
"Blink" "Noticed"
Then a thin divider, tiny neutral status mark and "LOCAL ONLY".
No numeric performance claims, no time-series charts, no scores.
Keep the HUD around 20% of desktop width, with ample padding; desktop Field remains the visual focus.

Below the main desktop, one thin editorial annotation strip, not three cards. On the left text "「 01 」 Presence" then "「 02 」 Head pose" then "「 03 」 Blink" then "「 04 」 Look region", aligned and separated by generous spaces. On the right small "FIELD / IRIS / TIDE". At the very bottom one discreet caption "Illustrative concept". No extra text.

Overall precision, line weights, typography and hierarchy should feel suited to an endr research and perception system. The intelligence/CIA mood comes only from the quiet instrumentation and restraint. No CIA logo, seals, classification markings, weapons, soldiers, drones, satellite imagery, hand tracking, surveillance feeds, enemy targets, maps, surveillance copy, threatening aesthetic, or invented product features. No lens flare, saturated accent, large green regions, three-tile collage, giant curved display frame, repeated slogans, fake code, unnecessary marketing copy. All written text must be accurate and clearly readable. A full rebuild, not a minor recolor of an earlier mockup.
```

---

## Historical v1 record — superseded visual direction

# Vigil concept preview

The owner requested a visual preview for the README after repository initialization. This authorizes the image and its documentation; application implementation remains unstarted.

- Asset: [vigil-concept-v1.png](vigil-concept-v1.png)
- Method: built-in image generation tool; no CLI fallback.
- Purpose: visual direction for Field, the Observation HUD in Mask mode, menu-bar controls, and Field/Iris/Tide scene previews.
- Status: generated concept art, not a running application, measured simulation, camera capture or verified screenshot. Interface values are illustrative.
- Visual review: near-black/off-white/phosphor palette, readable labels, diffuse attention region and explicit concept label. Final native UI may differ.

## Generation prompt

```text
Use case: ui-mockup.
Asset type: premium GitHub README concept preview for Vigil, a planned native macOS menu-bar app.
Create one exceptionally polished wide 16:9 product visualization at high resolution. This is a flat, front-facing desktop interface concept, not a photograph of a laptop, not a website, not a dashboard. Restrained editorial software design, precise geometry, generous space, physically plausible macOS window styling, readable typography.

Palette: near-black #0B0B0C, warm off-white #E8E4DA, restrained phosphor green #7CFF6B. No other saturated colors. Thin charcoal borders, subtle translucency, very little bloom. Clean and quiet, not gamer/cyberpunk.

Composition: A narrow editorial header at top left says "Vigil" in refined large off-white sans serif, with "A desktop that notices you." beneath it. Top right small monospace label "CONCEPT PREVIEW". Below, occupying most of the image, a wide rounded macOS desktop preview with a subtle top menu bar. Its wallpaper is Field: hundreds of small evenly spaced muted green dots, forming a beautiful shallow flowing deformation toward a broad soft attention lens near center-left. The lens is a gentle diffuse glow with uncertainty, never a crisp dot, crosshair or target. Keep the scene simple and coherent, like an interactive living wallpaper.

Within the desktop, a compact non-activating floating Observation HUD at the upper right (around one fifth desktop width). Title "Observation". A black inset contains a minimal abstract face-landmark mask: elegant sparse green face contour, two eye outlines and small pupil markers, no photograph, no actual person, no filled robot head. Below the inset display only these clear labels in aligned monospace rows: "PRESENCE  Detected", "REGION    Center", "MODE      Mask". Small green status indicator and "LOCAL ONLY" at its bottom. These are illustrative UI labels, no measured fps, accuracy, benchmark or medical/focus scores. A tiny compact menu-bar popover nearby may show only "Field", "Iris", "Tide", and "Pause", with Field selected; don't clutter or overlap the HUD.

Below the main desktop preview, three slender aligned scene previews across the width, with labels "01  Field", "02  Iris", "03  Tide". Field shows the dot matrix; Iris shows one delicate elliptical ring displaced by head position; Tide shows a subtle wave lattice with a ripple. All green on near-black, restrained and coherent. Bottom margin small caption "Illustrative interface • Not a running application".

Constraints: No application code, no fake charts, no browser chrome, no download buttons, no customer logos, no feature cards with prose, no gaze cursor, no scanning surveillance imagery, no human photo, no devices, no photos of workspace, no red, no rainbow, no giant glow. Typography must be crisp. Render as a tasteful finished product concept that communicates the app at a glance.
```
