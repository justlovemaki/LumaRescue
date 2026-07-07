# Photo Rescue Guide

## Diagnosis Checklist

- Autopilot classification: infer portrait, landscape/travel, architecture/interior, museum/gallery exhibit, product/food, document/artwork, black-and-white/old/damaged photo, or mixed scene before editing.
- Exposure: underexposed subject, blown highlights, flat midtones, crushed blacks.
- Color: white-balance cast, mixed lighting, faded scan, oversaturation, weak skin tone.
- Detail: motion blur, missed focus, noise, compression artifacts, excessive smoothing.
- Composition: tilted horizon, awkward crop, distracting edge elements, weak subject placement.
- Restoration: dust, scratches, tears, stains, missing emulsion, faded contrast, scan borders.
- Scenic impact: weak sky, flat light, poor depth, missing foreground anchor, unclear scale, dull atmosphere.
- Architecture: converging verticals, lens distortion, dull materials, blocked shadows, blown windows, messy edge clutter.
- Portrait: unflattering light, uneven skin tone, red eyes, harsh shadows, color cast, distracting background, weak subject separation, over-smoothed texture.
- Museum exhibit: low light, glare/reflections, mixed lighting, inaccurate color, unreadable labels, lost material texture.

## Light And Shadow First

Photography is the art of light and shadow. Before color grading, sharpening, filters, or beauty polish, decide the image's luminance hierarchy:

- Where should the viewer look first?
- What is the believable key-light direction?
- Which highlights should feel alive but not clipped?
- Which shadows should add depth, volume, mystery, or calm?
- Which dark areas need detail because they contain identity, text, material, or important context?

Avoid flat global brightening. A rescued photo should not make every area equally visible; it should make the important areas more luminous and the unimportant areas quieter. Use color as a supporting instrument after light and shadow establish the image's structure.

## Autopilot Decision Tree

When the user only says to use the skill, make these choices internally:

- If a face/person dominates: use Portrait Retouching Recipe, plus focal-length/background separation if useful.
- If nature, city view, travel scenery, sky, water, mountain, forest, or skyline dominates: use Epic Landscape Recipe or a calmer travel/scenic variant.
- If buildings, interiors, streets with architectural structure, or design details dominate: use Architecture Photography Recipe.
- If an artifact, painting, sculpture, display case, label, gallery wall, or museum object dominates: use Museum Exhibit Photography Recipe.
- If food or a sellable object dominates: use product/food logic under Photographer-Level Cropping and Aesthetic Lift Framework.
- If text, paper, artwork reproduction, or document fidelity dominates: prioritize perspective, legibility, complete edges, and faithful color over dramatic beauty.
- If the image is old, damaged, black-and-white, scratched, faded, or scanned: use restoration first, then colorization or beauty enhancement only after structure is repaired.
- If multiple types appear, optimize for the user's likely subject; when unclear, preserve all important content and choose the least destructive beauty edit.

Do not ask the user to choose a type unless two goals conflict.

## Variant Output Workflow

Always plan four labeled output variants:

- Programmatic natural: deterministic, faithful, clean, restrained.
- Programmatic beauty: deterministic, more polished and aesthetically assertive.
- AI natural: AI-assisted, restrained, faithful, cleaner and more dimensional.
- AI beauty: AI-assisted, more cinematic/editorial/atmospheric while preserving important facts.

The final deliverable should contain exactly these four labeled edited images by default. Keep the original upload only as an internal reference. Do not output the original, internal backup, intermediate crop, comparison grid, or contact sheet unless the user explicitly asks for it.

The AI prompts must be recorded and delivered with the final output. Build them from:

- Detected photo type.
- Variant intent: AI natural or AI beauty.
- Aesthetic direction.
- Hard anchors to preserve.
- Soft anchors that may be improved.
- Crop/recomposition goal.
- Subject-specific enhancement goals.
- Negative constraints such as no identity change, no warped geometry, no rewritten text, no fake artifact details, no plastic skin, and no fake HDR.

