---
name: rescue-bad-photo
description: Repair and beautify uploaded photos while preserving the original subject, identity, texture, and important details. Use when the user asks to save a bad photo, make a photo prettier, improve exposure/color/sharpness/noise, shape light and shadow, apply tasteful grading or filters, crop or recompose with master-photographer-level composition, restore damaged or faded photos, colorize black-and-white photos, make landscape photos cinematic or breathtaking, optimize architecture, retouch portraits with natural skin, flattering light, focal-length feel, or background blur, optimize museum/gallery exhibit photos faithfully with exhibit-focused crop/recomposition and background blur, or prepare polished images for sharing or printing. Produces clearly labeled programmatic natural, programmatic beauty, AI natural, and AI beauty variants; beauty variants should usually feel stunning, grand, vibrant, and visibly transformed.
---

# Rescue Bad Photo

## Core Rule

Preserve the subject and factual image content. Improve exposure, color, contrast, composition, clarity, and damage without changing identity, clothing, facial structure, pose, scene meaning, product details, text, logos, artwork, or historically important marks unless the user explicitly asks. Switch optimization logic by subject type: landscapes can be emotionally heightened, architecture should preserve geometry and materials, portraits should preserve identity and natural skin, and museum exhibits should preserve artifact color, material, labels, and documentary trust.

Photography is the art of light and shadow. Treat light shaping as the primary beauty lever before filters, saturation, or generic cleanup. Every meaningful edit should decide where the key light feels like it comes from, where highlights should lead the eye, which shadows should add depth, and which dark areas should stay detailed. A beautiful result should have intentional luminance hierarchy, not just brighter exposure or stronger color.

## Preservation And Beauty Resolver

Separate hard anchors from soft anchors before prompting or editing. Hard anchors must remain stable: human identity, anatomy, expression, pose, clothing, important objects, readable text, logos, artwork content, museum artifact facts, architecture identity, landmarks, core scene layout, and product design. Soft anchors may be improved for beauty: lighting quality, time-of-day feel, sky drama, atmospheric depth, background clutter, nonessential colors, crop, aspect ratio, lens feel, bokeh, local contrast, and print finish.

Do not write prompts that preserve everything with equal force. Over-preserving weak original lighting, dull color, accidental crop, haze, clutter, or flat phone-camera depth will make the AI output bland. For AI beauty, preserve only the hard anchors and explicitly allow soft anchors to change enough to make the photo beautiful.

## Autopilot Default

When the user invokes this skill with only an uploaded image, infer the photo type and run the full built-in pipeline without asking for extra instructions. Do not require the user to say "make it prettier", "crop it", "use portrait logic", or "apply landscape logic".

Default behavior:

1. Classify the image as portrait, landscape/travel, architecture/interior, museum/gallery exhibit, product/food, document/artwork, black-and-white/old/damaged photo, or mixed scene.
2. Apply the matching subject-specific recipe automatically.
3. Choose an aesthetic direction automatically from the image content.
4. Perform beauty enhancement, composition/crop evaluation, local cleanup, and final QA by default.
5. Produce four labeled outputs by default: programmatic natural, programmatic beauty, AI natural, and AI beauty.
6. Use generative editing or regeneration for the AI variants when it materially improves beauty, repair, outpainting, relighting, sky/background reconstruction, or subject separation while preserving the image's important facts.
7. Ask a clarification only when there is a genuine conflict, such as faithful museum documentation versus dramatic poster styling, or when user instructions contradict preservation.

## Beauty Target

Do not stop at a clean repair. The default goal is a visibly more beautiful photograph: stronger visual hierarchy, more flattering light, more intentional color, better subject separation, cleaner background, improved composition, and a coherent mood. In most non-documentary scenes, beauty variants should feel stunning, grand, vivid, energetic, and immediately better at first glance. A successful result should feel photographed with better timing, lens choice, framing, and post-processing, not merely scrubbed of defects. Recomposition is part of the default beauty edit, not an optional afterthought.

