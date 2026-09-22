# Information-design model audit

Use this protocol for Bayesian persuasion, endogenous disclosure, market testing, recommendation, data precision, or another model in which an actor commits to an information structure to influence another actor's operational decision.

## 1. Identify the information technology

Record separately:

| Object | Audit question |
| --- | --- |
| State | What payoff-relevant uncertainty exists and when is it realized? |
| Prior | Is it common, heterogeneous, or privately known? |
| Acquisition | Does information preexist, or must a test generate it at a cost? |
| Sender | Who designs or commits to the experiment? |
| Receiver | Who observes the signal and takes which action? |
| Experiment set | Which conditional signal distributions are technologically feasible? |
| Commitment | Why can the sender not redesign or misreport after the state or signal is observed? |
| Observability | Which actors observe the experiment, realization, and posterior-relevant information? |
| Reporting | Is signal transmission truthful, cheap talk, verifiable, audited, or contractible? |

Do not let the prose treat acquisition, experiment design, disclosure, and truthful reporting as the same primitive. A sender who can choose an arbitrary Bayes-plausible experiment has more power than a firm that can only disclose or suppress a fixed test result.

## 2. Verify Bayes plausibility and implementation

- Derive posterior beliefs after every on-path signal.
- Verify posterior probabilities lie in the simplex and zero-probability signals are handled.
- Check that the distribution of posteriors averages to the prior.
- Recover conditional signal probabilities from the proposed posterior distribution.
- Verify all conditional probabilities satisfy the technological restrictions, including monotone-likelihood or accuracy constraints when imposed.
- Distinguish statistical feasibility from institutional implementability.

An arbitrary Bayes-plausible posterior split is valid only if the declared experiment set allows it.

## 3. Re-solve the receiver problem

For every posterior region:

- solve the receiver's true feasible action problem;
- verify concavity, corners, kinks, and tie breaking;
- prove thresholds and action monotonicity;
- identify whether a higher posterior increases or decreases the action;
- check state-contingent realized outcomes, not only the expected action.

Then substitute the receiver best response into the sender payoff. Do not optimize the experiment against an off-equilibrium or desired receiver action.

## 4. Audit preference alignment

Construct:

| Posterior region | Receiver action | Sender-preferred action | Alignment | Active distortion |
| --- | --- | --- | --- | --- |

Verify every claimed alignment or misalignment threshold. A shared directional response does not imply identical preferred action levels. Distinguish action alignment, payoff alignment, and welfare alignment.

## 5. Solve the experiment problem

- Write the sender's interim value as a function of the posterior after incorporating the receiver response.
- Determine the concave envelope or solve the equivalent posterior-distribution problem.
- Verify the supporting posteriors, signal probabilities, and contact points.
- Compare full disclosure, partial disclosure, pooling, and any other feasible experiment.
- Prove existence and global optimality, including boundary experiments.
- Check whether multiple experiments implement the same posterior distribution or payoff.

When the manuscript claims that binary signals, full/partial/non-disclosure, or a particular posterior split is without loss of generality, require a support-reduction, concavification, or equivalent proof. A list of candidate experiments is not an exhaustiveness argument.

## 6. Audit informativeness measures

Identify whether the manuscript uses:

- Blackwell ordering;
- expected posterior entropy or mutual information;
- likelihood-ratio or precision parameters;
- posterior variance;
- a custom transparency or informativeness index.

For the chosen measure:

- verify the formula and benchmark normalization;
- state whether it completely or only partially orders experiments;
- check whether higher values mean more or less information consistently;
- verify continuity and differentiability on each regime;
- separate within-regime derivatives from jumps at experiment switches;
- do not accept an ordinary elasticity at a discontinuity unless a one-sided or generalized definition is provided.

An entropy ranking alone does not establish Blackwell dominance for arbitrary experiments.

## 7. Audit joint information and monetary levers

When the sender also chooses price, subsidy, commission, contract, capacity, or another operational lever:

1. solve the fixed-lever information problem only if it is used as a valid stepping stone;
2. verify the joint feasible set and timing of both commitments;
3. account for how the noninformation lever changes the receiver response and sender interim value;
4. distinguish continuous substitution or complementarity from a discrete switch in the optimal experiment;
5. compare joint optima with every relevant single-lever benchmark;
6. check whether the second lever changes information acquisition incentives, not only disclosure.

Do not infer complementarity solely because both levers are positive or used in the same regime.

## 8. Audit benchmark and stakeholder claims

Keep separate:

- no-information or no-design benchmark;
- fixed-lever mechanism-isolation benchmark;
- full-information benchmark;
- centralized or first-best benchmark;
- closest-paper recovery.

Verify that the named benchmark supports the claimed comparison. Maintain separate outcomes for sender profit, receiver profit, receiver action, service or matching performance, consumer surplus, and total welfare. More information need not benefit the receiver when the sender changes another endogenous lever.

## 9. Audit analytical-to-numerical handoffs

If a joint experiment or contract is solved numerically:

- list what has been proved analytically;
- verify the stated source of intractability;
- enumerate all experiment and operational regimes;
- optimize within each regime and compare boundaries, corners, and discrete alternatives;
- check global rather than only local optimality;
- record parameter domains, grids or solvers, tolerances, seeds, and refinement tests;
- repeat across admissible parameterizations sufficient for the claimed scope;
- label representative figures as illustrations rather than theorems.

Assign `INCOMPLETE` when the numerical search omits an admissible regime or has no credible global-optimality check.

## 10. Audit result provenance

For every formal result adapted from a closest paper, record:

- source and precise result locator;
- whether it is inherited, specialized, adapted, or newly proved;
- whether the focal assumptions satisfy the source result's conditions;
- whether the manuscript reproduces, re-proves, or modifies it;
- which downstream result genuinely belongs to the focal paper.

Do not credit an inherited response characterization or persuasion theorem as a contribution merely because notation or the operational context changed.