Prompt template:

`Enhance the uploaded photo as a [photo type] with a [aesthetic direction] photographic look. Preserve [specific hard anchors: identity, anatomy, text, artifact facts, architecture identity, landmarks, product design, or core scene layout]. Improve [soft anchors: light, crop, sky, background, color, subject separation, atmosphere, lens feel, restoration needs]. Use [crop/recomposition goal] if it strengthens the image. Keep it photorealistic and detailed. Avoid [short subject-specific negatives].`

Use two prompt strengths:

- AI natural prompt: restrained, faithful, natural-looking improvement that is still clearly better than the source.
- AI beauty prompt: stronger photographic beauty, more mood, more light shaping, more subject separation, more vitality, grander atmosphere, still photorealistic and detail-preserving.

## Prompt Conflict Resolver

Weak results often come from prompts that ask the model to "preserve exact" too much. Do not protect weak original lighting, dull weather, accidental crop, noisy shadows, clutter, flat phone depth, muddy color, or empty sky unless the user specifically wants faithful documentation.

Use this hierarchy:

- Hard anchors: identity, anatomy, expression, pose, clothing, important objects, text, logos, artwork content, artifact facts, building identity, landmarks, product design, and core scene layout.
- Soft anchors: light direction, time-of-day feeling, weather mood, sky texture, background clutter, crop, aspect ratio, lens compression, bokeh, nonessential colors, contrast, haze, and print finish.
- AI natural: preserve hard anchors and most soft anchors; improve gently.
- AI beauty: preserve hard anchors; actively improve soft anchors to create a stronger photograph.

Prompt order matters. Put the desired beautiful result first, then the hard anchors, then a short negative list. Long negative lists and blanket "preserve exact..." wording can make the model choose a timid cleanup.

## Natural Enhancement Recipes

Use small cumulative corrections. Prefer believable improvement over maximum impact.

## Aesthetic Lift Framework

Use this after basic repair. The image must become more attractive, not only technically cleaner.

## Master-Level Cropping And Composition

Cropping and recomposition are not minor corrections. Treat them as the photographer's second chance to remake the image. For every photo type, decide what the frame is about, how the eye enters, where it rests, and what should be excluded.

Before final export, compare at least four candidate frames:

- Clean original-ratio correction: straighten, correct perspective, remove dead borders and edge distractions.
- Subject-dominant crop: make the face, exhibit, building, product, food, or scenic anchor larger and more emotionally present.
- Expressive aspect crop: vertical grandeur, panoramic scale, square stillness, cinematic wide atmosphere, or editorial tightness.
- Negative-space or geometry-led crop: use emptiness, symmetry, leading lines, foreground layers, or repeated structure to create intention.

Choose the strongest frame, not the safest frame. A master-level crop should improve subject scale, visual hierarchy, edge cleanliness, rhythm, depth, and emotional intent. It should remove accidental corners, half-visible distractions, weak empty space, awkward tangencies, and visual weight that competes with the subject.

Keep original framing only when it is already the strongest composition or when cropping would remove required information: full artwork edges, complete document text, all group members, important labels, product boundaries, architectural identity, or user-requested dimensions. If a better crop needs space, use outpainting rather than settling for a weak frame.

## High-Impact Default

For most scenes, especially travel, landscape, city, food, product, lifestyle, architecture, and portraits, the beauty variants should be clearly more stunning, grand, vivid, energetic, and premium than the source. Do not treat "natural" as "barely changed"; natural should mean plausible and tasteful, not weak.

Escalate beauty when the result feels too similar to the original:

- Stronger master-level crop or recomposition.
- More directional light and local dodge/burn.
- Richer but controlled color contrast.
- Cleaner background hierarchy.
- Better subject separation and depth.
- More atmosphere, glow, haze, clarity, or texture where appropriate.
- More confident highlights and deeper but detailed shadows.

