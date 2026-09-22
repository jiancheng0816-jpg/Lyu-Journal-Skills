# Mechanism and narrative audit for analytical OM papers

Use this protocol after the algebraic claim ledger exists. Its purpose is to verify that the paper's economic story is actually implied by the model and that the benchmark-to-main progression isolates the claimed mechanism.

## 1. Environment-difference ledger

For every analytical environment, record:

| Environment | Added or removed primitive | Changed payoff/constraint/information | Unchanged objects | New candidate behavior | Formal evidence |
|---|---|---|---|---|---|

A main-model result is not attributable to a new feature merely because the feature appears in the same section. Identify the exact term, constraint, or belief that changes the optimizer or equilibrium.

For a policy paper, add:

| Policy | Adoption rule | Decision owner | Intensity fixed/chosen | Available instruments | Stakeholder outcomes |
|---|---|---|---|---|---|

Do not treat a mandatory policy parameter as a creator's signaling instrument. Distinguish a policy-induced change in a constraint from an independently chosen signal.

## 2. Mechanism trace

Translate each headline mechanism into a verifiable chain:

`primitive or institutional linkage -> payoff/constraint change -> marginal or deviation incentive -> endogenous decision response -> equilibrium outcome`.

Check every arrow. A verbal mechanism fails if any arrow depends on an omitted condition, uses an off-equilibrium derivative as an equilibrium comparative static, or reverses direction in an admissible region.

For opposing-forces claims, build separate traces for each force before deriving the net effect. Examples of distinct forces include continuation-value protection versus current revenue, imitation deterrence versus signaling opportunity cost, and direct payoff effects versus selection effects.

For information design, use the trace `state/prior -> experiment and posterior -> receiver best response -> sender interim payoff -> optimal posterior split`. Add a preference-alignment map showing how the sender's and receiver's desired actions move with the posterior. Verify that alignment of directional responses is not overstated as identical preferred actions or welfare alignment.

For instrument-dominance claims, identify each source of strategic power, the instrument through which it operates, and the threshold at which their relative strength changes. A shared observable action does not make two instruments equivalent if decision ownership, feasible deviations, binding constraints, or equilibrium outcomes differ.

## 3. Benchmark nesting and recovery

When the manuscript says it extends, generalizes, or subsumes a closest paper:

- state the exact parameter, policy, or decision restriction that should recover the prior model;
- verify payoffs, feasible sets, information, equilibrium concept, and tie-breaking under that restriction;
- recover the prior equilibrium or explain any remaining difference;
- identify the first condition under which the focal result departs from the recovered benchmark.

If the models are nonnested, require comparison language rather than a generalization claim.

## 4. Instrument and regime audit

When the paper uses multiple instruments or reports several regimes:

- identify which constraints bind in each regime;
- distinguish a decision that is independently distorted from one that changes mechanically because of an identity or binding feasibility constraint;
- prove the interior candidate exists before calling it a hybrid or double-instrument regime;
- verify first- and second-order conditions or tangency conditions, then compare the interior point with endpoints;
- prove regime thresholds are ordered and regions nonempty;
- check whether a regime name remains accurate at equality boundaries.

An apparent joint movement of two variables is not a hybrid mechanism if one variable merely adjusts to keep a product, budget, or threshold fixed.

When information and a monetary or operational lever are jointly chosen, identify whether the claimed substitution or complementarity is a within-regime derivative, an informativeness change, a discrete experiment switch, a receiver-action effect, or a comparison of global optima.

When an actor can choose whether to adopt a policy and how intensively to use it, separate the discrete adoption signal from the continuous intensity choice. Verify whether each independently affects beliefs or incentives.

## 5. Assumption-defense audit

For every consequential assumption, record:

- the property or proof step it guarantees;
- the trivial, infeasible, or off-scope cases it excludes;
- whether its admissible parameter set is nonempty;
- whether the manuscript provides an analytical special case, numerical witness, or institutional rationale;
- which result fails or changes when it is relaxed.

Do not accept “not restrictive” without evidence. A figure can demonstrate nonemptiness or illustrate a threshold but cannot prove general validity.

## 6. Comparative-static decomposition

For every comparative static, classify the claimed change as one or more of:

- direct effect on a payoff;
- strategic effect through another player's deviation or participation incentive;
- endogenous-response effect through another decision;
- regime-switching effect at a threshold;
- equilibrium-selection effect among coexisting outcomes.

Derive signs within each regime before describing the global path. Verify discontinuities explicitly. For reversals, identify the ranking or active constraint that changes at the reversal threshold and prove that the threshold lies in the claimed region.

## 7. Equilibrium-form and selection audit

When separation, pooling, deterrence, accommodation, or other equilibrium forms may coexist:

- derive existence conditions for every admissible form;
- verify off-path beliefs and refinements under the same equilibrium concept;
- distinguish existence from selection and selection from welfare;
- confirm that the claimed selection parameter changes the relevant payoff comparison;
- check whether a feature that disciplines one type can simultaneously reduce another type's incentive to reveal information.

