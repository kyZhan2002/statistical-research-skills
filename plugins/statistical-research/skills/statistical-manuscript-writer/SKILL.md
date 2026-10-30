---
name: statistical-manuscript-writer
description: "Draft, revise, or polish statistical and biostatistical research papers in LaTeX. Build a coherent mathematical story, express contributions and covered regimes constructively, minimize new notation, and present the main theoretical and empirical findings with source-grounded precision. Use for manuscript sections, related work, simulation-results prose, revision letters, and full-paper restructuring; use specialized workflows for proof development or simulation-code auditing."
---

# Statistical Manuscript Writer

## Shared writing rules

Before drafting or revising, read and apply [the shared writing principles](../../references/writing-principles.md). They govern the prose in this skill, including punctuation, American spelling, direct language, notation, contribution framing, and numerical interpretation. The guidance below specializes them for a LaTeX manuscript. For revision examples, consult [references/preferences.md](references/preferences.md).

## Core objective

Write natural, precise LaTeX prose suitable for a leading statistics journal such as the Annals of Statistics. Give readers a clear, interesting mathematical story: the statistical question, the idea that advances it, the evidence supporting that advance, and why it matters. State contributions strongly and specifically, with their assumptions and scope intact. Correctness and an engaging narrative should reinforce each other.

## Source-first, story-first workflow

1. Read the relevant manuscript and supporting sources, including theorem statements, figures, tables, appendices, and available computational evidence. Recover the notation, assumptions, local LaTeX conventions, and requested scope; existing prose may be stale.
2. Before drafting, identify the central message in a sentence: what question the paper resolves, through what idea, and in which regime. Use this as a working guide, not a required slogan or extra deliverable. For a local edit, identify how the passage serves that message.
3. Connect each major claim to its supporting result or comparison. Distinguish established facts, empirical evidence, intuition, and conjecture. If sources conflict or a missing fact changes the story, ask a focused question and continue work that does not depend on the answer.
4. Arrange the argument so that each section advances the central message. Introduce the problem before its machinery, motivate the method before its technical details, and explain the significance of results as they appear. Adapt the order to the paper rather than imposing a fixed outline.
5. Revise within scope. Preserve mathematical meaning and existing notation; flag necessary changes to theorem statements or unaffected sections. Keep editorial questions outside the manuscript text unless annotations are requested.
6. Complete the quality audit below. Deliver the requested LaTeX or file edits, with a brief account of material unresolved issues and checks actually performed.

## Narrative and contribution framing

Use connected prose with purposeful paragraphs. Lead with the statistical point, develop its evidence or explanation, and connect it to the next point. A sequence of correctly stated results is not yet a story: explain why these results belong together and what readers learn from their combination. Avoid repeated roadmaps, generic transitions, decorative vocabulary, and promotional adjectives.

State the advance directly: what the method enables, what the theorem establishes, which regime is covered, or what new understanding emerges. Prefer precise verbs such as "establish", "extend", "characterize", or "resolve" when the evidence supports their commitments. Strength comes from the specificity of the contribution, not from unsupported superlatives or excessive hedging.

Frame scope affirmatively. Replace defensive formulations such as "cannot do X", "cannot be understood as X", "is not doing X", and "is limited by X" with an exact account of the target, guarantee, and conditions. Preserve all material qualifications; do not turn a conditional result into a universal claim. Necessary mathematical negation, an established impossibility result, or a direct answer to a reviewer remains appropriate when it carries substantive meaning.

In literature comparisons, explain the contribution relative to prior work along a relevant axis: problem, assumptions, regime, guarantee, statistical accuracy, or computation. State the prior result fairly and identify the supported extension or complementary advance. Compare like quantities under comparable conditions; a smaller upper bound alone does not establish that one estimator outperforms another. Verify priority claims such as "first" or "no prior work" before using them.

Use natural transitions grounded in the argument. Do not introduce results with "Three findings stand out", "One finding per setting", "One xxx per yyy", "Three XXX, one YYY" or similar counting and allocation formulas. Lead with the substantive finding itself. This preference concerns rhetorical presentation; precise design descriptions such as the number of observations per subject remain appropriate.

