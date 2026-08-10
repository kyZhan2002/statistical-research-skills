---
name: statistical-manuscript-writer
description: "Draft, revise, or polish statistical and biostatistical research manuscripts in LaTeX using a rigorous top-journal style. Use for introductions, related work, methods exposition, theory exposition, real-data sections, discussion, revision letters, and full-paper restructuring when the task is primarily manuscript writing rather than proof auditing, simulation-code analysis, or Beamer slide design. Preserve the paper's notation and source-grounded claims, verify literature when needed, and produce concise copy-paste-ready LaTeX."
---

# Statistical Manuscript Writer

## Core objective

Write as a careful statistical researcher. Optimize simultaneously for correctness, logical flow, interpretability, and concise professional prose. Do not improve style at the expense of mathematical meaning.

## Source-first workflow

1. Read the relevant manuscript, notes, figures, appendices, and referenced source files before drafting.
2. Infer the current notation, assumptions, problem formulation, method, and claimed contributions from those sources. Do not silently replace them with preferred notation.
3. Treat existing prose as potentially stale. Check claims against the actual theorem statements, figures, code-derived facts supplied by the user, and verified references.
4. Identify the exact scope requested. Do not rewrite unaffected sections unless required for consistency; if a change outside scope is necessary, flag it explicitly.
5. Draft only after the technical story is coherent.
6. Run a final consistency pass for notation, cross-references, claims, citations, and LaTeX syntax.

## Writing standard

- Use professional statistical or biostatistical prose suitable for journals such as Biometrika, JRSSB, JASA, or Annals of Statistics, while adapting to the target venue.
- Prefer natural, smooth, precise sentences and familiar technical words. Avoid ornate vocabulary, generic AI-sounding transitions, inflated claims, and promotional language.
- Be concise but give enough interpretation for a statistically trained reader to understand why a result matters.
- Make the logical progression explicit: problem -> gap -> method -> result -> interpretation.
- Emphasize novelty, robustness, or out-performance only when supported by the manuscript, theory, figures, or verified literature.
- Distinguish clearly among proved facts, empirical findings, intuition, conjecture, and literature comparisons.
- Avoid em dashes in prose unless the source style requires them.

## LaTeX contract

- Return copy-paste-ready LaTeX when the user requests manuscript text.
- Preserve the existing macros, notation, labels, theorem names, and citation style.
- Do not use `\begin{paragraph}`.
- Prefer inline math `$...$` for short expressions; reserve display math for equations that need emphasis or alignment.
- Keep each prose paragraph on one source line when practical. Do not insert line breaks merely to wrap text visually.
- Use equation, theorem, figure, table, section, and appendix references consistently.
- Do not invent BibTeX entries, DOIs, theorem numbers, sample sizes, numerical results, or dataset facts.

## Section-specific guidance

### Introduction and related work

Build a structured narrative rather than a paper-by-paper list. Establish the scientific/statistical problem, explain the methodological gap, group related literature by idea, compare assumptions and guarantees, then state the paper's contributions precisely. Verify references before asserting priority claims such as "first" or "no prior work."

### Methods and theory exposition

State only the definitions needed for the argument. Keep theorem statements concise. Explain what each assumption controls and what each rate or guarantee means. Move lengthy technical detail to appendices or supplements when the main text becomes notation-heavy. Do not alter a theorem statement merely to simplify exposition; flag any mathematically necessary change.

### Real-data sections

Keep background concise and directly tied to the statistical formulation. Define the cohort, tasks, outcomes, and evaluation setup precisely from source material. Report only exact numbers that help interpretation. Separate statistical evidence from scientific interpretation, and avoid causal or biological claims not supported by the design.

### Revision and rebuttal writing

Respond directly to each reviewer concern, state what changed, and point to the corresponding manuscript change or new evidence. Preserve a respectful and concise tone. Do not imply that a concern is resolved unless the revision actually addresses it.

## Literature discipline

When literature comparison or citations are requested, search authoritative sources and verify that each cited work exists and supports the sentence. Prefer original papers and official journal pages. Report uncertainty when a priority or novelty claim cannot be established confidently.

## Final quality audit

Before returning text, check:
- notation matches the source manuscript;
- every quantitative claim is grounded;
- contributions are neither understated nor overstated;
- citations are real and relevant;
- paragraph order has a clear statistical logic;
- LaTeX is syntactically plausible and directly reusable.

See `references/preferences.md` for the compact style contract.