Do not describe a selected equilibrium as unique unless alternatives have been ruled out.

Do not call an equilibrium `preferred` until the preference criterion is defined. Verify whether it reflects a refinement, one player's profit, consumer delivery probability, total welfare, or another named objective.

## 8. Policy, delegation, and stakeholder audit

When comparing mandatory and voluntary policies, platform-determined and firm-determined parameters, or alternative instrument sets:

- compare them on a common primitive domain and identify policy-specific feasibility constraints;
- establish equilibrium existence with a fixed policy intensity before delegating its choice when the argument depends on that sequence;
- verify that added discretion does not destroy separation, participation, commitment, or another intended outcome;
- record profit or utility for every stakeholder named in the recommendation;
- distinguish information revelation, success probability, consumer surplus, firm profit, platform profit, and welfare.

Use these term checks:

- `optimal`: correct objective and feasible set;
- `dominates`: stated comparison dimensions and domain;
- `win-win`: every named stakeholder weakly improves and at least one strictly improves;
- `indispensable` or `necessary`: no admissible alternative policy or instrument achieves the stated outcome.

## 9. Figure audit

For analytical geometry figures, verify:

- every boundary is generated by the stated equation;
- shading matches the true feasible set;
- contour values move in the stated preferred direction;
- the marked optimum is feasible and lies on the claimed active boundary;
- axis units, parameter values, and regime captions match the text;
- the figure illustrates a proved result rather than standing in for proof.

For comparative-static figures, regenerate the path from the final formulas and verify within-regime slopes, threshold locations, jumps, plateaus, and benchmark lines.

Build a panel-level crosswalk:

| Figure panel | Formal result | Formula or boundary | Axis-to-primitive mapping | Economic role | Prose location |
|---|---|---|---|---|---|

Require the text before the figure to identify what propositions and parameter movements the visual maps. Require the text after the figure to interpret the cross-panel or cross-institution contrast, including profit, payment, trade, or stakeholder consequences when shown. If two figures depict paired regimes, verify that the manuscript states the comparison explicitly and does not ask the reader to infer it from colors or shapes alone.

## 10. Extension audit

Each extension must name the threat it tests. Set a verdict:

- `PRESERVES`: the same mechanism and qualitative result survive;
- `ATTENUATES`: the mechanism survives but weakens or requires tighter conditions;
- `REVERSES`: the same mechanism generates the opposite outcome in a named region;
- `REPLACES`: a different mechanism drives the result;
- `INCONCLUSIVE`: the extension has not established a clear relation to the headline mechanism.

A special-case numerical example cannot establish robustness over a class of primitives.

When analysis transitions to numerical optimization, require a regime-complete search with boundary and discrete-alternative comparisons. Record the analytical results retained, the source of intractability, reproducibility settings, and whether the computation is illustrative, systematic, or exhaustive.

Also state whether the extension changes the feasible policy, instrument ranking, or allocation of decision rights. A mechanism-preserving extension can still overturn a governance recommendation.

## 11. Narrative alignment audit

Create a final map:

| Formal result | Abstract claim | Introduction finding | Main-text mechanism | Figure/table | Literature distinction | Conclusion claim |
|---|---|---|---|---|---|---|

Flag any row in which:

- conditions disappear outside the proposition;
- a weak or local result becomes strict or global;
- a profit result becomes a welfare result;
- coexistence becomes uniqueness;
- an illustration becomes evidence;
- a different setting is described as a different mechanism without showing the changed incentive;
- the conclusion attributes a result to a feature that is not isolated by the benchmark.
- a policy-induced target or price change is mislabeled as an independently chosen signaling instrument;
- `preferred`, `dominates`, `necessary`, or `win-win` lacks its required criterion or stakeholder comparison.
- a disclosure taxonomy is treated as exhaustive without an experiment-support or concavification argument;
- an entropy or precision comparison is described as Blackwell dominance without proof;
- a derivative or elasticity is evaluated at a discontinuous regime switch;
- an inherited formal result is presented as a new contribution.

Correct the formal and narrative objects together.

## 12. Result-chain and discussion audit

For every proposition and corollary, verify that the main text does more than restate the formula. A headline result should normally receive one or two substantive paragraphs that cover its economic content, active mechanism, benchmark or predecessor, and decision relevance. A literature comparison is required only when a verified close analogue exists, but when used it must identify whether the conclusion is aligned or opposed and explain the mechanism responsible for the agreement or reversal.

Create a dependency ledger:

| Result | Predecessor or benchmark | What changes | New mechanism or remapping? | Downstream result | Figure panel |
|---|---|---|---|---|---|

Flag isolated results with no declared analytical role, paired results whose comparison uses different primitive domains, reverse mappings presented as new forces, and figure interpretations that introduce claims absent from the formal analysis. The chain should read cumulatively from benchmark to institutional comparison rather than as a sequence of unrelated propositions.