Hold back only when fidelity dominates: museum documentation, documents, artwork reproduction, product color accuracy, identity-sensitive portraits, medical/legal/evidence-like images, or user-requested conservative edits.

## Beauty Wow Test

Before delivery, judge each beauty variant with a two-second thumbnail test and a full-size side-by-side test against the natural version. The improvement must be visible first in light/shadow hierarchy, then in composition, color, subject separation, atmosphere, or finish without needing explanation. If the result reads as "cleaner but basically the same", it fails.

When a beauty variant fails, do not make tiny slider changes. Choose at least three escalation levers and redo the image:

- Crop/recompose more decisively: larger subject, stronger negative space, cleaner edges, panoramic/vertical/editorial aspect, better leading lines, or a more intentional geometry.
- Shape light locally: face lift, rim glow, sky glow, directional dodge/burn, deeper but detailed shadows, brighter subject plane, stronger key-light logic.
- Build color character: warm highlights/cool shadows, richer travel color, premium neutral contrast, appetizing food color, or cleaner skin/background separation.
- Increase depth: background blur for portraits, atmospheric layers for landscapes, foreground/midground/background separation, or selective clarity.
- Simplify distractions: remove edge clutter, reduce background saturation, soften nonessential detail, clean glare, or calm messy color patches.
- Add a finish: subtle print contrast, controlled grain, refined vignette, richer micro-contrast on the subject, or polished export sharpening.

Escalate by scene type:

- Landscape/travel/city: stronger time-of-day feel, dramatic but coherent sky, atmospheric depth, luminous water or snow, clearer scale, richer foreground, panoramic or vertical grandeur.
- Portrait: editorial light, brighter eyes, natural catchlights, healthier skin color, realistic longer-focal-length feel, shallow background separation, cleaner background, stronger crop around expression.
- Architecture/interior: hero perspective, clean verticals, stronger material contrast, premium shadow rhythm, reduced clutter, more orderly geometry.
- Food/product: commercial light, appetizing highlights, tactile texture, clean surface/background, premium color contrast, platform-ready crop.
- Museum/document/artwork: avoid theatrical drama; make it catalogue-quality, clear, dignified, straight, glare-reduced, materially faithful, appropriately cropped/recomposed, and for three-dimensional exhibits or display cases use natural background blur to isolate the object.

AI beauty prompt baseline:

`Create a high-impact photographic beauty version of the uploaded photo. Make it feel stunning, grand, vibrant, luminous, and intentionally photographed, not merely cleaned. Preserve the hard anchors: [specific identity/anatomy/text/artifact/building/landmark/product/core-layout details]. Improve the soft anchors boldly: master-photographer-level crop and composition, shaped light and shadow, subject separation, atmosphere, sky or background, lens feel, color harmony, depth, and premium print finish. Treat the upload as the subject and reference, but do not preserve weak original lighting, dull color, accidental crop, clutter, or flat phone depth. Keep it photorealistic; avoid fake HDR, plastic skin, warped geometry, invented key facts, rewritten text, and loss of fine detail.`

### Visual Hierarchy

Make the viewer know where to look first. Brighten, sharpen, warm, or add contrast to the subject; darken, cool, soften, or simplify less important areas. Remove or reduce edge distractions that pull attention away from the subject.

### Light Shaping

Create the feeling of better light. Add subtle dodge and burn, face/subject lift, rim-light emphasis, sky glow, window-light softness, or directional contrast when the source supports it. Avoid flat global brightening that makes everything equally important. The edit should feel lit, not merely exposed.

### Color Harmony

Choose a coherent palette instead of neutralizing everything. Examples: warm highlights with clean cool shadows, soft pastel portrait tones, rich golden-hour travel color, calm museum neutrals, crisp architectural whites, or moody cinematic contrast. Reduce clashing colors in the background when they distract from the subject.

### Subject Separation

