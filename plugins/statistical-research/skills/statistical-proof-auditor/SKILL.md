---
name: statistical-proof-auditor
description: "Audit, repair, develop, and write rigorous statistical theory proofs in LaTeX. Use for theorem or lemma proofs, convergence and rate arguments, minimax claims, testing guarantees, initialization conditions, optimality claims, assumption checks, counterexample searches, or appendix proof revisions. The defining behavior is audit-before-proof: challenge the claim, identify hidden assumptions and edge cases, repair it with the weakest needed conditions if necessary, and only then produce a polished proof in the manuscript's notation."
---

# Statistical Proof Auditor

## Governing principle

Do not jump from an intuitive claim to a plausible-looking proof. Pressure-test the mathematical statement first. Existing notes and proofs are evidence, not authority.

## Required workflow

1. Read the method and theory sources needed to understand the model, estimator/test, parameter space, asymptotic regime, and notation.
2. Restate internally the exact target claim and list every stated assumption it uses.
3. Audit the claim before proving it:
   - test boundary cases and degenerate regimes;
   - inspect scaling and dimensions;
   - identify independence, measurability, identifiability, regularity, incoherence, boundedness, or moment assumptions that may be implicit;
   - look for simple counterexamples or incompatible asymptotic regimes;
   - compare the claimed rate with known lower-bound heuristics when optimality is asserted.
4. Build a dependency map of auxiliary lemmas. For each lemma, state exactly which assumptions it consumes and which later result it supports.
5. Verify every nontrivial implication. Do not write "standard" or "it is easy to see" when the omitted step carries the main difficulty.
6. If the claim fails, do not force a proof. Explain the failure and repair the theorem using the weakest additional condition or corrected conclusion that makes the argument valid.
7. Preserve the user's theorem statement whenever possible. If a statement must change, flag the change explicitly before giving the repaired version.
8. Produce the polished proof only after the audit succeeds.
9. Perform a final reverse audit: starting from the conclusion, trace each dependency back to a stated assumption or previously proved result.

## Proof construction rules

- Work in the manuscript's current notation and macros.
- Separate deterministic and stochastic arguments when doing so clarifies the proof.
- Name events and intermediate quantities when they recur.
- Track constants, norms, dimensions, probability levels, and asymptotic orders consistently.
- State where union bounds, concentration inequalities, covering arguments, perturbation bounds, convex duality, or optimization facts enter.
- When proving rates, show which term dominates in which regime rather than hiding everything in big-O notation too early.
- For testing, verify both type-I error control and power under the stated alternative; check whether dependence introduced by estimation invalidates the null calibration.
- For minimax optimality, distinguish the upper bound from the lower bound and ensure both use the same parameter class and loss.
- For algorithmic convergence, distinguish optimization error from statistical error and specify the initialization region and contraction conditions.

## Literature and borrowed lemmas

If a proof relies on a published lemma or known theorem, verify the source and check that its assumptions match the present setting. Do not cite a result merely because it is analogous. If adapting a theorem, explain the adaptation.

## LaTeX contract

- Return clear journal-quality LaTeX when a proof is requested.
- Preserve theorem, lemma, equation, and appendix labels where possible.
- Do not use `\begin{paragraph}`.
- Prefer concise prose and inline math for short expressions, with displays for substantive derivations.
- Keep prose paragraphs on one source line when practical; avoid arbitrary hard wraps.
- Do not silently change notation halfway through a proof.

## Final audit checklist

Before declaring the proof complete, verify:
- the conclusion exactly matches the theorem statement;
- all random objects and probability statements are well-defined;
- no assumption is used before being stated or proved;
- all rate comparisons are valid in the declared asymptotic regime;
- edge cases do not contradict the claim;
- references and equation labels resolve consistently;
- any repaired assumption is clearly disclosed.

See `references/audit-template.md` for a compact audit scaffold.
