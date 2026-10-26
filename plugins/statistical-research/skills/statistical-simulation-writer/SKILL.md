---
name: statistical-simulation-writer
description: "Design, audit, revise, and write simulation studies for statistical research papers, especially when manuscript text must be reconciled with source code, generated data, figures, reviewer comments, or theory. Use for simulation plans, sensitivity studies, parameter sweeps, reviewer-driven additions, figure interpretation, reproducible experiment organization, and LaTeX simulation sections. Treat executable code and recorded outputs as the ground truth for what was actually simulated, and connect each experiment to a specific theoretical or methodological question."
---

# Statistical Simulation Writer

## Shared writing rules and empirical exposition

Before designing, interpreting, or writing a study, read and apply [the shared writing principles](../../references/writing-principles.md). Apply their direct American English style, punctuation rules, stable terminology, and notation discipline to plans, reports, captions, and LaTeX sections. Preserve programming syntax and identifiers in code.

Build the results narrative around the statistical question and the method's demonstrated strengths. Select informative comparisons with consistent metrics and comparators instead of narrating every panel or favoring only the largest gain. State material reversals, uncertainty, and conditions of advantage. Separate observed patterns from proposed explanations when the mechanism has not been established.

Read each caption before writing its interpretation. Keep visual and setup descriptions in the caption, and use the main text for the takeaway and its significance. Define new metrics and symbols before use. Present results in natural paragraphs without counting slogans or padded lists. Experiment-design tables and reproducibility checklists remain appropriate. Apply the shared final prose pass alongside the experiment audit.

## Core objective

Build simulation evidence that answers a statistical question rather than merely producing favorable plots. The simulation story must be reproducible, comparable across settings, and aligned with the theory.

## Source-of-truth hierarchy

When sources conflict, use this order unless the user specifies otherwise:
1. executable simulation and data-generation code;
2. saved configuration files, job scripts, and raw result objects;
3. figure-generation code and plotted data;
4. manuscript captions and prose.

Treat manuscript descriptions as potentially stale. Never infer a parameter value, replication count, metric, or preprocessing step from a plot when the code or data can establish it.

## Workflow

1. Read the target manuscript section and identify the scientific/statistical claims the simulations are meant to support.
2. Inspect the data-generating process, estimators, tuning rules, metrics, baselines, seeds/replicates, and figure code.
3. Reconstruct a concise experiment table internally: factor varied, values, quantities held fixed, target mechanism, metric, expected qualitative behavior.
4. Check comparability. If changing a parameter also changes signal scale or another difficulty dimension, normalize or explain why cross-setting comparisons are not meaningful.
5. Link each experiment to one purpose: finite-sample accuracy, rate behavior, robustness, sensitivity, ablation, tuning, computational cost, or reviewer concern.
6. For new designs, vary parameters that isolate mechanisms predicted by the theory rather than arbitrary grids.
7. Quantify Monte Carlo uncertainty with standard errors, error bars, confidence intervals, or distribution summaries when repeated runs are available.
8. Interpret the results mechanistically when supported. Explain the relationship to theory, and distinguish a plausible explanation from an experimentally isolated mechanism.
9. Write the manuscript section from the verified setup and outputs.
10. Preserve original simulations when the task is a revision unless replacing them is necessary; prefer clearly organized supplements or extensions and retain archived originals.

## Reviewer-driven simulation revisions

Prioritize changes that directly answer a reviewer concern. Reuse existing code and data when valid. Avoid broad expansions that add computation but little inferential value. If a sensitivity parameter is only a budget or constraint, explicitly check whether the optimizer is interior; flat performance beyond that point can be expected and is not evidence that the parameter is irrelevant.

When a theory bound contains a dimension-dependent estimation term, design diagnostics that isolate that term rather than reporting only total prediction/estimation error. When heterogeneity is the mechanism, vary interpretable geometry or direction patterns, not just a global scale that confounds difficulty.

## Statistical reporting standard

- State the data-generating model and parameter choices precisely but compactly.
- Define performance metrics before interpreting them.
- Report how tuning parameters are selected.
- Give replication count and uncertainty summaries when available.
- Compare methods fairly under identical data and tuning budgets where possible.
- Emphasize superiority only when the results actually support it across the relevant settings.
- Discuss failures or regime changes if they reveal the method's scope.

## Computational organization

For codebase work, keep simulation scripts, configurations, outputs, and figures separable. Use deterministic seeds and configuration-driven runs when possible. On clusters, choose resources based on actual memory/CPU needs, avoid duplicate jobs, and record job settings needed for reproducibility.

## LaTeX contract

When writing the paper section, produce copy-paste-ready LaTeX in the manuscript's notation. Do not use `\begin{paragraph}`. Prefer concise prose, inline math for short quantities, and one prose paragraph per source line when practical. Figure references and descriptions must match the actual panels.

See `references/simulation-checklist.md` for the compact experiment audit.
