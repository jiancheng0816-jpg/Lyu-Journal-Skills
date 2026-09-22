---
name: om-theory-model-auditor
description: Audit analytical OM and quantitative-management theory models before writing or journal calibration. Verify model logic, equilibrium, derivations, propositions, comparative statics, boundary cases, and proofs; perform proposition-level novelty-sensitive result triage against supplied closest papers; identify which results can support headline claims; and determine whether the current main model actually carries the paper's core mechanism. Use before om-working-paper-builder. Do not trade mathematical truth for narrative strength.
---

# OM Theory Model Auditor

## Purpose

This skill is the correctness, proposition-level audit, and model-role triage layer for analytical OM and quantitative-management papers.

It answers four questions in sequence:

1. Is the model correct?
2. Which formal results are genuinely distinct from the closest prior results?
3. Which verified results deserve headline status?
4. Does the current main model directly generate the intended headline mechanism, or is the real mechanism buried in a benchmark, extension, or robustness section?

Required workflow:

proposition-level audit
→ headline-result identification
→ main-model promotion/demotion recommendation
→ handoff to paper reconstruction.

This skill does not write the full paper. It produces a verified research-release packet for om-working-paper-builder.

---

# Scope and integration

Recommended research-core sequence:

1. om-theory-model-auditor → correctness + proposition-level result audit + model-role triage.
2. om-literature-positioning → external novelty search, closest-paper verification, literature ownership.
3. om-working-paper-builder → main-model promotion/demotion and full-paper reconstruction.
4. om-journal-calibrator → venue routing and submission calibration.

When closest papers are already supplied or verified, this auditor may perform a proposition-level novelty-sensitive comparison directly. When literature coverage is incomplete, mark novelty conclusions provisional and hand them to om-literature-positioning.

Never let a novelty or venue preference override a mathematical failure.

---

# Required inputs

Use the latest manuscript, TeX/PDF, model description, or derivation notes.

Extract at minimum:

- players and decision makers;
- timing;
- information structure;
- objective functions;
- constraints;
- strategy spaces;
- uncertainty and distributions;
- equilibrium concept;
- benchmark cases;
- every lemma, proposition, theorem, corollary, and major numerical claim;
- claimed headline contributions;
- supplied closest papers or closest-paper summaries;
- intended managerial/economic mechanism.

If multiple manuscript versions exist, audit the latest version unless the user explicitly asks for comparison.

---

# Stage 1 — Model map and dependency graph

Before checking claims, reconstruct the model as a dependency graph.

Record:

- primitives and parameter domains;
- endogenous variables;
- timing and observability;
- beliefs and information sets;
- feasibility constraints;
- participation / IR constraints;
- incentive / IC constraints;
- resource / capacity / liquidity constraints;
- equilibrium-selection or refinement assumptions;
- objective functions by stage;
- backward-induction order.

Then map each formal result to the exact assumptions and earlier results it uses.

Dependency rule: a proposition cannot be treated as verified if one of its required lemmas, feasibility conditions, or equilibrium-selection steps remains unresolved.

---

# Stage 2 — Mathematical release gate

Audit every formal result and assign exactly one status:

- VERIFIED
- CONDITIONALLY VERIFIED
- INCOMPLETE
- INCORRECT
- CANNOT VERIFY

For each result check:

## Algebra and optimization
- first-order and second-order conditions;
- monotonicity and curvature;
- envelope arguments;
- thresholds and regime boundaries;
- continuity at boundaries;
- interior vs. boundary solutions;
- sign restrictions;
- denominator positivity;
- existence and uniqueness.

## Game/equilibrium logic
- sequential rationality;
- best responses at every stage;
- on-path beliefs;
- off-path beliefs where relevant;
- IC and IR constraints;
- deviations;
- equilibrium multiplicity;
- refinement claims;
- selection assumptions.

## Comparative statics
- derivative signs;
- parameter dependence of regime boundaries;
- cross-regime consistency;
- global vs. local claims;
- nonmonotonicity hidden by regime switching.

## Feasibility and boundary cases
Explicitly test:
- zero / one limits;
- costless / frictionless limits;
- degenerate information;
- no-competition / full-competition limits;
- unconstrained / fully constrained limits;
- parameter values at regime intersections.

