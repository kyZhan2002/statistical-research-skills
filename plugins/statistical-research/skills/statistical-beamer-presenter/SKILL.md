---
name: statistical-beamer-presenter
description: "Create or revise academic Beamer presentations in LaTeX for statistical and biostatistical research. Turn manuscripts, theory notes, or simulation studies into coherent talks with readable mathematics, clear proof ideas, and concise interpretation. Deliver compile-ready Beamer source when requested. Use the PowerPoint presenter for editable PPTX decks."
---

# Statistical Beamer Presenter

## Required References

Before planning or writing, read [shared writing principles](../../references/writing-principles.md) and [academic presentation principles](../../references/presentation-principles.md). Read [Statistical LaTeX Style](../../references/latex-style.md) for the notation, equation, citation, and graphics conventions. Apply these rules to frames and presenter notes, adapted to a talk rather than manuscript paragraphs.

## Workflow

1. Read the source manuscript or notes and any existing deck. Identify the central message, audience, duration, and required coverage. Preserve a supplied template and project macros where compatible with the requested changes.
2. Outline the statistical story before writing frames. Give each frame one purpose, motivate essential notation, and connect the main guarantee and evidence to the contribution. Separate main-talk material from backup derivations.
3. Establish a consistent theme and readable fonts. For new decks, include `\usefonttheme{professionalfonts}` so Beamer respects the selected mathematical fonts. This command does not install or select a font. Choose compatible text and math fonts for the actual compilation engine and verify the output. When revising a deck, preserve compatible choices and resolve conflicts rather than stacking font packages.
4. Write concise frames using the shared presentation rules. Do not use `\footnote`, `\tiny`, `\scriptsize`, `\footnotesize`, frame shrinking, or an equivalent small-text workaround for explanations. Move necessary text into the body or a readable caption, split dense frames, and leave optional narration to notes or the presenter. Apply the same rule to explanatory strips at the top. Preserve essential qualifications and readable attribution.
5. Compile with the project's engine and bibliography tool when available. Inspect every rendered frame, including backup frames and intended overlay states. Fix clipping, missing symbols, small legends, and overflow. Check the log for unresolved citations and references.
6. Deliver the requested `.tex` and supporting sources or assets needed to reuse it, plus a compiled PDF when requested. Identify missing dependencies or compilation/rendering checks that could not be completed.

## Beamer Content and Layout

Use informative titles and restrained visual complexity. Short bullets or sentence fragments are appropriate. Explain assumptions and important rates in readable words beside the essential mathematics. Give the decisive proof idea enough space and put routine algebra in backup frames.

Keep displayed derivations to at most three lines and often fewer for comfortable reading. Use `align` or `align*` for multiline mathematics, preserve labels and macros, and avoid `\begin{paragraph}`. Use Title Case for new frame titles unless the venue or deck specifies otherwise. Full sentences follow normal punctuation even when they end in a formula.

Use vector PDF plots where possible and size their labels for the final slide. Keep explanatory captions in readable type rather than shrinking them below the figure. Avoid densely packed theorem blocks, algorithms, or multi-panel figures. A professional font theme is not a substitute for inspecting readability.

## Final Check

Apply the shared deck review and [Beamer deck checklist](references/deck-checklist.md). Check both the rendered appearance and whether the source compiles with the supplied dependencies. Do not describe an uncompiled deck as verified or invent results, citations, examples, or assumptions to fill a frame.