Avoid timid edits. If the enhanced result looks almost the same as the original, iterate with stronger light direction, more confident crop, richer but controlled color, better subject separation, more atmosphere, and cleaner background hierarchy. Keep faithful naturalness for museum/document/artifact cases, but still make them clearer and more dignified.

Use photographer-informed visual language without copying a living artist's exact style. Translate references into general craft moves: tonal range, light direction, timing, color harmony, lens feel, scale, negative space, gesture, atmosphere, and print finish.

## Master Composition Rule

Treat crop and recomposition as a master-photographer-level creative decision for every photo type, not a cleanup step and not an exhibit-only rule. A strong edit should feel newly seen: cleaner edges, stronger subject scale, better visual flow, deliberate negative space, purposeful aspect ratio, and a frame that guides the viewer without explanation.

Do not preserve the camera's original framing just because it is available. For every non-strict-documentation image, compare multiple crops and choose the one with the strongest photographic intention. For strict documentation, still straighten, remove dead borders, correct perspective, and make the frame calmer unless doing so would remove required content.

Composition failure is beauty failure. If the beauty version has better color but the same weak accidental framing, it is not finished. Rework the frame before delivery or use outpainting when the best composition needs breathing room around a head, hand, building, exhibit, product, label, or landscape edge.

## Beauty Failure Rule

Treat every beauty variant as failed if it looks like a light cleanup, a cleaner duplicate, or a merely safer version of the natural edit. At thumbnail size and full size, the viewer should immediately feel stronger presence, better light, master-level composition, richer atmosphere, and a more premium photographic finish.

Do not deliver a weak beauty variant. If `program_beauty` is not clearly more attractive than `program_natural`, redo it with at least three stronger moves: bolder recomposition, more directional local light, clearer subject/background separation, richer but controlled palette, deeper tonal structure, background simplification, atmospheric depth, or a more decisive finish. If `ai_beauty` is not the most impressive of the four outputs, regenerate it with a stronger high-impact prompt and choose the best attempt.

AI beauty may be more transformative than programmatic beauty: change time-of-day feel, rebuild bland sky, add coherent atmospheric depth, extend canvas, simplify clutter, create natural lens separation, relight the subject, and strengthen crop or viewpoint feel when the source supports it. Preserve identity, anatomy, core scene geometry, landmarks, readable text, architecture, artifact truth, clothing, pose, and important details.

## Variant Output Requirement

Always deliver exactly four edited images unless the user explicitly asks for a different count:

- Programmatic natural: deterministic, faithful, clean, and tasteful. It should still be clearly improved, not barely changed. Use crop/recomposition, perspective correction, exposure, tone curve, color balance, saturation, local contrast, denoise, sharpening, vignette, dust/scratch cleanup, and non-generative background cleanup without pushing the look too far.
- Programmatic beauty: deterministic but more aesthetically assertive. Push mood, light shaping, color harmony, subject separation, crop, and polish further while preserving factual content. It should usually feel more impressive, atmospheric, vibrant, and premium than the natural version.
- AI natural: AI-assisted but restrained. Use generative repair, cleanup, outpainting, subtle relighting, restoration, background blur, or colorization where it improves the photo without making it look invented. It should improve the image visibly while staying plausible.
- AI beauty: AI-assisted and visibly more beautiful. Treat the upload as the subject/reference, not as a weak frame that must be pixel-locked. Go further on cinematic/editorial mood, relighting, outpainting, sky/background reconstruction, subject separation, scale, and atmosphere while preserving the hard anchors. It should usually be the most stunning, grand, energetic, and share-worthy version.

Keep the original image only as an internal reference. Do not output, display, link, copy, or count the original image as a deliverable unless the user explicitly asks for an original copy. Do not deliver temporary intermediates, contact sheets, before/after composites, or extra comparison images by default.

Each image must be clearly labeled in the filename and final response. Use labels exactly: `program_natural`, `program_beauty`, `ai_natural`, and `ai_beauty`.

