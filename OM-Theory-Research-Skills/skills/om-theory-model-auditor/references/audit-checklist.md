# Audit checklist

Use this checklist as a set of proof obligations. Mark each item `pass`, `fail`, `not applicable`, or `not testable from supplied material`.

## Model foundation

- Identify every player and the owner of every decision variable.
- Reconstruct the event timeline and information available at each move.
- Verify that observability, commitment, recall, learning, and updating assumptions match the institutional story.
- Check units, parameter domains, distribution support, normalization, and outside options.
- Distinguish primitives from equilibrium objects and exogenous variables from endogenous choices.
- Verify that demand, probability, market share, precision, reach, and prices remain within feasible ranges.
- Distinguish policy adoption, policy intensity, decision ownership, and the endogenous instrument set across regimes.
- For information design, distinguish state uncertainty, acquisition, experiment design, disclosure, reporting, commitment, posteriors, and receiver action.

## Optimization

- Write each objective on its true feasible set.
- Check existence before characterizing an optimum.
- Verify first-order conditions, second-order conditions, concavity or quasiconcavity, and nondifferentiable points.
- Compare interior candidates with all relevant boundaries and discrete alternatives.
- Apply the envelope theorem only after its hypotheses and optimizer dependence are established.
- Check whether an alleged optimum is local, global, unique, or one of several optima.

## Games and information

- Verify the equilibrium concept and off-path beliefs when relevant.
- Check every unilateral deviation, not only the deviation emphasized in the text.
- Write incentive-compatibility, participation, individual-rationality, and feasibility constraints separately.
- Verify pooling, separating, semi-separating, deterrence, accommodation, and no-trade candidates whenever admissible.
- Check tie-breaking assumptions and measure-zero boundaries because they can affect threshold statements.
- Confirm that signals are observable at the time agents are assumed to respond.
- Separate a discrete adoption signal from a continuous policy-intensity choice and test whether each independently affects beliefs.
- Verify Bayes plausibility, experiment-set restrictions, zero-probability signals, receiver best responses at every posterior, and sender commitment.
- Require a support-reduction or concavification argument for claims that a signal alphabet or disclosure taxonomy is without loss of generality.

## Thresholds and regions

- Derive each threshold from the binding equation rather than from verbal intuition.
- Prove the threshold lies in its claimed domain.
- Prove all reported thresholds have the stated ordering.
- Make regions mutually exclusive and collectively exhaustive.
- Check continuity, jumps, and agreement of formulas at shared boundaries.
- State empty regions explicitly when an ordering makes them infeasible.
- Distinguish independently distorted instruments from variables that move mechanically to maintain a binding identity or constraint.
- For an interior or hybrid regime, verify tangency or first-order conditions, curvature, endpoint comparisons, and nonemptiness.
- For each consequential assumption, verify its role, excluded cases, nonempty admissible region, and the result affected by relaxation.
- For derived informativeness, efficiency, alignment, or elasticity measures, verify the economic construct, domain, ordering content, continuity, and differentiability.

## Benchmarks and nesting

- Recover complete-information and mechanism-off benchmarks on their correct feasible sets.
- If the paper claims to extend, generalize, or subsume a closest model, verify the exact parameter or policy restriction that recovers it.
- Check that the recovered payoff, information structure, decision ownership, equilibrium concept, and result match the cited model.
- Use comparison rather than generalization language when the models are nonnested.

## Comparative statics

- Differentiate the equilibrium object, not an off-equilibrium objective, unless clearly labeled.
- Account for endogenous responses and regime switching.
- Verify the sign over the full claimed domain; report sign changes and nonmonotonicity.
- Distinguish weak from strict inequalities and local from global comparative statics.
- For U-, inverted-U-, V-, or inverted-V claims, verify turning points, slopes on both sides, and smoothness or kinks.
- Check whether an effect is direct, strategic, selection-driven, or induced by a changing active set.
- Separate within-regime derivatives from discontinuous jumps across regimes and verify both parts of any global path.
- For a claimed reversal, identify and prove the threshold at which the relevant success, payoff, or incentive ranking changes.

## Robustness and computation

- Test limiting cases, symmetry, zero-cost, prohibitively high-cost, full-information, and no-information benchmarks when admissible.
- Search systematically for counterexamples within the declared parameter domain.
- Record code, solver, precision, parameter grid, random seed, and tolerances for computational checks.
- Distinguish numerical support, exhaustive computation, symbolic identity, and formal proof.
- Classify each extension as mechanism-preserving, mechanism-attenuating, mechanism-reversing, or introducing a new mechanism.
- Record whether each extension changes policy feasibility, instrument ranking, or decision ownership even when the mechanism survives.
- For analytical-to-numerical handoffs, record the analytical frontier, source of intractability, regimes and boundaries searched, global-optimality logic, parameter coverage, and exact claim scope.

## Policy and stakeholder claims

- Compare mandatory and voluntary policies, fixed and delegated intensities, and instrument sets on a common primitive domain.
- Verify that delegation preserves the intended equilibrium before treating added discretion as beneficial.
- Maintain separate outcome columns for every modeled stakeholder and operational performance measure.
- Require a named objective for `optimal`, a criterion for `preferred`, comparison dimensions for `dominates`, and weak gains for all named stakeholders plus one strict gain for `win-win`.
- Verify necessity or indispensability against every admissible alternative policy and instrument.
- For information and monetary levers, distinguish local marginal substitution/complementarity, discrete experiment switches, action effects, and global policy comparisons.

## Manuscript consistency

- Match every proposition to its proof and every figure/table to the formula that generated it.
- Check notation, equation numbers, cross-references, captions, and parameter values.
- Verify that the abstract, introduction, mechanism discussion, and managerial implications do not exceed the formal result.
- Trace every corrected result through later sections and appendices.
- Separate a model artifact from an institutionally meaningful mechanism.
- Verify that each enriched environment differs from its benchmark by the exact term or constraint credited with the new result.
- Map each abstract and introduction finding to a formal result with identical conditions and direction.
- Verify that literature contrasts identify a different active mechanism rather than only a different application or notation.
- Verify that claimed nested literature results are recovered exactly and that policy recommendations use the stakeholder scope proved by the model.
- Verify that every reused formal result is attributed and classified as inherited, specialized, adapted, or new.