Use local contrast, selective sharpening, depth-of-field blur, haze control, background cleanup, and crop to separate the subject. The subject should feel more present and dimensional after editing.

### Composition Upgrade

Reframe for intention. Improve balance, negative space, leading lines, gaze direction, symmetry, foreground/background relationship, and edge cleanliness. A technically correct crop that still feels accidental is not enough.

### Mandatory Crop Decision

For every beauty edit, compare at least three compositions before final export:

- Original-ratio refinement: straighten, trim dead edges, reduce distractions, improve balance.
- Subject-strength crop: tighter framing that makes the subject larger, clearer, and more emotionally present.
- Expressive crop: cinematic wide, vertical grandeur, square editorial, panoramic landscape, or negative-space composition.

Default to the strongest recomposed version. Preserve the original framing only if it is already the strongest composition or if cropping would remove necessary context, labels, full artwork edges, group members, product boundaries, architectural identity, or user-required dimensions. If no crop is used, mention the reason. A crop that merely trims borders is not enough for a beauty variant unless the original composition is already excellent.

Use outpainting when the better crop needs extra space around a head, hands, building top, mountain edge, product, label, or artwork border. Keep added space plausible and visually quiet.

### Finish

Add a final polish pass: micro-contrast where texture matters, gentle vignette or edge burn only when invisible, tasteful grain if it helps, and export sharpening appropriate to the final size. Stop before the image looks preset-heavy or artificial.

If a clean edit looks bland or too similar to the original, push two or three aesthetic dimensions further: stronger light direction, better crop, warmer/cooler mood, background simplification, subject separation, atmosphere, depth, or a more confident color palette. Do not simply increase saturation and contrast everywhere.

### Underexposed Photo

Raise exposure/midtones carefully, lift shadows selectively, reduce noise after shadow recovery, then add mild contrast. Protect highlights and avoid gray blacks. If the subject is a face, brighten the face locally instead of lifting the whole frame too far.

### Overexposed Photo

Recover highlights first, reduce whites, rebuild contrast with a gentle curve, and use selective dehaze only where it improves texture. Do not add fake detail into fully clipped areas unless restoration is explicitly requested.

### Flat Or Hazy Photo

Set black/white points conservatively, add midtone contrast, use mild clarity or local contrast, and increase saturation only after the tone is stable. Watch for halos around buildings, hair, trees, and skyline edges.

### Color Cast Or Mixed Lighting

Neutralize global white balance from known neutrals when possible. For mixed light, correct the subject first and let background light remain slightly warm/cool if that looks natural. Skin should not become gray, orange, magenta, or green.

### Noisy Low-Light Photo

Apply luminance noise reduction before final sharpening. Preserve edges and skin texture. Sharpen only important edges and avoid sharpening chroma noise or compression blocks.

### Soft Or Slightly Blurry Photo

Use deconvolution/unsharp masking modestly. Improve perceived sharpness through contrast, local clarity, and subject separation. Do not over-sharpen faces, text edges, or high-contrast silhouettes.

## Epic Landscape Recipe

Use this when editing a landscape or scenic view for a beauty variant. The default should feel like a breathtaking scenic blockbuster rather than merely corrected unless documentation or realism constraints require restraint.

### Tonal Drama

Create a strong but believable luminance hierarchy. Let the eye land on the main mountain, coastline, city skyline, road, waterfall, temple, tree, or sunlit area. Use deeper blacks and brighter highlights than a neutral edit, but keep shadow texture and avoid clipping broad sky or snow.

### Light And Atmosphere

Shape light as if a skilled landscape photographer waited for the right moment. Enhance golden hour glow, storm break, mist, haze layers, rim light, water reflections, or night-sky luminosity only when the image supports it. Match sun direction and shadow direction. Avoid light beams that cross objects impossibly.

### Sky Enhancement

Recover sky detail first. If the sky is empty, blown out, or too dull, use generative editing or replacement only when needed. Match cloud perspective, focal length, weather, horizon line, and reflected colors in water, glass, snow, and wet ground. Keep tree and mountain edges clean.

