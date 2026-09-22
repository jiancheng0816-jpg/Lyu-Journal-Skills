# Working-paper release checklist

## Analytical integrity

- Every headline result has an approved audit verdict.
- Proposition conditions match proofs and downstream prose.
- Parameter regions are exhaustive and boundaries are handled.
- Figures and tables reproduce the final equations or data.
- Extensions are classified by their effect on the main mechanism.
- Claimed nested benchmarks are recovered exactly under the stated parameter or policy restriction.
- Consequential assumptions have a documented role, excluded cases, nonempty admissible region, and relaxation test.
- Information-design models satisfy the stated commitment, Bayes-plausibility, receiver-response, and experiment-feasibility conditions.
- Claims that full, partial, and non-disclosure exhaust the optimum have an analytical basis.
- Derived informativeness, efficiency, alignment, and elasticity measures are valid on their claimed domains and treat discontinuities correctly.
- Reused formal results are marked internally as new, adapted, specialized, or inherited and are attributed accurately.
- Analytical-to-numerical handoffs document the analytical frontier, intractability, regime coverage, boundary comparisons, reproducibility, and claim scope.

## Literature integrity

- Every citation exists and its metadata is verified.
- Source-specific claims respect full-text, abstract, or metadata evidence status.
- Closest papers are confronted directly.
- Novelty language is bounded by the documented search.
- Citation keys in the manuscript exist in the bibliography and unused entries are reviewed.

## Manuscript consistency

- Title, abstract, introduction, model, results, implications, and conclusion use consistent constructs.
- Actors own the correct decisions throughout.
- Symbols, subscripts, superscripts, and parameter domains are stable.
- Equation, proposition, section, figure, table, and appendix references resolve.
- No result is duplicated under multiple proposition labels without a clear reason.
- Abstract finding groups, introduction finding groups, main-section order, proposition chain, and conclusion synthesis are isomorphic.
- Every proposition and corollary identifies its closest predecessor or benchmark, its analytical role, and the question it resolves or creates; reverse mappings and reparameterizations are not mislabeled as new mechanisms.
- Every enriched environment states the exact payoff, constraint, or information linkage added relative to the preceding environment.
- Every benchmark has one declared job: mechanism isolation, fixed-lever comparison, full information, first best, or closest-paper recovery.
- Regime labels are economically meaningful and stable throughout the manuscript.

## Exposition quality

- Each main section answers one analytical question and motivates the next.
- Each headline proposition receives a benchmark comparison, mechanism explanation, and condition-sensitive interpretation, not merely a paraphrase.
- Every formal result receives substantive discussion; headline results normally have one or two natural paragraphs covering the result, mechanism, institutional or managerial relevance, and a verified literature comparison when materially applicable.
- Direct, strategic, regime-switching, and selection effects are not conflated.
- Figures identify their objects, parameterization, optimum, and analytical role in the surrounding text.
- Every figure panel, boundary, slope, jump, plateau, and no-trade region is mapped to the formal result that supports it, and paired figures are explicitly compared across products, instruments, or institutions.
- Figure introductions explain the axis-to-primitive mapping; post-figure prose explains the economic or distributional consequence rather than merely repeating the caption.
- Information-design figures distinguish state geometry, posterior or preference geometry, optimal-policy regions, benchmark outcomes, and numerical illustration.
- Substitution and complementarity language identifies whether it describes a local response, informativeness metric, regime switch, receiver action, or global policy path.
- Literature comparisons distinguish setting, endogenous choices, and mechanism rather than relying on keyword overlap.
- Extensions state the threat tested and whether the mechanism persists, attenuates, reverses, or is replaced.
- Policy papers identify adoption rule, decision owner, policy intensity, instrument set, and stakeholder outcomes in every compared regime.
- `Optimal`, `preferred`, `dominates`, and `win-win` are supported by the stated objective, criterion, stakeholders, and parameter scope.
- Headline new instruments or mechanisms address the strongest plausible equivalence objection.
- Paragraphs have clear topic sentences and one dominant analytical function; repeated stock transitions and mechanical subheadings have been removed.
- Concision edits remove duplication and processing cost without deleting concrete stakes, comparison baselines, necessary antecedents, mechanism bridges, or question-generating transitions.
- Each headline reversal or unexpected result states the benchmark intuition it departs from and the condition or regime that produces the departure; interest does not rely on unsupported promotional adjectives.
- Analytical density varies deliberately: formal statements and conditions are followed by enough economic translation for first-pass comprehension, with short payoff sentences used selectively rather than mechanically.

## LaTeX and visual QA

- The project compiles from a clean state with the documented command sequence.
- Bibliography and cross-references are rerun until stable.
- Overfull boxes, clipped equations, blank pages, broken links, and misplaced floats are fixed.
- Every rendered page is inspected at readable resolution.
- Final PDF and source files correspond to the same build.

## Release decision

Label the package `submission-ready`, `circulation-ready`, `internal draft`, or `blocked`. List every unresolved item and its effect on claims or presentation.
