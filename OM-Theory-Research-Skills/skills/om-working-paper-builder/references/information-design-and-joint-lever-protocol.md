# Information-design and joint-lever writing protocol

Use this protocol for Bayesian persuasion, endogenous disclosure, market testing, recommendation, data precision, or another model in which an actor designs information while also choosing a price, subsidy, contract, capacity, or operational lever.

## 1. Freeze the information-design contract

Before writing results, record:

| Object | Required statement |
| --- | --- |
| State | What uncertainty is payoff relevant and when it is realized |
| Prior | What each actor knows before the experiment |
| Sender | Who commits to the experiment and what objective is optimized |
| Receiver | Who observes the signal and which action responds |
| Acquisition | Whether information already exists or must be generated at a cost |
| Experiment | Feasible conditional signal distributions and any technological restrictions |
| Commitment and credibility | Why the announced experiment and signal realization are binding or truthful |
| Posterior | How beliefs update and the Bayes-plausibility restriction |
| Interim payoff | Sender payoff after substituting the receiver's best response |
| Informativeness | Blackwell order, entropy, mutual information, precision, or another declared measure |

Do not use `information acquisition`, `forecasting`, `sharing`, `disclosure`, and `persuasion` interchangeably. State which stage is strategic.

## 2. Build the preference-alignment map

Before solving the optimal experiment, characterize the operational action under an arbitrary posterior. When useful, identify a sufficient statistic such as a critical ratio, marginal value, or target action.

Create a map:

| Posterior region | Receiver's optimal action | Sender's desired action | Aligned or misaligned? | Active risk or distortion |
| --- | --- | --- | --- | --- |

This map should explain why full, partial, or no disclosure is desirable. If the sender sometimes wants to reduce rather than increase the receiver's action, state that explicitly; information design is action matching, not automatically action expansion.

## 3. Use the joint-lever architecture

When information interacts with a monetary or operational lever, a useful cumulative sequence is:

1. characterize the receiver's operational response;
2. derive actor preferences as beliefs change;
3. solve the monetary or operational benchmark without information design;
4. fix the other lever and solve the optimal experiment as a mechanism-isolating step;
5. jointly optimize the information and noninformation levers;
6. identify substitution, complementarity, and inactive-lever regions;
7. compare actions, profits, stakeholder outcomes, and efficiency with the relevant benchmarks;
8. add a third lever only when it creates a new alignment or risk-sharing mechanism.

An exogenous-lever analysis belongs in the main text when it exposes the mechanism used by the joint solution. Otherwise, keep it in the appendix.

## 4. Maintain a benchmark portfolio

Different benchmarks answer different questions:

- **No-information or no-design benchmark:** incremental effect of the experiment.
- **Fixed-lever benchmark:** isolates information design from pricing or contracting.
- **Full-information benchmark:** removes state uncertainty or private information.
- **Centralized or first-best benchmark:** measures coordination or welfare loss.
- **Closest-paper benchmark:** establishes the contribution and any nesting relationship.

Name the job of each benchmark before using it. Do not use a profit benchmark to support an efficiency claim or a separation benchmark to support consumer welfare.

## 5. Write disclosure regimes through action consequences

For each disclosure regime, state:

1. the induced posterior distribution;
2. the receiver action after each signal;
3. which action distortion is corrected or created;
4. why the sender prefers the regime;
5. how the other endogenous lever changes;
6. the stakeholder consequences.

Use full, partial, and non-disclosure labels only after proving that the candidate experiment set is exhaustive for the claimed environment. If the optimal experiment uses pooling, splitting, or boundary posteriors, explain its posterior geometry rather than only reporting conditional signal probabilities.

## 6. Explain substitution and complementarity precisely

Two levers are substitutes or complements only relative to a named response and comparison:

- local marginal response within one regime;
- change in an optimal informativeness metric;
- discrete switch between disclosure regimes;
- joint effect on the receiver action;
- global comparison of optimal policies.

Separate continuous adjustment from threshold jumps. A discontinuous switch from no disclosure to full disclosure is not an ordinary positive elasticity.

## 7. Use derived metrics carefully

When introducing entropy, mutual information, efficiency ratios, elasticities, alignment gaps, or another derived measure:

- define its domain and benchmark;
- explain why it measures the economic construct of interest;
- state whether it provides a complete order or only a scalar summary;
- distinguish level, derivative, jump, and regime classification;
- avoid differentiating at a discontinuity unless a one-sided or generalized notion is defined.

Do not introduce a new metric solely to redescribe a result already clear from regime boundaries.

## 8. Mark formal-result provenance

Maintain a provenance ledger:

| Result | Status | Source or prior result | What is re-proved or changed | Role in the focal paper |
| --- | --- | --- | --- | --- |

Use:

- `NEW` for a result first established by the focal analysis;
- `ADAPTED` when a prior argument is rebuilt under changed primitives;
- `SPECIALIZED` for a restricted version of a known result;
- `INHERITED` when the result is invoked without a new contribution claim.

Attribute inherited results in the formal label or immediately preceding sentence. Explain why the result is needed downstream.

## 9. Manage the analytical-to-numerical handoff

When joint optimization lacks a useful closed form:

1. state which response functions, regimes, boundaries, or monotonicities are analytical;
2. explain the exact source of intractability;
3. optimize within every admissible regime and compare local optima with boundaries and discrete alternatives;
4. document parameter domains, grids or solvers, tolerances, and global-search logic;
5. label figures as examples, systematic numerical characterizations, or exhaustive computations;
6. test whether the observed regime sequence and comparative statics survive alternative parameterizations;
7. restrict prose claims to the demonstrated numerical scope.

The narrative should explain what the computation teaches about the mechanism, not merely display an optimizer.

## 10. Design the visual portfolio

Use a small set of visuals with distinct jobs:

- state or support geometry;
- preference-alignment or critical-ratio map;
- optimal policy and regime map;
- benchmark comparison;
- stakeholder or efficiency outcome;
- numerical extension when no analytical characterization exists.

Do not use multiple figures to repeat the same regime path. Every visual must identify whether boundaries are proved, computed, or illustrative.
