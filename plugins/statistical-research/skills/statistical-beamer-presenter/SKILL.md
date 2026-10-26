---
name: statistical-beamer-presenter
description: "Create or revise academic Beamer presentations for statistical and biostatistical research. Use when turning a manuscript, theory note, simulation study, or research project into a coherent LaTeX slide deck for a statistics audience. Optimize for intuition, logical flow, readable density, mathematically correct notation, and clear proof ideas rather than manuscript-level detail. Produce a complete compile-ready Beamer file when requested."
---

# Statistical Beamer Presenter

## Shared writing rules adapted to slides

Before planning or writing frames, read and apply [the shared writing principles](../../references/writing-principles.md). Use their American spelling, direct language, punctuation rules, constructive contribution framing, and stable terminology in titles, bullets, captions, and speaker notes.

Build the talk around a central statistical message. Give each frame a substantive takeaway, and present contributions and supported regimes directly. Short bullets and sentence fragments are appropriate for slides. Use as many points as the argument needs, without padding to a fixed count or using announcements such as "Three findings stand out". Avoid manuscript-length interpretation paragraphs.

Define symbols on the frame where they first appear or on a preceding notation frame that the audience can follow. Reintroduce essential notation briefly after a long gap when useful. Interpret major guarantees in a short sentence. Give the decisive proof idea enough space, and put routine derivations or full verification in backup frames. For numerical figures, use titles or nearby text for the main finding and demonstrated strength, while captions supply reading details. Retain conditions and tradeoffs that affect the claim. Apply the shared final prose pass with the deck audit.

## Core objective

Teach the statistical idea to an audience. Slides are not compressed manuscript pages. Preserve technical correctness while reducing notation and cognitive load.

## Workflow

1. Read the relevant manuscript or notes and identify the central problem, method, guarantees, empirical evidence, and practical takeaway.
2. Determine the talk length and audience. For an approximately 60-minute research talk, use roughly 30--35 main slides unless the user specifies otherwise; allocate backup slides separately.
3. Build the narrative before writing frames. A strong default is:
   motivation and concrete examples -> statistical formulation -> opportunity for an advance relative to existing work -> method intuition -> formal estimator/test -> main theory -> proof ideas -> simulations or implementation -> practical interpretation -> takeaways.
4. Make every frame serve one main purpose. Remove material that does not advance the narrative.
5. Introduce notation only when first needed and reuse it consistently.
6. Present theorem statements in audience-readable form: assumptions, guarantee/rate, and one-sentence interpretation. Put technical variants and full proofs in backup slides.
7. Present proof ideas as a sequence of conceptual steps or lemmas, not line-by-line algebra.
8. For testing procedures, make the final statistic, calibration, rejection rule, and guarantee visually explicit before discussing extensions.
9. For examples, ensure the application actually exhibits the modeled structure; do not use a generic biomedical example that does not motivate low rank, smoothness, sparsity, robustness, or whatever structure the method assumes.
10. End with a compact summary of what is new, when it works, and what the audience should remember.

## Slide-density rules

- Prefer one main idea per frame.
- Use short bullets or sentence fragments, not manuscript paragraphs.
- Avoid putting multiple dense theorem blocks, algorithms, and figures on the same slide.
- Keep equations to the minimum needed for comprehension; highlight the object that changes from one step to the next.
- Use progressive structure such as "problem -> obstacle -> solution" rather than dumping notation.
- Provide intuition before technical detail whenever possible.
- Keep fonts and mathematical symbols comfortably readable at presentation distance.

## Background and motivation

Make the opening inclusive to statisticians who do not know the application. Explain what the observed data dimensions represent, why the structural assumptions are plausible, and what inferential task matters. Use examples such as EHR, public health, imaging, or multi-source data only when they map precisely to the model dimensions and structural assumptions.

## Theory slides

State the strongest useful theorem, not every technical lemma. Explain what the rate depends on, the asymptotic regime, and what is optimal or adaptive only when justified. For extensions such as heteroskedasticity, summarize what changes in the procedure and guarantee rather than reproducing a second full derivation.

## Beamer/LaTeX contract

- Produce complete, compile-ready Beamer LaTeX when requested.
- Preserve project macros and notation where available.
- Use a professional statistics-talk style with restrained visual complexity.
- Keep frame titles informative and specific.
- Avoid `\begin{paragraph}` and avoid manuscript-length text blocks.
- Verify braces, environments, labels, citations, and bibliography commands.
- Do not fabricate citations, examples, or numerical results.

See `references/deck-checklist.md` for the compact presentation audit.
