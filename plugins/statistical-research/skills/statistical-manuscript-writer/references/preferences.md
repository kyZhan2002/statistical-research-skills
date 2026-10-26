# Phrasing examples for difficult revisions

Consult these examples when revising defensive contribution statements, dense notation, or mechanical simulation summaries. They illustrate editorial decisions, not fixed sentence templates. All scenarios below are hypothetical; use a formulation only when the manuscript's evidence supports it.

## State the supported advance

Defensive: "Our method cannot handle arbitrary dependence and is limited by a sparsity condition."

Constructive: "The method provides valid inference under weak dependence when the sparsity condition in Assumption~\ref{ass:sparsity} holds."

The revision foregrounds the guarantee and retains its conditions. It is appropriate only if those conditions support valid inference. If the original sentence reports a demonstrated failure relevant to the claim, preserve that finding explicitly in the discussion of scope.

Defensive comparison: "Unlike the existing method, we are not achieving a global guarantee."

Contribution-centered comparison: "Theorem~\ref{thm:local} characterizes convergence from the stated initialization region, complementing the global analysis of \citet{existing} with an explicit rate in the high-dimensional regime."

Use this comparison only if the initialization result, rate, and characterization of prior work are verified. A change in regime can be a contribution; it need not be portrayed as dominance on every axis. The illustrative labels and citation keys must be replaced with existing, verified project identifiers.

## Make notation serve the argument

Unnecessary machinery: "Define the estimation-quality index $Q_n := \mathbb{E}\|\widehat\theta-\theta\|^2$. We compare $Q_n$ across methods."

When used once, write: "We compare the mean squared error $\mathbb{E}\|\widehat\theta-\theta\|^2$ across methods."

Retain a named quantity when it supports repeated derivations or clarifies an essential concept. For several necessary definitions, explain their relationship in a sentence before presenting them instead of adding a separate name for each explanatory observation.

## Give simulation paragraphs a statistical point

Mechanical: "Three findings stand out. First, the method has lower error. Second, coverage is close to nominal. Third, computation is fast."

For hypothetical results supporting the accuracy and coverage claims, write:

```latex
The proposed estimator reduces mean squared error in the sparse settings while maintaining coverage close to the nominal level (Figure~\ref{fig:accuracy}). The reduction is most pronounced at smaller sample sizes and narrows as the sample size increases. This pattern supports the value of the regularization step when information is scarce.
```

Supply the most informative verified numerical comparison if needed to assess the size of the improvement. Discuss runtime where it supports a substantive computational claim. If dense settings reverse the ranking, state that pattern and narrow the conclusion to the supported regime.

Avoid "One comparison per setting" or other allocation slogans as results narration. Explain what the comparison reveals. Keep genuine design facts, such as repeated measurements per subject, precise.

## Replace emphasis with evidence

Before: "Additionally, an enduring testament to the method's value is its ability to delve into intricate dependencies, showcasing a seamless integration that underscores its pivotal role."

After, if the comparison is verified: "The method also captures higher-order dependencies, which the baselines miss (Table~\ref{tab:dependencies})."

Before: "It is worth noting that, importantly, the gain holds across scenarios."

After, if all three scenarios support the claim: "The gain holds across all three scenarios (Table~\ref{tab:scenarios})."

The revised claims require evidence. Stylistic editing alone does not establish a baseline failure, a scenario count, or consistency across settings. Replace illustrative labels with the project's actual labels.

## Split stacked clauses and integrate modifiers

Before: "The estimator reduces error in sparse settings, which are common in the application, while retaining nominal coverage, with the largest gains occurring at small sample sizes, which supports its use when information is scarce."

After, when supported: "The estimator reduces error in sparse settings while retaining nominal coverage. The gains are largest at small sample sizes, supporting its use when information is scarce."

Retain the application-specific qualification separately if it matters to the argument and has supporting evidence. Splitting a sentence should clarify which evidence supports each claim.

Before: "This approach, while effective in many settings, may struggle with highly heterogeneous data."

Direct syntax with the same qualification: "Although this approach is effective in many settings, it may struggle with highly heterogeneous data."

When the manuscript identifies the relevant conditions, replace vague phrases such as "many settings" with those conditions. Preserve a material qualification while giving the supported contribution its proper emphasis.

## External examples considered

The author's requirements govern this skill. Two external skills informed selective checks, expressed here in the manuscript writer's own workflow:

- [stat-paper-styling-skill](https://github.com/jiapivialiu/stat-paper-styling-skill): preserve LaTeX structure and distinguish language, notation, and logical consistency. Its fixed house style, mandatory logs, and layered execution protocol are not required here.
- [statistical-paper-qc](https://github.com/BIG-S2/statistical-paper-qc/blob/main/skills/jasa-acs-qc/SKILL.md): verify main/supplement agreement, check numerical comparisons in their experimental context, and verify apparent omissions or PDF extraction errors before reporting them. Its full proof-audit workflow, journal-specific page allocations, and Word reports are outside this writing skill's scope.