## Counterexample search
For every strong qualitative claim, actively search for:
- feasible parameter regions where it fails;
- equilibrium branches that reverse it;
- alternative constraints that bind;
- numerical counterexamples.

Do not repair a false theorem by silently narrowing the parameter set. State the needed condition.

---

# Stage 3 — Proposition inventory

Build a result inventory before deciding contribution importance.

For every lemma/proposition/corollary record:

1. exact formal statement;
2. mathematical status;
3. economic mechanism;
4. direct decision/performance consequence;
5. assumptions required;
6. whether it is a benchmark, structural result, equilibrium consequence, design result, extension, or robustness result;
7. closest prior analogue, if supplied;
8. whether the result is needed for a later headline result.

Use this inventory to prevent a paper from treating every proposition as equally important.

---

# Stage 4 — Proposition-level novelty audit

Novelty is evaluated at the level of formal result + mechanism, not title or notation.

For every result classify it as one of:

- PRIOR RESULT / SAME MECHANISM
- SPECIAL CASE OR REPARAMETERIZATION
- COMBINATION OF KNOWN CHANNELS
- NEW BOUNDARY / REGIME
- NEW EQUILIBRIUM CONSEQUENCE
- NEW MECHANISM
- NEW DESIGN IMPLICATION
- NOVELTY UNRESOLVED

## A. Equivalence test
Ask whether the result becomes a known result after renaming variables, changing notation, normalizing parameters, taking a special case, or imposing/removing a slack constraint. If yes, it is not a headline contribution.

## B. Nested-recovery test
Can the present model recover the closest paper as a limit or benchmark? If yes, identify exactly what new primitive or constraint creates the new result.

## C. Mechanism-isomorphism test
Two results with different formulas may still be the same mechanism. Ask: What causal chain produces the result? If the chain is already known, a new threshold formula is not enough.

## D. Shape-is-not-novelty test
Do not treat an interior optimum, U-shape, inverted-U, threshold, nonmonotonicity, multiple regimes, win-win region, or sign reversal as novel by itself. The paper must explain why the shape arises from a mechanism not already established in the closest literature.

## E. Aggregation test
Distinguish a change in conditional/postdecision behavior from a change in aggregate performance caused only by participation, entry, selection, or funding probability. Do not claim a post-action behavioral mechanism if the model only changes an aggregate outcome through selection.

## F. Composition test
If a proposition simply balances one known increasing constraint and one known decreasing constraint, classify the interior balance as COMBINATION OF KNOWN CHANNELS unless the interaction itself changes behavior or equilibrium in a new way.

---

# Stage 5 — Headline-result identification

A result may be a headline candidate only if it passes all relevant gates.

Check:

1. Correctness — VERIFIED or clearly CONDITIONALLY VERIFIED.
2. Novelty — not merely prior/special-case/reparameterization.
3. Mechanism — reveals a distinct causal mechanism, strategic force, or operational tradeoff.
4. Non-obviousness — a knowledgeable reader would not infer the result without solving the model.
5. Economic/managerial significance — changes a decision, performance metric, design principle, or theoretical understanding.
6. Model centrality — generated by the model the paper presents as central.
7. Robustness of mechanism — survives reasonable relaxation even if closed form changes.
8. Narrative independence — can be stated as an insight, not merely a formula.

Classify each result into one of:

- HEADLINE
- CORE MECHANISM
- EQUILIBRIUM CONSEQUENCE
- BENCHMARK
- EXTENSION
- ROBUSTNESS
- APPENDIX
- MERGE / DELETE

Prefer 2–4 headline results. More usually indicates hierarchy failure.

---

# Stage 6 — Main-model adequacy test

This is a hard gate.

Ask for each intended headline result:

1. Does the main model itself contain the primitive that generates the claimed mechanism?
2. Is the key behavioral response endogenous in the main model?
3. Does the result operate at the level claimed in the prose?
4. Is the paper relying on an extension to obtain the mechanism it claims in the Introduction?
5. Was the current main model chosen mainly because it has cleaner closed forms?

## Promotion rule

Recommend promoting an extension/robustness model to the main model when:

