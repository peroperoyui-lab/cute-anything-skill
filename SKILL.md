---
name: cute-anything
description: Transform a reference image into a cute two-part character study: keep the original photo as the upper panel, then redraw the same subject below as a tiny naive hand-drawn creature. Preserve the subject's identity cues while making the lower drawing deliberately simple, loose, and adorable.
---

# Cute Anything

Turn **anything recognizable in a photo** into a tiny cute hand-drawn creature while keeping the original photo visible for comparison.

The core visual idea is:

**original subject above → same subject, cutified and doodled below**

This is **not** a postcard, travel-zine, scrapbook, magazine, or full-scene watercolor skill.

## When to use

Use this skill when the user asks for things like:

- “把这个做成上面原图、下面可爱小画”
- “把照片里的动物画成下面这种小生物”
- “cute anything”
- “原图 + 手绘小动物对照”
- “把这个东西拟成一个可爱的小生物”
- “保留照片，上面真实、下面涂鸦”

If the image contains multiple plausible subjects and the user did not specify one, choose the most visually salient subject when the choice is obvious. Ask only when the choice is genuinely ambiguous.

## Output format

Default to **one composite image**.

### Upper panel: source photo
- Occupy roughly **55–65%** of the canvas.
- Keep it photographic.
- Preserve the original subject, pose, lighting, texture, and scene.
- Cropping is allowed to focus attention on the chosen subject.
- Do **not** repaint, watercolorize, beautify, or stylize the upper photo.
- Do **not** replace the original background with an invented scene.

### Lower panel: cute creature reinterpretation
- Occupy roughly **35–45%** of the canvas.
- Use a warm white or paper-white empty background.
- Draw only the selected subject, not the whole original scene.
- Keep generous negative space.
- The creature should feel small, spontaneous, and slightly silly rather than polished.
- No caption, date, location, number, stamp, border decoration, or title unless the user explicitly asks for text.

The relationship between panels should be immediately obvious: the lower creature is the same thing as the upper subject.

## Subject extraction

Before drawing, internally identify **3–6 identity cues** from the source. Preserve these cues in the lower creature.

Useful cues include:
- silhouette
- head shape
- ear / horn / crest shape
- tail shape
- beak or muzzle shape
- dominant color blocks
- distinctive markings
- eye placement
- posture
- one memorable accessory
- unusual proportion or gesture

Do not preserve every photographic detail. Preserve the details that make the subject recognizable.

### Animals
Keep species cues and the most recognizable markings, then simplify aggressively.

### Objects
Turn the object into a tiny creature while preserving its iconic geometry, color blocks, openings, handles, buttons, or protrusions. Add only minimal eyes/limbs when needed.

### Food / plants / miscellaneous things
Use the same rule: preserve the recognizable core shape, then add the minimum anatomy needed to make it feel alive.

## Cute-creature style

The lower drawing should look like a charming doodle made quickly by hand.

### Linework
- loose black or dark-gray pencil / graphite line
- slightly shaky contour
- uneven line weight
- occasional broken or doubled line
- imperfect symmetry
- tiny scribbles for texture
- avoid clean vector curves

### Color
- low-saturation colored-pencil or very light watercolor wash
- translucent, uneven fill
- leave some white gaps
- color may slightly escape the outline
- no glossy digital rendering
- no realistic fur rendering
- no smooth airbrush gradients

### Shape language
- simplified rounded mass
- slightly oversized head when appropriate
- tiny body or compact torso
- short or abbreviated limbs
- small dot-like eyes
- tiny mouth / beak
- expression: innocent, blank, curious, mildly confused, or quietly happy
- preserve the original pose whenever possible

Cute does **not** mean anime eyes, Disney polish, plush-toy rendering, or chibi vector art.

The ideal result feels like:

> “someone noticed the funniest/cutest thing about the subject and captured it in five imperfect strokes.”

## Important visual rule: cute, not artistic

