# Proof audit scaffold

Use this scaffold internally or expose it when the user asks for an audit report.

1. Target claim: exact conclusion and probability/asymptotic statement.
2. Stated assumptions: model, parameter class, noise, dependence, dimensions, tuning.
3. Hidden-risk scan: identifiability, dependence, boundary cases, scaling, constants.
4. Counterexample attempts: simplest regimes first.
5. Lemma dependency graph: each lemma -> assumptions -> downstream use.
6. Rate sanity check: compare dominant terms and plausible lower-bound scale.
7. Verdict: valid as stated / valid with repair / false in stated generality.
8. Only then: polished proof.