Both AI variants must include the exact optimization prompts used or close reconstructions of them. Put the prompts in the final note under `AI natural prompt used:` and `AI beauty prompt used:` so the user can reuse or adjust them.

## Workflow

1. Inspect the uploaded image before editing. Identify subject type, key-light direction, shadow structure, lighting problem, color cast, sharpness, noise, damage, horizon, distractions, and the likely use case. If the user provided no detail, proceed with the Autopilot Default.
2. Choose an aesthetic direction before editing: clean natural, warm filmic, airy bright, dramatic cinematic, premium commercial, romantic portrait, faithful documentary, geometric architectural, quiet minimalist, street-poetic, vibrant travel, grand landscape, or another style that fits the subject.
3. Keep an untouched original copy only for internal reference and rollback. Create exactly four deliverable output copies: program_natural, program_beauty, ai_natural, and ai_beauty.
4. Build the programmatic natural version first. Apply faithful global corrections: white balance, exposure, highlight recovery, shadow lift, contrast, tone curve, and natural saturation.
5. Build the programmatic beauty version from the best programmatic natural or original source. Push deterministic aesthetic lift: shape light first, deepen or soften contrast, separate subject from background, simplify distractions, tune color harmony, strengthen crop, add vitality, and polish the mood using non-generative operations.
6. Apply local programmatic corrections where they improve beauty or fidelity: face/skin exposure, eye clarity, sky recovery, foreground separation, background cleanup, dust/scratch repair, mild dehaze, or selective noise reduction.
7. Perform a master composition pass for all four variants. Evaluate at least four framing choices: original aspect improved, tighter subject crop, expressive aspect ratio such as panoramic/vertical/square/cinematic wide, and negative-space or geometry-led composition. Judge subject scale, edge cleanliness, leading lines, gaze/motion room, balance, foreground/background relationship, and thumbnail impact. Default to the strongest recomposed/cropped output. Keep the original framing only when it is already the strongest frame or when crop would harm documentary accuracy, full-artwork edges, exhibit labels, group-photo completeness, or user-specified aspect ratio.
8. Create the AI natural and AI beauty variants from the best source: original, programmatic natural, programmatic beauty, or cropped/outpainted intermediate. Use explicit prompts that encode the detected photo type, natural/beauty variant intent, aesthetic direction, hard anchors to preserve, soft anchors that may change, crop/composition goal, and desired improvements. Keep AI beauty prompts shorter and more decisive than audit checklists; too many negative constraints can make the image timid.
9. For landscape images that should feel breathtaking, consider stronger sky, light, atmosphere, scale, foreground depth, color separation, and panoramic/cinematic crop. Use generative editing or full regeneration for the AI beauty variant when ordinary correction cannot create the requested impact from the available pixels.
10. For architecture, portraits, and museum exhibits, apply the subject-specific logic before any stylization.
11. Verify all four results visually at full image, zoomed-in detail, and thumbnail scale. Check for halos, waxy skin, crushed blacks, clipped highlights, warped faces, fake texture, color banding, over-sharpening, lost fine detail, and an edit that is merely clean but visually bland. Apply the Beauty Failure Rule: if a beauty variant does not look clearly more striking than the source and natural version, iterate before delivery; if AI beauty is not the strongest output, regenerate it with a bolder prompt that relaxes soft-anchor preservation.
12. Deliver only the four labeled edited images plus a concise note describing the detected photo type, variant labels, major differences, chosen crop/recomposition, and AI prompts used. Do not include the original or intermediate images in the final response. If no crop was applied, state why.

## Editing Priorities