## Economical definitions and notation

Introduce a new symbol, abbreviation, or named definition only when it is mathematically necessary or materially simplifies repeated reasoning. Prefer existing notation or a short verbal description for a quantity used once. Avoid naming every intermediate expression, regime, or observation.

Define every new symbol at its first use, explaining why it is needed when that purpose is not immediate. Alternatively, collect the nontrivial notation in a clearly identified paragraph or subsection before it is used and direct readers there. A later notation summary does not excuse an undefined first use. When several related objects are essential, introduce them together with a compact explanation of their roles. Use a collected notation paragraph or subsection when it reduces the reader's burden; do not create a glossary by default. Move proof-only machinery to the proof or supplement when appropriate, retaining definitions needed to understand the main statements.

Preserve the manuscript's established notation. Simplify exposition by removing redundant introductions and improving explanations before proposing renaming. Keep theorem statements concise while retaining their quantifiers, conditions, probability statements, and asymptotic regime.

## Section-specific guidance

### Abstract, introduction, and related work

Open the abstract with concise, problem-specific background and an explanation of why the statistical question matters. Then describe the key idea, principal contributions, and their implications at a high level. Use mathematical notation only when essential to communicate the contribution accurately. Avoid opening with a formal model, parameter definitions, assumption lists, or technical rates. Express the scope in accessible words where possible, while matching the strength of the claims to the body of the paper.

Let the introduction develop from the background and importance of the problem to the statistical difficulty, the opportunity for an advance, and the paper's key idea. In the contribution discussion, include concise formal definitions when they make the advance clear and precise. State a convergence rate or other quantitative guarantee when it is a main contribution, and explain its significance and the meaning of its symbols. Integrate this formal detail with the conceptual explanation rather than requiring a separate informal account of every contribution. Usually leave assumptions and their detailed statements to the methods or theory section. Include only a brief scope qualification or cross-reference when needed to keep a contribution claim accurate. Group literature by ideas and explain how the present work advances that conversation. Keep the opening concise and specific rather than padding it with generic motivation.

### Methods and theory exposition

Motivate the construction and explain why its essential components address the stated difficulty. Explain what each assumption controls and what each rate or guarantee means in the relevant regime. Distinguish the role of a theorem from the details of its proof. Keep lengthy derivations in the appropriate appendix when they interrupt the main argument; preserve the bridge that explains the proof idea.

After an important theorem or other substantive result, add a clear, concise interpretation when it helps readers understand the contribution. Explain the consequence for the statistical problem, the role of the relevant regime, or the improvement established by the result. Interpret the mathematics rather than restating the theorem in words; retain its conditions and avoid repeating an explanation already given nearby.

When writing or revising proof exposition, identify the decisive argument and the steps that require real explanation before allocating space. Give the main insight, difficult transitions, and consequential uses of assumptions enough detail for readers to follow. Compress routine algebra and standard applications with precise justifications or references, while keeping every step needed to verify the argument. The length of each part should reflect its mathematical importance and difficulty, rather than treating every step equally. Flag substantive gaps for proof development or auditing instead of smoothing them over through prose.

### Simulation results

Organize the exposition around the statistical questions the experiments answer and their connection to the paper's central contribution. Select the most informative findings and representative comparisons that explain the method's strengths. Prioritize scientific relevance, effect size, and consistency across the examined settings, rather than the largest favorable number.

Lead each results paragraph with the main empirical pattern, support it with a figure or table reference and only the numerical comparisons needed to judge its importance, then explain its implication. Use a consistent comparison basis across settings: metric, comparator, direction of improvement, and regime. Give exact ranges or relative changes only when verified. Account for Monte Carlo uncertainty when it affects the interpretation of a difference.

Give captions and main text complementary roles in numerical studies. A caption should describe the figure clearly and concisely, including the settings and visual elements needed to read it. The main text should explain the principal takeaways, what the comparisons reveal about the method's strengths, and why those findings matter for the paper's contribution. Read the caption before drafting the interpretation; avoid repeating its panel descriptions, axis definitions, or setup details unless a brief reminder is necessary for the argument.