### Depth And Scale

Increase separation between foreground, midground, and background through contrast, haze, color temperature, and sharpness. Keep foreground texture crisp, distant objects slightly softer, and atmospheric perspective believable. If people, boats, cars, buildings, or animals show scale, preserve them.

### Color Direction

Choose one clear mood:

- Golden epic: warm highlights, clean blue shadows, luminous sky.
- Storm cinematic: cool shadows, silver highlights, dramatic cloud contrast.
- Alpine clean: crisp neutrals, deep blue sky, restrained saturation.
- Ocean/travel: clear water color, warm sand/stone, realistic foliage.
- Twilight/night: controlled blue hour, preserved city lights/stars, no muddy blacks.

Avoid single-slider HDR, oversaturated foliage, cyan shadows everywhere, purple skies with mismatched ground, and neon sunsets.

### Composition For Impact

Straighten horizon and correct perspective before cropping. Use panoramic crop for wide scale, vertical crop for cliffs/waterfalls/trees, foreground-heavy crop for immersion, or road/river/shoreline leading lines for motion. Keep the best sky/land ratio; dramatic sky can dominate, but only if it earns the frame. Do not deliver a landscape beauty edit without testing whether panoramic or vertical cropping makes it more powerful.

## Generative Landscape Rebuild

Use generative editing or full regeneration when the request asks for an awe-inspiring scenic result and the source image cannot get there with tonal editing alone.

Good uses:

- Extend canvas into a stronger panorama or vertical grand scene.
- Replace a blank or blown sky with a coherent dramatic sky.
- Rebuild clipped highlights, missing cloud texture, or damaged scenic areas.
- Add plausible mist, atmospheric layers, sunset glow, reflected light, or star detail.
- Remove distracting tourists, wires, trash, signs, or edge clutter when they are not the subject.

Boundaries:

- Preserve known landmarks, mountain shapes, coastline, skyline, road layout, buildings, water bodies, and viewpoint unless the user asks for fantasy.
- Do not add fake landmarks, impossible moons, duplicated mountains, extra roads, altered building identities, or unsafe-looking terrain.
- If the result is a generated reinterpretation rather than a strict edit, say so in the delivery note.

Prompt pattern for generative editing:

`Create a breathtaking cinematic landscape enhancement from the uploaded photo. Preserve the viewpoint, main landforms, skyline, waterline, buildings, roads, people, and scene geometry. Improve dramatic natural light, atmospheric depth, sky detail, color harmony, and professional composition. Keep it photorealistic, high-detail, clean edges, no fake HDR, no warped structures, no invented landmarks unless necessary for reconstruction.`

## Architecture Photography Recipe

Use this for buildings, interiors, bridges, streets with strong architectural subject, historic sites, real estate, hotels, temples, churches, museums, and design details.

### Geometry And Perspective

Correct lens distortion and converging verticals before color grading. Keep verticals vertical unless the tilted perspective is clearly intentional. Preserve facade proportions, rooflines, columns, windows, stairs, railings, signage, and repeated patterns. Avoid generative edits that bend walls, duplicate windows, or invent structural details.

### Light And Material

Make materials feel tactile and beautiful: stone, concrete, brick, wood, metal, glass, tile, fabric, and plaster should retain texture. Recover window highlights when possible without making interiors look fake. Use contrast to reveal form, bring out rhythm and depth, and make the building feel intentional. Avoid crunchy HDR halos around rooflines and edges.

### Color Direction

Keep white walls, stone, concrete, and metal believable. Remove ugly color casts from mixed indoor light, but preserve intentional warm lighting in hotels, galleries, restaurants, temples, and night architecture. For modern architecture, use clean neutrals and crisp separation; for historic architecture, preserve patina and age.

### Composition

