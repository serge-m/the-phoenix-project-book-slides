# Generate the next paragraph image

Process paragraph **<PARAGRAPH_NUMBER>** of the *The Phoenix Project* Slidev presentation.

## Project context

- The complete authoritative story is in `short_version1.md`. Read all 34 paragraphs before doing any work.
- The presentation source is `slides.md`.
- The reusable slide component is `components/NarrativeSlide.vue`.
- Existing accepted images are in `public/images/`.
- Existing documented generation briefs are in `prompts/`.
- There is one image per numbered paragraph. Each narrative slide contains two consecutive paragraphs and two corresponding images.
- The title slide remains text-only.

## Mandatory workflow

### 1. Prepare and document the context

Identify paragraph `<PARAGRAPH_NUMBER>` and its corresponding `image1` or `image2` description in `slides.md`.

Before generation, create `prompts/<PARAGRAPH_NUMBER>.md`. It must document:

1. The full-story context. Explicitly require the generation agent to read `short_version1.md` completely; include a concise synopsis as orientation, but treat the complete file as authoritative.
2. The exact target paragraph, copied without changes.
3. The exact reviewed scene description from `slides.md`.
4. The complete style guidelines below.
5. Every visual reference supplied to the generation agent, with its role explained.
6. The generation-only boundary: the delegated agent may create, inspect, and save the bitmap but must not edit any presentation source.

### 2. Choose visual references

Always provide this image to the generation agent:

- `public/images/paragraph-01-parts-unlimited-factory.png` — mandatory style reference for every generated image. Match its line weight, flat-color rendering, palette family, simplified geometry, daylight/shadow treatment, and level of detail.

Also provide accepted earlier images whenever the target paragraph contains a recurring character. Use the earliest clear accepted appearance of each character as an identity reference. Add other earlier images only when they materially help preserve clothing, location, or prop continuity.

Current canonical character reference:

- Bill Palmer and Steve Masters: `public/images/paragraph-02-bill-promotion.png`

Inspect all reference images before delegating generation. Clearly label each as a style reference or character-appearance reference. References are not edit targets: generate a new scene.

### 3. Delegate image generation only

Spawn an image-generation subagent and provide it:

- The complete contents and requirements of `prompts/<PARAGRAPH_NUMBER>.md`.
- The requirement to read `short_version1.md` completely.
- The mandatory paragraph 1 style-reference path.
- All applicable prior character-reference paths.
- The required output path: `public/images/paragraph-<NN>-<descriptive-slug>.png`.

The generation agent must:

1. Read the image-generation skill instructions completely.
2. Inspect every reference with `view_image`.
3. Use the built-in image-generation tool.
4. Pass paragraph 1 as an image reference on every request, plus applicable character references.
5. Generate one new bitmap for this paragraph.
6. Inspect the generated image itself.
7. Save/copy only the final bitmap into `public/images/`.
8. Make no edits to `slides.md`, Vue, CSS, package files, or other presentation sources.
9. Return the exact final generation prompt, output path, dimensions, and self-check.

### 4. Run a separate compliance review

After generation, spawn a different review-only subagent. Give it:

- `prompts/<PARAGRAPH_NUMBER>.md`
- `short_version1.md`
- The candidate image
- Paragraph 1’s mandatory style reference
- Every supplied character reference

The reviewer must inspect all images and return `ACCEPT` or `REJECT` first. It must evaluate:

1. Fidelity to the exact paragraph and reviewed scene description.
2. One concrete, coherent, physically plausible scene rather than an abstract metaphor.
3. Style continuity with paragraph 1.
4. Appearance continuity for every recurring character.
5. Originality: no recognizable copyrighted characters or proprietary designs.
6. Half-slide usability: landscape framing, clear focal action, safe crop margins.
7. Absence of unintended text, logos, branding, watermarks, photorealism, painterly rendering, or 3D rendering.

If rejected, send the reviewer’s smallest precise corrections back to the generation-only agent. Regenerate and repeat independent review until accepted. Do not integrate a rejected image.

### 5. Integrate in the primary session

Only the primary agent edits the presentation:

1. Inspect the accepted bitmap independently.
2. Add the appropriate `image1Src` or `image2Src` value to the matching `<NarrativeSlide>` in `slides.md`.
3. Preserve the existing image description in the `image1` or `image2` property as alt/title metadata.
4. Do not change the narrative paragraph or chapter comments.
5. Do not replace other placeholders.

### 6. Render and verify

After integration:

1. Render the affected slide with a headless browser.
2. Visually inspect the rendered slide.
3. Confirm the image loads at natural resolution and fills only its intended frame.
4. Confirm both narrative paragraphs remain visible without overflow.
5. Run `npm run build` and `git diff --check`.
6. Report the prompt-document path, image path, reviewer decision, rendered result, and whether changes are committed.

## Image style guidelines

- Original simple 2D adult animated-sitcom cartoon illustration.
- Use only broad qualities associated with classic prime-time workplace cartoons: bold clean black outlines, flat bright colors, simplified geometric forms, expressive faces, and slightly exaggerated but believable anatomy and perspective.
- Match `paragraph-01-parts-unlimited-factory.png` for palette family, line weight, shadow treatment, architectural design language, and detail level.
- Do not copy characters, locations, logos, signature palettes, or proprietary designs from *The Simpsons*, *Futurama*, or any other existing series.
- Use a wide landscape composition suitable for one half of a 16:9 presentation slide.
- Keep the important subject, faces, actions, and artifacts away from crop edges.
- Depict one coherent real-world scene or artifact that could physically be photographed or captured as a screenshot.
- Prefer concrete evidence: monitors, diffs, comments, messages, tickets, logs, runbooks, receipts, boards, terminals, racks, checklists, dashboards, reports, and factory equipment.
- Avoid glowing paths, streams, funnels, symbolic machinery, transformations, personified software, diagrams pretending to be scenes, generic posed meetings, and contrived multi-location collages.
- People are appropriate when naturally performing a specific plot action.
- Short readable interface or document text is allowed only when it is necessary to communicate the scene.
- No gradients, painterly rendering, photorealism, 3D rendering, visual clutter, watermark, unintended branding, or invented text.

## Values for this run

- Paragraph number: `<PARAGRAPH_NUMBER>`
- Exact paragraph: `<COPY_FROM_SLIDES_MD>`
- Reviewed image description: `<COPY_MATCHING_IMAGE_DESCRIPTION_FROM_SLIDES_MD>`
- Applicable recurring characters: `<CHARACTER_NAMES_OR_NONE>`
- Additional character-reference images: `<PATHS_OR_NONE>`
- Output filename: `public/images/paragraph-<NN>-<descriptive-slug>.png`