- it is the first place where the headline mechanism is directly represented;
- the simpler current main model can only mimic the aggregate shape indirectly;
- the richer model changes interpretation rather than merely numerical values;
- the paper's contribution statement is false or overstated under the simpler main model.

## Demotion rule

Recommend demoting the current main model to benchmark or appendix when:

- it is analytically convenient but conceptually secondary;
- its main result is already close to prior literature;
- it suppresses the behavior central to the paper's claimed contribution;
- its closed form is useful mainly to illustrate or discipline the richer main model.

Never keep a model as the main model merely because it is easier to solve.

---

# Stage 7 — Result-lineage audit

For each candidate headline result identify the source of novelty:

new primitive
→ new constraint / strategic response
→ new equilibrium mechanism
→ new decision or performance consequence.

If the chain breaks, downgrade the claim.

Useful labels:

- Inherited — carried from prior literature or benchmark.
- Adapted — same mechanism in a different institutional form.
- Interaction — created by interaction of otherwise known forces.
- New mechanism — qualitatively new causal channel.
- New consequence — known mechanism creates a new endogenous outcome because of a new decision layer.

The paper should not call an inherited or adapted element a contribution.

---

# Stage 8 — Main-model promotion/demotion matrix

Produce a matrix with:

Result | Math status | Closest prior overlap | Mechanism source | Current role | Recommended role | Reason

Typical recommendations:

- promote extension → main model;
- main model → benchmark;
- proposition → lemma;
- proposition → corollary;
- proposition → appendix;
- merge with another result;
- delete as redundant;
- retain as headline.

The recommendation must follow logical importance, not original numbering.

---

# Stage 9 — Research release packet

The final output should be directly usable by om-working-paper-builder.

## A. Model correctness
- core model status;
- unresolved derivations;
- required assumptions;
- counterexamples found.

## B. Proposition audit table
For every formal result:
- statement;
- status;
- closest overlap;
- novelty classification;
- recommended role.

## C. Headline set
For each headline:
- formal claim;
- mechanism;
- boundary conditions;
- why it is not a prior result;
- what later section should build on it.

## D. Promotion/demotion decisions
Explicitly state:
- which model becomes main;
- which becomes benchmark;
- what moves to appendix;
- which propositions are demoted or deleted.

## E. Paper-reconstruction instruction
Provide:
- one-sentence paper mechanism;
- preferred result order;
- benchmark purpose;
- extension purpose;
- claims that must not appear in the Introduction.

---

# Mandatory failure conditions

Stop headline promotion when:

- a proof is incomplete;
- equilibrium selection is unverified but required for the claim;
- a result is only numerical and is stated as general;
- the closest paper already proves the same mechanism;
- a result is a trivial corollary of a known result;
- the claimed mechanism occurs only in an extension while the main model lacks it;
- the paper claims a conditional behavioral effect but only demonstrates an aggregate selection effect.

Mark the problem explicitly instead of writing around it.

---

# Domain-specific checks

## Screening / mechanism design
Check IC ordering and single crossing, binding constraints, rents and outside options, exclusion vs. coverage, bunching/pooling/separation, and transfer feasibility.

## Information design / Bayesian persuasion
Check Bayes plausibility, commitment, signal support, posterior feasibility, obedience/action incentives, concavification, and whether information structure or action rights truly generate the result.

## Crowdfunding / platform governance
Check that funding and fulfillment are distinct events; target, price, reserve, and production cash are not conflated; postfunding hidden action is modeled at the stage claimed; refund protection is distinguished from realized delivery; and platform-held funds are distinguished from creator-available working capital.

## Operations finance
Check cash-flow timing, state-contingent repayment, working-capital feasibility, limited liability / recourse assumptions, and whether outside finance relaxes liquidity while changing incentives.

---

# Integration rule

- om-theory-model-auditor owns correctness, proposition-level result integrity, headline eligibility, and model-role triage.
- om-literature-positioning owns comprehensive literature discovery and final closest-paper novelty substantiation.
- om-working-paper-builder owns paper architecture, promotion/demotion implementation, and full narrative reconstruction.
- om-journal-calibrator owns venue routing and journal-specific calibration.

Conflict hierarchy:

1. mathematical truth;
2. verified novelty evidence;
3. mechanism clarity;
4. paper architecture;
5. journal framing.

No later layer may override an earlier failure.