- Natural first: make the image look like a good original photograph, not an obvious filter.
- Light and shadow first: decide the luminance hierarchy before saturation, filters, or stylistic color. Better light beats heavier color.
- Subject first: prioritize the face, person, product, animal, document, or focal object over background drama.
- Detail retention: protect hair, eyelashes, skin texture, fabric weave, printed text, edge lines, and small highlights.
- Color honesty: avoid unnatural skin tones, radioactive greens, cyan shadows, orange faces, and one-click preset looks.
- Beauty over sanitation: remove flaws, then improve mood, light, composition, vitality, and subject presence until the image is clearly more attractive.
- High-impact default: except for faithful documentation tasks, beauty variants should aim for an impressive, spacious, lively, premium result rather than a subtle clean-up.
- Master-level recomposition by default: do not preserve the camera's original framing out of inertia. Make crop, aspect ratio, subject scale, negative space, and edge control as deliberate as light and exposure decisions.
- Reversibility: keep factual content stable, but do not be timid with tasteful aesthetic improvement when the user asks to save or beautify a photo.
- Landscape impact: when the user asks for a stunning scenic result, optimize for awe, atmosphere, depth, light, and scale while avoiding fake-looking HDR or impossible scenery unless asked for fantasy.
- Subject-appropriate beauty: architectural, portrait, and museum photography each need different correction priorities; never apply a dramatic landscape grade by default to people, buildings, or artifacts.

## Composition Guidance

- Treat cropping/recomposition as mandatory master-level evaluation for every photo type. The final image should have a more intentional frame than the upload unless preservation requirements override it.
- Straighten horizons, architecture, table edges, and verticals when they are unintentionally tilted.
- Crop to strengthen eye line, gesture, leading lines, symmetry, negative space, subject scale, depth, rhythm, and edge cleanliness.
- Remove dead space, weak corners, accidental tangencies, half-visible distractions, and visual weight that competes with the subject.
- Choose aspect ratio deliberately: vertical for grandeur or portraits, panoramic for scale, square for stillness or object dignity, cinematic wide for atmosphere, and tighter editorial crop for presence.
- Avoid cutting through joints, fingertips, important props, typography, product edges, or hair silhouette.
- For portraits, usually leave breathing room toward the gaze direction and avoid placing eyes dead center unless the symmetry is intentional.
- For travel, landscape, food, product, and documentary images, preserve context that explains the scene.
- Consider generative outpainting when the best composition needs a little extra breathing room, a corrected edge, or a stronger aspect ratio; preserve subject and scene geometry.
- Export at the original resolution when possible; only resize when requested or required by the destination.

## Subject-Specific Logic

- Architecture: prioritize straight verticals, clean perspective, material texture, facade rhythm, spatial depth, shadow structure, and believable light. Avoid warped buildings, fake windows, altered signage, and over-HDR surfaces.
- Portrait: prioritize identity, flattering but natural light, healthy skin tone, eye clarity, hair detail, fabric texture, and expression. Retouch blemishes and distractions lightly; when useful, simulate a more portrait-like focal length and shallow depth of field through background blur, subject separation, and subtle perspective cleanup. Do not change facial structure, age, body shape, or personal features unless requested.
- Museum exhibits: prioritize documentary fidelity plus exhibit isolation. Correct glass glare, low museum lighting, white balance, label readability, and object texture while preserving true material, patina, brushwork, inscriptions, damage, provenance marks, and necessary display context. Recompose by default: straighten perspective, crop away empty walls, distracting visitors, case edges, and excess gallery space, and make the exhibit occupy a stronger, calmer position in the frame. Add natural background blur or depth separation by default when it makes the artifact more prominent; keep the artifact, inscriptions, labels that matter, frame, plinth, case edges, and material texture sharp.
- Product/food: prioritize appetizing or premium presentation, accurate geometry, clean surface texture, controlled highlights, color appetite/brand truth, and practical crop for sharing or commerce.
- Document/artwork: prioritize legibility, perspective correction, clean edges, faithful colors, and complete content; beauty edits must not damage text or artwork accuracy.
- Use generative edits more conservatively for portraits, architecture, and museum exhibits than for landscapes. Prefer local repair, glare reduction, perspective correction, and background cleanup over invention.

## Black-And-White, Faded, Or Damaged Photos

When the image is black-and-white, faded, torn, stained, scratched, scanned, or otherwise damaged:

