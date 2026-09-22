---
name: om-theory-model-auditor
description: Audit analytical operations-management, management-science, information-systems, marketing, and game-theoretic models for mathematical and economic correctness and proposition-level contribution integrity. Use when the user asks to verify a model, derivation, equilibrium, lemma, proposition, corollary, proof, threshold, comparative static, robustness result, numerical illustration, or manuscript claim; to find counterexamples or missing parameter regions; to perform proposition-level novelty triage against supplied closest papers; or to determine which verified results deserve headline status and whether the current main model actually carries the claimed mechanism.
---

# OM Theory Model Auditor

Audit correctness before improving exposition or publication positioning. Treat every stated result as a claim to verify, not as a conclusion to defend.

## Required inputs

Collect or reconstruct, with explicit uncertainty:

- players, sequence of moves, information sets, and observability;
- primitives, parameter domains, distributions, and maintained assumptions;
- decision variables, feasible sets, objectives, outside options, and constraints;
- equilibrium concept and tie-breaking rules;
- benchmark, main model, extensions, and the claims attached to each;
- any source equations, LaTeX, code, tables, or figures used to support the claims.

Do not block on a perfectly polished manuscript. If an input is missing, state the narrowest additional assumption required and audit conditionally. Never silently invent a primitive or repair the model.

## Audit workflow

1. Read `references/audit-checklist.md`, `references/mechanism-and-narrative-audit.md`, and `references/proposition-level-novelty-and-headline-protocol.md` for every manuscript-level audit. For Bayesian persuasion, disclosure, market testing, recommendation, or endogenous information acquisition, also read `references/information-design-audit.md`.
2. Build a model map: timing, ownership of choices, information, payoffs, constraints, and parameter domains. When policy or governance matters, add a policy-instrument-decision-rights map distinguishing mandatory versus voluntary adoption, fixed versus endogenous intensity, and the owner of every choice. For information design, add the state-prior-experiment-posterior-action chain and distinguish acquisition, experiment design, disclosure, and reporting. Flag notation that changes meaning across sections.
3. Build a claim ledger covering every lemma, proposition, corollary, comparative static, figure, table, mechanism statement, literature contrast, and managerial implication. Record whether each formal result is new, adapted, specialized, or inherited and verify its provenance. For each result, also record its predecessor or benchmark, whether it adds a mechanism or merely reverses or reparameterizes an earlier mapping, its downstream role, and the figure panels that display it. Link introduction and abstract claims to this ledger.
4. Re-solve the model independently by backward induction or the appropriate equilibrium method. For information design, derive the receiver best response, sender interim payoff, Bayes-plausible posterior problem, and concavification or equivalent experiment optimization. Do not merely retrace the manuscript's algebra.
5. Check feasibility and optimality before comparative statics: candidate regimes, first- and second-order conditions, corners, participation and incentive constraints, deviations, multiplicity, nonexistence, and tie cases.
6. Partition the parameter space into mutually exclusive and collectively exhaustive regions. Verify threshold existence, ordering, continuity at boundaries, and the direction of every inequality. For consequential assumptions, verify their mathematical role, excluded cases, nonempty admissible region, and whether the claimed extension genuinely relaxes them. Separate within-regime derivatives from jumps caused by regime switching. Audit any derived metric for economic validity, domain, ordering content, continuity, and differentiability before accepting an elasticity or global monotonicity claim.
7. Check each proof line against the exact proposition statement. Distinguish sufficient, necessary, and necessary-and-sufficient conditions.
8. Use symbolic algebra, numerical search, plots, or optimization tools when useful. Use computation to discover errors and counterexamples, not as a substitute for proof. When a manuscript hands off from analysis to numerics, verify the analytical frontier, source of intractability, coverage of every regime and boundary, global-search logic, reproducibility, and scope of the resulting claim. Invoke `operations-research-optimization` for substantial computational or solver work when available.
9. Stress-test headline results with boundary values, limiting cases, alternative admissible parameter values, and direct profitable deviations. For an alleged new mechanism, remove the focal feature or set its intensity to zero and verify that the claimed regime, reversal, or interior solution changes as stated. In information design, test no-information, full-information, uninformative-experiment, and restricted-experiment cases and verify any claimed signal-support reduction. If the paper claims to generalize or subsume a closest model, recover that model and its result under the stated restriction. Report the first valid counterexample prominently.
10. Audit mechanisms only after the formal result survives. Trace each verbal mechanism through a binding constraint, derivative, payoff difference, or equilibrium comparison. Separate the mathematical driver from the economic interpretation and from the managerial implication.
11. Audit policy and stakeholder claims. Verify instrument rankings under a common feasible comparison, test whether delegation preserves the intended equilibrium, and require an explicit objective or criterion for `optimal`, `preferred`, `dominates`, and `win-win`.
12. Audit the result chain: benchmark, enriched environments, comparative statics, policy or instrument comparison, coexistence or selection, and extensions must use compatible assumptions and equilibrium concepts. Verify that the prose explains the links between neighboring results, that paired propositions are compared on common primitives, and that a reverse parameter traversal is not marketed as an independent mechanism.
13. Use `references/report-template.md` for the final audit report.


## Proposition-level novelty, headline, and model-role gate

After the mathematical audit survives, run the proposition-level workflow in `references/proposition-level-novelty-and-headline-protocol.md`. This stage is mandatory for manuscript reconstruction and contribution assessment.