Choose symmetry, one-point perspective, strong vertical grandeur, facade rhythm, or detail abstraction based on the image. Crop cleanly around building edges and avoid cutting important arches, signs, doors, domes, towers, or corners awkwardly. A good architectural edit should feel calmer, more premium, and more designed than the source. Try at least one geometry-led crop that aligns the building to the frame.

## Portrait Retouching Recipe

Use this for individual portraits, selfies, group photos, candid people, wedding/travel portraits, profile images, and environmental portraits.

### Identity And Skin

Preserve facial structure, age, expression, scars, moles, freckles, hairline, body shape, clothing, and personal marks. Retouch temporary blemishes, red-eye, under-eye harshness, shine, and distractions lightly. Keep pores and natural skin texture; avoid plastic smoothing and face reshaping.

### Light And Color

Prioritize natural skin tone before background color. Correct green/magenta casts, mixed lighting, red/orange skin, and dull eyes. Add gentle catchlight and local face brightness only if it remains believable. Shape flattering light on the face, reduce background color noise, and make the person feel more luminous and present. Keep hair, eyelashes, eyebrows, fabric texture, jewelry, and glasses crisp.

### Focal Length And Background Blur

For portraits, use shallow depth of field to separate the person from a distracting background. Prefer realistic lens behavior: the subject's eyes, face, hairline, hands near the face, clothing edges, jewelry, and glasses should remain sharp; background blur should increase with distance from the focus plane. Avoid smearing hair, cutting out ears, blurring fingers, or creating a cardboard cutout edge.

When the source looks like a wide-angle phone portrait, improve the portrait feel carefully:

- Use crop and perspective correction to reduce edge distortion and make facial proportions more natural.
- Simulate mild telephoto compression only if it does not reshape the face or body.
- Use a portrait-like depth of field equivalent to a moderate telephoto lens, not an extreme fake blur.
- Keep environmental portraits readable when the background explains the person, place, or story.

Use AI generation only if local blur/masking cannot separate the subject cleanly. Ask the model to preserve exact identity, anatomy, clothing, pose, and background layout while adding natural lens blur and subject separation.

### Composition

Crop for expression and posture. Avoid cutting through fingers, wrists, elbows, knees, chin, hair, or important clothing details. Leave space into gaze or motion. Try a tighter portrait crop, an environmental portrait crop, and a negative-space/editorial crop when the image allows. For group photos, preserve every face, gesture, and relationship. A portrait beauty edit should make the person look better lit, more emotionally present, and more intentionally photographed without making them look like a different person.

### Generative Boundaries

Use generative tools only for background cleanup, natural lens blur, small clothing/hair repairs, eye-glass glare reduction, or missing edge extension. Do not regenerate the face, alter anatomy, change age, beautify into a different person, or add makeup/clothing unless requested.

Prompt pattern for generative portrait repair:

`Enhance this portrait while preserving the person's exact identity, facial structure, expression, age, skin texture, hair, clothing, pose, and background context. Improve natural light, color balance, eye clarity, mild blemishes, and distractions. Add natural portrait lens separation with realistic background blur if helpful, keeping hair, glasses, fingers, jewelry, and clothing edges clean. No face reshaping, no plastic skin, no changed anatomy, no changed clothing.`

## Museum Exhibit Photography Recipe

Use this for artifacts, paintings, sculptures, fossils, jewelry, ceramics, manuscripts, textiles, installations, display cases, gallery walls, museum labels, auction/documentation shots, and cultural heritage objects.

### Documentary Fidelity

Treat the exhibit as evidence, not decoration. Preserve true color, material, patina, cracks, brushwork, inscriptions, labels, inventory marks, mount, case, frame, and damage. Do not "restore" an artifact to a new-looking state unless the user explicitly asks for a speculative reconstruction.

### Lighting And Glare

Museum photos often have dim light, glass reflections, spotlights, and mixed color temperature. Reduce glare and reflections locally where possible while preserving visible surface texture and display context. Recover shadows without flattening sculpture volume or painting brushwork. Make the exhibit feel clear, dignified, and gallery-quality rather than aggressively stylized.