1. Restore structure before color: dust/scratch cleanup, tear repair, contrast recovery, and tonal balancing.
2. If colorizing, infer plausible colors from context but avoid claiming historical certainty.
3. Keep skin, fabric, and background color restrained; vintage colorization should be believable, not neon.
4. Preserve original grain and age cues unless the user asks for a modern clean restoration.
5. If a missing area requires invention, say that reconstruction was inferred.

## Epic Landscape Enhancement

When the photo is a landscape, cityscape, travel scene, mountain, ocean, forest, desert, night sky, sunrise, sunset, cloudscape, or scenic viewpoint, assume the beauty variants should feel "大片", "震撼", "绝美", "cinematic", "epic", or "breathtaking" unless the user asks for restraint:

1. Push beyond simple correction. Build depth with foreground, midground, background separation; guide the eye with light; make atmosphere and scale legible.
2. Use dramatic but coherent color grading: golden hour warmth, cool shadows, storm contrast, alpine clarity, teal water, luminous sky, or filmic dusk only when it suits the scene.
3. Recover or enhance sky and light carefully. Avoid pasted-looking clouds, mismatched sun direction, overdone rays, and halos along mountains, trees, rooftops, and horizons.
4. Crop for impact: panoramic, vertical grandeur, wide cinematic, or tighter leading-line composition depending on the scene.
5. If the original lacks enough visual information, use generative editing to extend canvas, rebuild sky, add atmospheric depth, repair blown regions, or relight the scene. Full regeneration is acceptable when the user wants a magnificent interpretation rather than strict restoration.
6. When generating a new landscape from the uploaded image, preserve recognizable terrain, viewpoint, landmarks, human-made structures, and subject placement unless the user asks for a freer reimagining.

## Tool Use

Use the best available local or image-editing tool for the environment. For programmatic variants, prefer deterministic image-processing operations for exposure, curves, color, crop, perspective, denoise, sharpening, and scratch cleanup. For AI variants, use generative image editing or regeneration and instruct it to preserve only the hard anchors that matter for the detected subject. For AI beauty, explicitly ask for a high-impact, stunning, grand, vibrant photographic transformation while allowing soft anchors such as lighting, sky, background, crop, atmosphere, and lens feel to change; weak or over-constrained prompts produce weak beauty edits. For landscapes, instruct generative tools to preserve viewpoint and major scene structure while improving light, sky, atmosphere, scale, and composition. For architecture, preserve straight geometry, design intent, signage, facade details, and material truth. For portraits, preserve identity and natural anatomy; if simulating a longer focal length or shallow depth of field, keep facial proportions natural and protect hair, glasses, fingers, jewelry, and clothing edges from blur spill. For museum exhibits, preserve artifact authenticity and label content while adding realistic exhibit-focused background blur when the background is not itself the subject.

Read `references/photo-rescue-guide.md` when choosing detailed enhancement recipes, aesthetic lift strategy, restoration/colorization settings, or QA criteria for a non-trivial edit. If the user gives no specific instructions, still use it to select the appropriate default recipe.

Read `references/photographic-style-playbook.md` when the edit needs to become more beautiful, cinematic, editorial, atmospheric, street-like, fine-art, minimalist, or photographer-level rather than merely clean.

## Output Standard

Return exactly four labeled image outputs unless the user asks otherwise:

- `original-name_program_natural.png`: programmatic natural version.
- `original-name_program_beauty.png`: programmatic beauty version.
- `original-name_ai_natural.png`: AI natural version.
- `original-name_ai_beauty.png`: AI beauty version.

Do not return the uploaded original, an original copy, a before/after comparison, contact sheet, or temporary intermediate unless specifically requested. Include a short note naming the detected photo type, aesthetic direction, crop/recomposition decision, and a clearly labeled description of each output. Include `AI natural prompt used:` and `AI beauty prompt used:` followed by the prompts used for those AI variants. If AI images could not be generated because no AI image tool is available, provide only the two programmatic variants plus the exact two AI prompts that should be used; do not pad the output with the original image.
