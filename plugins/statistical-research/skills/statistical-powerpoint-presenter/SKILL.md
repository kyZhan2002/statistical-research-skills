---
name: statistical-powerpoint-presenter
description: "Create or revise editable PowerPoint (.pptx) presentations for statistical and biostatistical research. Turn manuscripts, theory notes, or simulation studies into clean academic talks with readable mathematics, clear proof ideas, and native slide objects that support manual editing and reuse. Use for PowerPoint or PPTX research decks, not Beamer source or manuscript prose."
---

# Statistical PowerPoint Presenter

## Required References and Output

Before planning or writing, read [shared writing principles](../../references/writing-principles.md) and [academic presentation principles](../../references/presentation-principles.md). Use the same statistical story and academic voice as the Beamer presenter, adapted to native PowerPoint objects. Deliver an editable `.pptx` file unless the user explicitly requests another destination. A rendered PDF or a collection of slide images is not a substitute.

Use the available presentation authoring tools and their format-specific documentation. Keep this workflow portable across Codex and Claude Code: it requires no particular connector, library, or service. If a preferred tool is unavailable, use a supported local PowerPoint workflow. Do not claim to have created or inspected a file when tools only support an outline.

## Workflow

1. Read the source material and any reference deck. Identify the central message, audience, duration, required coverage, and whether the reference supplies content, visual style, or both. For edits, inspect slide masters, layouts, notes, fonts, charts, and equations before changing them.
2. Outline the narrative using the shared presentation rules. Give each slide one purpose and plan main slides separately from backup material. Explain the statistical idea before its machinery, and connect guarantees and experiments to the contribution.
3. Establish a reusable design using the supplied template or a restrained academic default. Use a consistent theme, layouts, margins, font hierarchy, and palette. Default to 16:9 for a new deck unless another size is required. Use commonly available fonts with the needed mathematical glyphs, and verify substitutions on rendering.
4. Build slides with native editable content following the contract below. Keep explanations in the main text or a readable caption. Put optional narration in speaker notes or leave it to the presenter. Never add tiny explanatory footnotes or top-of-slide text strips.
5. Save the PPTX, render every slide, and inspect it at presentation scale. Check content, overlap, clipping, figure labels, math glyphs, and line breaks. Inspect the saved file's object structure or reopen it in an editor to verify editability, then fix defects and rerender affected slides.
6. Deliver the PPTX with any requested preview. Retain source data, assets, and generation source when needed to regenerate non-native content. Provide reusable source files when requested and disclose any rasterized equations, noneditable charts, unavailable fonts, or incomplete validation that affects manual reuse.

## Editable PowerPoint Contract

- Use native text boxes, shapes, connectors, and tables. Keep text as text, not outlines or screenshots. Group related elements logically while allowing users to ungroup and edit them. Use theme fonts and colors, slide masters, and reusable layouts when the authoring tool supports them. Avoid dozens of fragmented boxes for a single paragraph or formula.
- Use editable charts with embedded data when the available tool faithfully represents the statistical graphic. Preserve source data and plotting code for specialized plots that require external rendering. Use vector graphics in a format PowerPoint and the target tool support, such as SVG, or adequate-resolution raster images when needed. Do not insert PDFs as a universal PowerPoint image format or flatten whole slides into images.
- Prefer native PowerPoint equations when supported, preserving editable mathematical structure. Use Unicode and proper subscript/superscript formatting for simple expressions. If a complex equation requires vector or raster rendering, retain its editable mathematical source and disclose the limitation. Do not represent a rendered equation image as editable math. Never leave raw LaTeX commands in visible text.
- Preserve mathematical notation and define symbols at first use. Split dense derivations into meaningful steps with at most three lines per displayed block. Use readable upright operators and intentional delimiter sizes without importing LaTeX package commands. Native equation formatting replaces Beamer macros, `align` environments, and font-theme directives.
- Use readable author–year citations in context and reference slides or speaker notes for full entries. Use native slide references or descriptive pointers when useful. Resolve source manuscript references into the actual content or corresponding deck location rather than displaying `\ref`, `\eqref`, `\citet`, or `\citep` commands. Verify citations and preserve attribution.
- Keep evidence self-contained in the delivered deck. Embed graphics and chart data rather than relying on links to local files that will break on another device. Keep images proportionate and preserve sufficient resolution. Notes may hold optional narration and provenance, but material theorem conditions and qualifications remain visible.

## Readability and Academic Style

Use the shared direct prose rules in titles, bullets, captions, and notes. Aim for roughly 28–36 pt titles and 22–28 pt body text on a new 16:9 deck, adjusting to the template and rendered appearance. Treat smaller labels and captions as a reason to simplify or split the display, not an opportunity to pack in detail. Do not solve overflow with automatic font shrinking. Essential text must be comfortably readable at presentation distance.

Use clean alignment, ample space, high contrast, and limited emphasis. Avoid decorative panels, gradients, icons, and animation that do not explain the statistical argument. Use native tables with restrained rules. Keep figure explanations concise, giving the main takeaway without duplicating captions. Make the deck easy to revise by keeping related slides on consistent layouts and using stable terminology.

## Final Check

Apply the shared deck review. Confirm the PPTX opens without a repair warning when an editor is available, the intended text and objects remain editable, and no assets are missing. Rendered appearance alone does not establish editability. Confirm equations and chart labels remain legible, notes contain no drafting residue, and main slides retain all qualifications needed for the claims. Report precisely which structural and visual checks were performed.