The required sequence is:

`proposition-level novelty audit -> headline-result identification -> main-model promotion/demotion recommendation -> handoff to paper restructuring`.

For each lemma, proposition, and corollary, distinguish mathematical novelty from economic novelty. A new formula, threshold, U-shape, inverted-U, interior optimum, or regime partition is not a headline contribution by itself. Compare the result with the supplied closest papers at the level of causal mechanism and decision structure.

Classify each formal result as one of:

- `HEADLINE`;
- `CORE MECHANISM`;
- `EQUILIBRIUM CONSEQUENCE`;
- `BENCHMARK`;
- `EXTENSION`;
- `ROBUSTNESS`;
- `APPENDIX`;
- `MERGE / DELETE`.

Also record a novelty-sensitive label such as `PRIOR RESULT / SAME MECHANISM`, `SPECIAL CASE OR REPARAMETERIZATION`, `COMBINATION OF KNOWN CHANNELS`, `NEW BOUNDARY / REGIME`, `NEW EQUILIBRIUM CONSEQUENCE`, `NEW MECHANISM`, `NEW DESIGN IMPLICATION`, or `NOVELTY UNRESOLVED`.

### Headline-result gate

A result may be promoted to headline only if:

1. its formal claim is `VERIFIED` or `VERIFIED WITH CONDITIONS`;
2. it is not merely a special case, reparameterization, or known mechanism in new notation;
3. the mechanism is non-obvious and substantively changes a decision, equilibrium, performance outcome, or design principle;
4. the result is generated by the model that the paper presents as central;
5. the mechanism, not merely the exact closed form, survives reasonable relaxation;
6. the result can be stated as an economic or operational insight rather than only as a formula.

Prefer two to four headline results. A larger set usually signals a hierarchy problem.

### Conditional-versus-aggregate test

Distinguish carefully between a conditional behavioral outcome and an aggregate outcome created by participation, entry, funding, or selection. For example, a decrease in `Pr(funded and delivered)` does not by itself establish a decrease in `Pr(delivered | funded)`. Do not attribute a post-decision behavioral mechanism to a model that only changes the extensive margin.

### Main-model adequacy test

For each claimed headline mechanism ask:

- Does the main model contain the primitive that generates it?
- Is the key behavioral response endogenous in the main model?
- Does the formal result operate at the same level claimed in the prose?
- Does an extension or robustness section contain the first direct representation of the mechanism?
- Is the current main model retained mainly because it gives cleaner closed forms?

Recommend promoting an extension or robustness model to the main model when it is the first model that directly represents the headline mechanism. Recommend demoting a tractable main model to benchmark, closed-form specialization, or appendix when it suppresses the mechanism or mainly reproduces prior logic.

Do not keep a model as the main model merely because it is easier to solve.

### Promotion/demotion matrix

Before handoff, produce a matrix with:

`Result | Math status | Closest prior overlap | Mechanism source | Current role | Recommended role | Reason`.

Possible recommendations include: promote extension to main model; main model to benchmark; proposition to lemma; proposition to corollary; proposition to appendix; merge; delete; or retain as headline.


## Claim verdicts

Assign exactly one status to each claim:

- `VERIFIED`: the stated conditions and conclusion are supported by a complete argument.
- `VERIFIED WITH CONDITIONS`: correct only after adding or tightening named conditions.
- `INCOMPLETE`: plausible, but a proof obligation, region, or deviation remains unresolved.
- `FALSE`: contradicted by derivation or an admissible counterexample.
- `UNVERIFIABLE`: required definitions, equations, data, or source material are absent.

Do not use confidence language as a substitute for these verdicts.

## Correction rules

- Preserve the original result beside any corrected result so the change is auditable.
- Give the smallest correction that restores validity: revised condition, restricted region, corrected sign, new corner case, or withdrawn claim.
- Recheck all downstream propositions, figures, contribution claims, and managerial implications affected by a correction.
- Label numerical evidence as illustration unless it establishes an exhaustive finite claim.
- Do not upgrade a robustness exercise into a general theorem without proving the relevant class of primitives.
- When correcting a result, revise not only its statement but also its regime name, benchmark contrast, mechanism paragraph, figure, introduction finding, and conclusion claim.

## Handoff contract

Before handing results to `om-working-paper-builder`, provide:

- the verified model map and notation;
- the claim ledger and final verdicts;
- corrected proposition statements and proofs;
- unresolved obligations and excluded parameter regions;
- a robustness map distinguishing mechanism-preserving from mechanism-changing extensions.
- a narrative-consistency map linking formal results to the abstract, introduction, figures, literature distinctions, and conclusion;
- a proposition-level novelty table, verified headline set, and main-model promotion/demotion matrix;
- a reconstruction instruction stating the one-sentence core mechanism, preferred result order, benchmark purpose, extension purpose, and claims that must not appear in the Introduction.
- when relevant, the verified policy-instrument-decision-rights map, closest-model recovery test, assumption ledger, and stakeholder outcome ledger.
- when relevant, the verified information-design contract, preference-alignment map, experiment-feasibility and informativeness audit, formal-result provenance ledger, benchmark portfolio, and analytical-versus-numerical status map.

Do not authorize a headline result for drafting while its status is `INCOMPLETE`, `FALSE`, or `UNVERIFIABLE`.