Summarize repeated patterns rather than narrating every panel or table cell. Keep essential design information in the section and place detailed configurations or secondary results in captions, tables, or the supplement as appropriate. Retain material reversals, tradeoffs, and conditions of advantage where readers can assess the main claim. Describe observed behavior as empirical evidence; connect it to theory only within the theory's scope. Never imply that simulations prove a theorem or establish universal superiority.

For detailed phrasing examples, consult [references/preferences.md](references/preferences.md). Experiment design, code auditing, and new simulation runs are separate tasks; do not silently expand a prose revision into them.

### Real-data analysis and discussion

Tie the application to the statistical question. Define the cohort, outcomes, evaluation design, and relevant quantities from source material. Present the findings that demonstrate the method's practical value and separate statistical evidence from scientific interpretation. Match causal or biological language to the design. In the discussion, synthesize what the results jointly establish, describe the supported scope constructively, and connect concrete open questions to that contribution.

### Revision letters

Answer each reviewer concern directly, explain the actual change or evidence, and identify its manuscript location. Use a respectful, substantive tone. Preserve an explicit qualification when it is needed to answer the concern accurately; do not imply resolution without a corresponding revision or justification.

## LaTeX contract

Read [Statistical LaTeX Style](../../references/latex-style.md) before editing LaTeX. Apply its three-line display limit, equation punctuation, notation conventions, citation grammar, and figure/table checks. For new manuscripts, use its bibliography and macro defaults when compatible with the venue. For existing papers, inspect the actual preamble and preserve established mathematical conventions. Interpret assumptions where useful and verify the rendered material affected by the edit.

- Return copy-paste-ready LaTeX for requested manuscript text; preserve macros, citation commands, labels, theorem environments, and the existing `\input`/`\include` structure. Follow the paper's document class and package choices.
- For a focused revision, preserve the package setup and global notation. Add dependencies or macros when creating a template or carrying out a requested style conversion, following the shared LaTeX conventions. Use the project's existing reference commands and citation keys and verify that targets exist and support the sentence.
- Prefer inline `$...$` for short expressions and display mathematics for statements that need emphasis or alignment. Punctuate equations as part of their sentences. Keep each prose paragraph on one source line when practical.
- Do not use `\begin{paragraph}` or `\paragraph{}`. Instead, use natural language to summarize and connect paragraphs. Preserve valid sectioning commands already used by the project; do not introduce unnecessary headings to fragment connected prose.
- Never invent bibliography entries, DOIs, theorem numbers, sample sizes, numerical results, assumptions, or dataset facts. Verify new literature claims against original papers or authoritative journal sources. Report unresolved source questions outside the proposed manuscript text.
- When editing a complete LaTeX project, use its existing build command if available and inspect relevant errors and unresolved references. For isolated snippets, check syntax and compatibility with supplied macros. Distinguish a successful build from a source-only check; compilation does not verify the mathematics.

## Final quality audit

Before returning the revision, check:

1. **Story:** The central contribution is clear, and the selected results advance it through a coherent argument.
2. **Notation:** Every new definition earns its place; symbols are defined at first use or in an earlier, clearly identified notation paragraph or subsection, their roles are clear, and existing conventions are preserved.
3. **Claims:** Contributions are direct and constructive, with exact assumptions and regimes; comparisons and empirical statements match the evidence.
4. **Exposition:** Important results receive useful, concise interpretation, numerical takeaways complement captions, and proof detail concentrates on the decisive and difficult steps. Apply the shared writing principles: check spelling, punctuation, sentence structure, stable terminology, and evidence in place of filler. Empirical claims retain sufficient evidence and any tradeoff that changes their interpretation.
5. **Consistency:** Relevant abstract, body, captions, and supplement agree on claims, settings, and numbers. Recompute derived numerical comparisons when inputs are available; account for rounding and different experimental settings. Search relevant sources before claiming something is absent, and inspect the rendered equation if a suspected error could come from PDF extraction.
6. **LaTeX and sources:** Labels, citations, mathematical syntax, and dependencies are sound for the supplied context. State only the checks actually completed and identify unresolved issues precisely.
