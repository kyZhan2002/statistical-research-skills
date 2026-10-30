# Statistical LaTeX Style

Read this reference when drafting or revising LaTeX with any statistical research skill. Apply the relevant sections to the requested work. These are the author's house conventions, not a claim that every convention is required by AMS.

## Applying the Conventions

Follow explicit task instructions and the target journal's requirements. For an existing project, inspect its preamble, macros, bibliography setup, and theorem environments before editing. Preserve established mathematical meaning and notation. Apply these defaults to new material where compatible, and flag any conflict that would require a document-wide notation or package migration. For a new manuscript or a requested style conversion, use the defaults below. A focused prose edit does not require rebuilding the template.

Use the [AMS Journal Style Guide](https://www.ams.org/publications/authors/AMS-StyleGuide-online.pdf) for unresolved mathematical typesetting questions, subject to explicit author and venue requirements. Consult the relevant passage before claiming that AMS requires a convention. Keep reusable instructions free of manuscript-specific theorem statements, numerical results, filenames, and custom macro assumptions.

## Mathematical Sentences and Notation

Introduce a sentence with words rather than a formula, for example, "The estimator $\widehat\theta$ satisfies ...". Treat inline and displayed mathematics as parts of grammatical sentences. Add a period when a sentence ends with a display, and use a comma only when the sentence continues. A line break in an aligned derivation does not itself end a sentence.

Define notation before use and briefly remind readers of nontrivial definitions after a long gap or at a consequential reuse. Avoid repeating every definition. Keep short expressions inline, using $y/x$ instead of an inline stacked fraction and $n^{1/2}$ instead of $n^{\frac12}$. Display important or lengthy expressions.

For new notation, use italic scalars, bold italic vectors, and bold uppercase matrices. Use uppercase Latin letters for random scalars and random vectors, and lowercase Latin letters for deterministic scalars and vectors. Preserve conventional Greek parameter symbols and their meaning rather than forcing them into a case distinction. These conventions distinguish mathematical roles without renaming established project symbols.

Use existing project macros for probability, expectation, real numbers, variance, covariance, and differentials. In a new template, provide and consistently use `\PP`, `\EE`, `\RR`, `\Var`, `\Cov`, and `\dd` with documented definitions. Write probability as `\PP(\cdot)`, expectation as `\EE[\cdot]`, and a differential as `\dd x`, with spacing such as `\int f(x)\,\dd x`. Check that each macro exists before using it in delivered LaTeX. Inspect the actual preamble location rather than assuming a particular path.

Prefer `\ell` to the visually ambiguous index `l` for newly introduced notation. Use `\ldots` in lists, as in `$x_1,\ldots,x_n$`, and `\cdots` between binary operators, as in `$x_1+\cdots+x_n$`. Write discrete index ranges as `$i=1,\ldots,n$` and continuous ranges as `$0\leq x\leq1$`.

Avoid stacked accents, underbars, accents spanning products or sums, and scripts nested to third or higher order. Align paired subscripts and superscripts on the same base. Simplify notation only while preserving its meaning: `\widehat{ab}` need not equal `\widehat a\widehat b`. If a composite estimate needs an accent, define an economical symbol for the estimated object rather than silently changing the estimator. Use an upright operator for variance rather than putting an accent over the word `Var`.

## Displays, Delimiters, and References

Keep each displayed equation or derivation block to at most three rendered lines. Break longer arguments into logically meaningful displays separated by short explanations. Introduce auxiliary terms only when they clarify the decomposition, and define them immediately. Preserve every equality, inequality, condition, and justification. Do not meet the limit by shrinking the font or crowding a line beyond the text width.

Use `align` or `align*` for multiline derivations, never `eqnarray`. Align at relational operators such as `=` or `\leq`, and break long expressions at meaningful additive or logical boundaries. Single-line displays may use `equation`, `equation*`, or `\[...\]`. Madsen's [Avoid eqnarray!](https://tug.org/pracjourn/2006-4/madsen/madsen.pdf) explains the spacing and numbering problems that motivate this choice.

Prefer manually sized paired delimiters such as `\bigl`/`\bigr`, `\Bigl`/`\Bigr`, `\biggl`/`\biggr`, or `\Biggl`/`\Biggr` over `\left`/`\right`. Use ordinary size when sufficient. For purely grouping enclosures, nest parentheses, then brackets, then braces: `\{[(\cdot)]\}`. Preserve delimiters with mathematical meaning, including norms, absolute values, sets, conditioning bars, and expectation brackets. Delimiter size and shape must clarify the expression rather than change it.

Use upright roman type for newly defined operators. For example, `\mathop{\mathrm{Risk}}` gives `\mathrm` lettering with operator spacing. Preserve existing `\DeclareMathOperator` or `\operatorname` definitions when they already provide correct upright operators. Use `\mathtt{...}` for specially named mathematical objects or algorithms when this distinguishes a formal identifier, and `\texttt{...}` for code identifiers in prose.

Number only equations that are referenced. Use unnumbered environments or `\notag` for other lines. Before removing a label, search the main manuscript and supplement for references to it. Use `\eqref{...}` for equation citations and nonbreaking spaces in `Theorem~\ref{...}`, `Figure~\ref{...}`, and similar references. Preserve equivalent project reference macros. Place figure and table labels after their captions. Use `refcheck` as a temporary draft check when available and compatible, then remove or disable its diagnostic markings for delivery. Never report a check that was not run.

## Theorems and Algorithms

Use the project's definition, assumption, remark, proposition, lemma, theorem, proof, example, and corollary environments consistently. Add informative optional titles where useful. Follow substantive assumptions with a concise explanation of what they control and why they are plausible. Explain important guarantees without repeating their statements. Retain all conditions needed for correctness even when compressing exposition.

Use explicit appendix references when deferring proofs and descriptive proof headings when presenting them. Avoid empty proof environments that merely repeat a pointer. Algorithms should state inputs, initialization, updates, stopping conditions, and outputs clearly, using the project's existing algorithm package. Verify that symbols agree with the method and theorem. Treat illustrative equations and algorithms as layout examples, not as mathematical claims to copy into a new paper.

## Citations and Bibliography

For a new journal or arXiv manuscript without a prescribed template, use `natbib` and `\bibliographystyle{ims}` when the style file is available. Preserve a venue-mandated bibliography system or an established project setup unless a conversion is requested. Check package and style compatibility before changing the preamble.

Use `\citet{key}` when author names are part of the sentence, as in `\citet{key} establish consistency`. Use `\citep{key}` when the citation supports a grammatically complete statement, as in `The estimator is consistent \citep{key}`. The removable-citation test helps distinguish the two, but sentence grammar and intended attribution determine the choice. Match the verb to the cited author group.

Prefer bibliographic metadata from the original journal or publisher page over unverified Google Scholar exports. Verify authors, title, year, venue, volume, pages or article number, and DOI when relevant. Protect case-sensitive title terms with braces, such as `{LASSO}`, and mathematical content with proper LaTeX, such as `$\ell_1$`. Preserve capitalization in proper names and acronyms without bracing entire titles unnecessarily. Maintain one authoritative project bibliography and reuse verified entries and keys. Do not fabricate missing fields.

## Figures, Tables, and Reproducible Graphics

Export manuscript and slide figures as PDF. Generate vector PDF directly for plots and diagrams so text and lines remain sharp. If the source is inherently raster, retain adequate resolution and embed it in PDF when required. Converting a low-resolution PNG or JPEG to PDF does not restore detail. Preserve source assets and follow venue requirements.

Use `tabular` when it helps align a grid of subfigures, with consistent panel dimensions, labels, and spacing. Use compatible subcaption support when needed. Prefer clear layout to large negative spacing adjustments or clipped content. Tables should use restrained horizontal rules and avoid vertical rules, particularly outer borders. Keep headers, units, precision, and alignment consistent.

Captions must identify every line, symbol, color, and panel needed to read the display, including the meaning of error bars. Verify the caption against the actual figure or table. Keep main-text interpretation focused on the takeaway and contribution rather than repeating this visual description.

Save simulation results independently of plotting. In an R workflow, save the required result objects as `.RData` and maintain one plotting entrypoint that regenerates the figures from those objects without rerunning simulations. Preserve a project's established reproducible format, such as `.rds`, when revising it. In other languages, use the corresponding native serialized output and plotting script rather than requiring R. Save enough configuration and metadata to reproduce the displayed comparisons.

## Final Typesetting Pass

Check macro definitions, first uses and reminders, equation punctuation and line counts, delimiter semantics, labels, and citation grammar. Compile with the project's existing toolchain when available and inspect changed displays, figures, tables, and references in the output. On slides, keep derivations shorter when needed for readability, place technical detail in backup frames, and use consistent punctuation for fragments. Full sentences still require normal punctuation. Record unavailable dependencies or checks rather than claiming a verified build.