Prefer:
- naive doodle
- notebook sketch
- tiny diary illustration
- handmade sticker sketch
- children’s scribble with good observation
- soft pencil + imperfect watercolor

Avoid:
- travel postcard
- editorial illustration
- painterly landscape
- professional children’s-book rendering
- elegant botanical illustration
- polished concept art
- retro poster
- cinematic frame
- scrapbook collage
- zine typography
- decorative frames
- elaborate paper textures
- large titles or metadata

If the result starts looking “beautiful” before it looks “cute”, simplify it.

## Composition rules

Default composition:
1. clean photo panel on top
2. breathing room
3. small creature drawing below, centered or slightly off-center
4. lots of blank space around the creature

The lower creature should usually occupy only **20–35% of the lower panel**, not fill the entire area.

A faint paper texture is acceptable, but the page should still read as mostly plain white.

Do not add a heavy divider. A simple margin or whitespace separation is enough.

## Transformation strength

Use these internal modes when the user's wording implies them:

- **more faithful**: preserve pose, silhouette, markings, and proportions more strongly
- **more cute**: enlarge head slightly, compact body, shorten limbs, soften shape
- **more doodly**: rougher lines, less detail, less complete coloring
- **more weird-cute**: keep an awkward pose or odd expression instead of correcting it
- **more minimal**: reduce to only the strongest identifying marks

Default balance: **recognizable first, cute second, polished last**.

## Prompt construction

When calling an image generation/editing model, construct the request around this structure:

1. Identify the chosen subject and its key cues.
2. State that the upper panel must preserve the source photograph.
3. State that the lower panel must redraw only that subject.
4. Describe the naive doodle style in concrete rendering terms.
5. State the layout ratio and large amount of white space.
6. Add explicit exclusions against postcard/zine/polished illustration drift.

Reusable prompt skeleton:

> Create one vertically composed image from the provided reference. In the upper 55–65%, keep the selected subject as a faithful photographic crop from the original image; do not stylize the photo. In the lower 35–45%, redraw only that same subject as a tiny naive hand-drawn creature on a plain warm-white background. Preserve these identity cues: [CUES]. Keep the original pose or gesture when possible. Use loose shaky dark pencil lines, uneven contours, minimal dot-like facial features, simplified rounded anatomy, and sparse low-saturation colored-pencil / translucent watercolor fills with small white gaps and occasional color outside the outline. Make it cute, slightly awkward, handmade, and intentionally unpolished. Leave abundant negative space. No text, dates, location labels, postcard layout, zine typography, decorative borders, scene repainting, vector mascot style, anime eyes, 3D rendering, realistic fur painting, or polished children’s-book illustration.

## Example: cockatiel

If the chosen subject is a cockatiel standing in an awkward upright pose:

Identity cues to keep:
- tall yellow crest
- round orange cheek patch
- pale cream/yellow body
- long narrow tail
- small curved beak
- upright slightly ridiculous stance

Lower drawing:
- tiny pear-shaped bird body
- crest reduced to 3–5 quick pencil strokes
- orange cheeks as imperfect round color spots
- two dot eyes
- tiny feet
- long tail indicated with only a few strokes
- preserve the funny standing posture
- do not add a branch, cage, scenery, title, or decorative elements unless visible cues are essential

## Quality check

Before finalizing, verify all of the following:

- [ ] Upper panel still looks like the original photograph.
- [ ] The chosen subject is clear.
- [ ] Lower panel contains the same subject, not a generic cute animal.
- [ ] At least 3 identity cues survived the transformation.
- [ ] Lower drawing is visibly hand-drawn and imperfect.
- [ ] The creature is small relative to the blank lower panel.
- [ ] There is substantial white space.
- [ ] No unnecessary text or postcard metadata appeared.
- [ ] No full-scene watercolor reinterpretation appeared.
- [ ] The result feels cute before it feels “designed.”