### Exhibit Isolation And Background Blur

By default, make the exhibit stand out from the museum environment with realistic depth separation. Keep the artifact, object edges, inscriptions, important labels, frame, plinth, display case front plane, and material texture sharp. Blur or soften nonessential background walls, distant cases, visitors, reflections, visual clutter, and empty gallery space when it improves focus.

Use blur like museum/gallery photography, not portrait cutout blur:

- Apply gradual depth falloff based on distance from the exhibit.
- Preserve glass reflections only when they reveal the display case or material truth; reduce distracting reflections.
- Keep labels readable when they are part of the documentation goal; if the label is background clutter, soften it gently instead of inventing or rewriting text.
- Avoid halo edges around sculptures, pottery, fossils, jewelry, frames, and transparent display cases.
- Do not blur the artifact's own relief, brushwork, surface cracks, patina, inscriptions, mounts, or base.

### Exhibit Crop And Recomposition

Crop and recompose exhibit photos by default unless full-context documentation is more important. The goal is a calm museum catalogue or gallery-publication frame: the exhibit should feel intentional, centered or deliberately off-center, and visually separated from wall clutter.

Evaluate at least three exhibit compositions:

- Documentation crop: straighten perspective and preserve the full object, frame, plinth, display case, and important label.
- Hero exhibit crop: make the artifact larger and more prominent while keeping complete silhouette, base, inscriptions, and necessary scale/context.
- Editorial gallery crop: use negative space, symmetry, a vertical frame, square frame, or quiet off-center placement when it gives the object more dignity.

Remove or reduce empty wall, floor, ceiling, edge visitors, case reflections, neighboring exhibits, and awkward partial labels unless they are necessary to understand the object. Do not crop through an artifact's base, hands, tools, inscriptions, frame corners, sculpture silhouette, object shadow, or label that the user needs to read. Use outpainting when the best crop needs a little breathing room around the object, frame, plinth, or label.

### Color And Material

Use neutral white balance when the goal is documentation. Preserve warm gallery lighting if it supports the viewing atmosphere, but avoid color shifts that misrepresent the object. Metallic, ceramic, paper, textile, stone, lacquer, and pigment surfaces should keep distinct texture and reflectance.

### Framing And Perspective

Straighten frames, plinths, vitrines, labels, and wall edges. For paintings/documents, correct perspective while preserving full artwork edges. For sculptures, preserve volume and silhouette; do not crop off base, hands, tools, inscriptions, or scale references unless intentional. Crop museum images to remove empty walls or distracting visitors only when the artifact, label, scale, and display context remain faithful. The result should look like a high-quality museum catalogue or gallery documentation image.

### Generative Boundaries

Use generative tools only for removing glare, dust, sensor spots, mild background clutter, extending a missing border, or creating realistic exhibit-focused background blur. Do not invent missing artifact details, rewrite labels, change colors, remove age marks, alter inscriptions, or replace material texture. If any reconstruction is inferred, say so.

Prompt pattern for exhibit repair:

`Enhance this museum exhibit photograph for faithful, beautiful gallery documentation. Preserve the exact artifact, material, patina, damage, inscriptions, important labels, frame, display case, mount, and proportions. Correct perspective and recompose with an intentional museum-catalogue crop: remove excess wall/floor/clutter, make the exhibit more prominent, and keep necessary label or display context. Shape dignified museum light, reduce glare/noise, correct white balance, improve readability and texture, and add realistic background blur/depth separation so the exhibit is clearly isolated from nonessential gallery clutter. Keep the artifact and important label text sharp. Do not invent missing details, recolor the object inaccurately, rewrite text, make the artifact look new, crop off important object parts, or create halo blur around object edges.`

## Photographer-Level Cropping

- Portrait: keep eyes near upper third when natural; leave space into gaze or motion; avoid cutting hands and hair unnaturally.
- Group photo: preserve every face and meaningful spacing; do not crop too close to heads or shoulders.
- Architecture: keep verticals clean; crop around structural edges, symmetry, vanishing points, and repeated patterns.
- Museum exhibit: preserve the full object, frame, plinth, and necessary label/case context, but crop away empty walls, edge clutter, visitors, and excess gallery space; use a hero crop or quiet negative-space crop when it makes the exhibit more dignified.
- Product: keep product geometry accurate and leave margin for platform use; straighten verticals and horizontals.
- Food: crop to highlight texture and shape; avoid amputating plates or utensils unless the crop feels deliberate.
- Landscape/city: straighten horizon; use leading lines, foreground interest, and sky/ground balance.
- Document/artwork: preserve full edges unless the user asks for a presentation crop; correct perspective without warping text.

## Black-And-White Colorization

1. Restore contrast and damage first.
2. Colorize with plausible low-to-medium saturation.
3. Use natural skin variation, not a single flat skin color.
4. Keep whites, blacks, metal, stone, and paper from becoming tinted unless context supports it.
5. Mention that colors are inferred when historical accuracy is uncertain.

## Restoration Boundaries

Allowed by default:

- Remove dust, scratches, fold marks, scan borders, stains, sensor spots, red-eye, mild background clutter, and compression artifacts.
- Repair small missing areas using surrounding texture.
- Improve faded contrast, color balance, and legibility.

Avoid unless requested:

- Changing age, expression, body shape, hairstyle, clothing, background location, product design, artwork content, document text, logos, jewelry, or identifying marks.
- Replacing faces or inventing major missing content.
- Turning a documentary or archival photo into a fantasy/studio look.
- Replacing real landscape geography or landmarks when the user expects a faithful travel/scenic edit.
- Altering building structure, museum artifact details, inscriptions, labels, or portrait identity.

## QA Before Delivery

Inspect at fit-to-screen and at 100% zoom:

- Four labeled variants are present by default: programmatic natural, programmatic beauty, AI natural, and AI beauty; or the reason AI images could not be produced is stated.
- No original upload, internal backup, intermediate image, or comparison grid is included as a default deliverable.
- The final response includes the AI natural and AI beauty optimization prompts used.
- Subject identity and important details are unchanged.
- Edits do not create halos, plastic skin, smeared hair, duplicated texture, warped geometry, or fake bokeh.
- Crop/recomposition was actively evaluated; the final frame is more intentional than the source, or the reason for retaining original framing is clear.
- Cropping and composition feel photographer-level: subject scale, edge cleanliness, visual flow, aspect ratio, and negative space are deliberate.
- Crop does not remove important context or create awkward tangencies.
- Highlights and shadows retain useful detail where possible.
- Light and shadow have intentional hierarchy; the edit is not just brighter, more saturated, or cleaner.
- The image is not merely clean; it has stronger visual hierarchy, light, mood, subject separation, and composition than the source.
- Beauty variants are not subtle duplicates of the original or natural version; they feel clearly more impressive, spacious, lively, premium, or emotionally engaging while staying appropriate to the subject.
- AI beauty is the most visually compelling of the four outputs. If it is not, regenerate or strengthen it before delivery.
- Colors look plausible on skin, sky, foliage, food, fabric, and neutral surfaces.
- For landscapes, sky, light direction, reflections, terrain, and atmospheric depth are coherent.
- For architecture, verticals, facade rhythm, signage, and material texture remain coherent.
- For portraits, identity, anatomy, skin texture, hair, clothing, focal-length feel, and background blur remain natural.
- For museum exhibits, artifact color, texture, labels, inscriptions, patina, and damage remain faithful; crop/recomposition makes the exhibit more intentional and prominent; the exhibit is sharp and nonessential background is naturally softened unless documentation requires full-context sharpness.
- Final file opens correctly and is saved in a practical format.
