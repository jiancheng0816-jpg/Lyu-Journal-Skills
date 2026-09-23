---
name: om-working-paper-builder
description: Build or structurally reconstruct complete analytical OM and management-science working papers from verified models and source-backed literature. Implicitly trigger for 重构working paper、重写论文、生成完整working paper、按照OM顶刊标准写作、重新组织全文、写LaTeX/PDF、paper restructuring, build/rewrite a theoretical manuscript, or requests to promote/demote models and reorganize headline results. Do not trigger for model checking alone, literature search alone, reviewer-response letters, or small prose edits that do not require paper-level architecture.
---

# OM Working Paper Builder

Turn verified analytical results and source-backed positioning into a coherent, reproducible working paper. Preserve correctness across equations, propositions, mechanisms, contributions, figures, and citations.


# Smart-trigger routing

This skill supports implicit invocation, but only when the task falls inside its ownership boundary.

## Positive trigger phrases / intents

- `重构working paper`
- `重构论文`
- `重写working paper`
- `生成完整working paper`
- `按照OM顶刊标准`
- `重新组织全文`
- `生成LaTeX`
- `生成PDF论文`
- `paper restructuring`
- `build working paper`
- `rewrite manuscript`
- `full theoretical manuscript`
- `promote/demote main model`

## Exclusion conditions

Do **not** implicitly invoke this skill when the user is only asking for:

- 只检查模型/命题/证明;
- 只做文献检索和novelty comparison;
- 只回复审稿人;
- 只润色一个段落/一句话且不涉及全文结构;


## Ownership

Primary owner: **paper architecture and full working-paper reconstruction**. If another OM skill more directly owns the requested deliverable, defer to that skill and act only as a supporting gate when needed.

## Cross-Skill routing order

Use the following ownership order to avoid competing implicit invocations:

1. **Reviewer package present** → `om-reviewer-response-builder` owns the user-facing task. It may request support from the auditor or literature-positioning logic, but the response builder integrates the final revision/letter.
2. **Correctness / proof / equilibrium requested** → `om-theory-model-auditor` runs before any rewriting.
3. **Closest-literature / novelty requested** → `om-literature-positioning` owns external novelty substantiation. If the novelty claim depends on whether a proposition is mathematically valid, auditor first.
4. **Full-paper generation or reconstruction requested** → `om-working-paper-builder` runs after any required correctness and novelty gates.
5. **Journal/venue routing** → do not auto-route to `om-journal-calibrator`; use it only when the user explicitly asks for journal selection, department ownership, venue calibration, or a pre-submission audit.

### Multi-intent examples

- “检查模型并重构全文” → auditor → builder.
- “逐命题和 Guo (2025) 比较后重构” → auditor when correctness is in scope → literature positioning → builder.
- “按照审稿意见修改模型并写回复信” → response builder owns the workflow; use auditor for challenged derivations and literature positioning for challenged novelty, then return to response builder.
- “这篇文章适合投 MS 还是 M&SOM” → journal calibrator only when explicitly requested; do not launch the full research-core pipeline unless the user also asks for it.

## Entry gates

Collect the strongest available versions of:

- research question, institutional motivation, and target audience;
- model map, notation, assumptions, equilibrium concept, and source equations;
- claim ledger from `om-theory-model-auditor` or equivalent verification;
- proofs, counterexamples, numerical checks, and robustness map;
- closest-paper matrix and verified references from `om-literature-positioning`;
- existing LaTeX, bibliography, figures, prior manuscript, and preferred style sample;
- target journal family, length, proof-placement preference, and desired deliverables.

If headline results have not been audited, route them through `om-theory-model-auditor` before presenting the paper as verified. If literature claims are not source-backed, route them through `om-literature-positioning`. Continue with an explicitly labeled provisional draft only when the user requests it.

## Workflow

1. Read `references/reference-paper-writing-standard.md`, `references/paper-architecture.md`, `references/result-writing-protocol.md`, `references/model-promotion-and-paper-reconstruction-protocol.md`, and `references/release-checklist.md`. For Bayesian persuasion, disclosure, information acquisition, or joint information-monetary-lever papers, also read `references/information-design-and-joint-lever-protocol.md`.
2. Freeze a manuscript contract: research question or connected question ladder, central analytical architecture, two to four headline result groups, contribution boundaries, maintained assumptions, excluded cases, target outlet family, and deliverables.
3. Build linked maps for the event timeline, result hierarchy, section-to-result allocation, result-to-result dependency chain, vocabulary, and result-to-figure crosswalk; when policy or governance matters, also build a policy-instrument-decision-rights map with stakeholder outcomes. The dependency chain should identify the benchmark for each result, whether the result adds a mechanism, changes an institution, or merely reverses an earlier parameter mapping, and which next question it creates. For information-design papers, add a state-prior-experiment-posterior-action map and a preference-alignment map showing how each actor's desired action changes with beliefs. Give each section one analytical job and trace every headline claim and visual panel to a verified proposition or evidence record.
4. Choose the story architecture that fits the verified model. Use a mechanism-progression architecture for opposing forces, continuation values, reversals, or equilibrium selection; use a policy-and-instrument architecture for instrument substitution, mandatory versus voluntary adoption, staged endogenization, or allocation of decision rights; use a joint-lever architecture when an informational lever and a monetary or operational lever are first isolated and then optimized together. Combine architectures only when each organizes genuine headline results.
5. Draft the title, abstract, and introduction only after the result hierarchy is stable. Ensure that motivation, research question, findings, contributions, and implications use the same vocabulary as the model. Use the introduction's finding groups as a faithful map of the main analysis rather than as a separate sales pitch.
6. Organize related literature by decision problem and mechanism. Use only verified citations and calibrated novelty language. Distinguish a different mechanism from a different setting or notation.
7. State the model with institutional mapping, a complete timeline, actor-specific decisions, information, objectives, feasibility, assumptions, equilibrium concept, and notation table. In information-design models, distinguish information acquisition from experiment design and disclosure; define the state, prior, commitment, experiment set, signals, posteriors, Bayes-plausibility condition, receiver action, and sender interim payoff. Distinguish inherited structure from genuinely new features without forcing those phrases into section titles. Defend consequential assumptions by stating what they guarantee, what they exclude, why the admissible region is nonempty, and what relaxation would threaten.
8. Present complete-information, mechanism-removed, fixed-lever, no-information, closest-paper, or first-best benchmarks according to the separate analytical jobs they perform. Recover a structurally nested closest model at the appropriate restriction whenever the claimed relationship requires it. Order the analysis cumulatively: characterize the receiver or operational response, derive actor preference alignment, solve the focal instrument with other levers fixed, jointly endogenize the levers, compare benchmark and stakeholder outcomes, then examine extensions or selection when relevant.
9. Write every formal result with `references/result-writing-protocol.md`. Preserve the exact conditions and verdict from the audit ledger. Give every proposition and corollary an interpretive discussion; a headline result normally needs one or two substantive paragraphs covering the economic content, mechanism, benchmark or predecessor, and decision relevance. Add a verified literature comparison when the result materially agrees with, reverses, or qualifies an existing conclusion. Use continuous scholarly prose by default; do not mechanically repeat labeled paragraphs after every result.
10. Put full proofs in the appendix by default when that protects the economic narrative, while retaining the key derivation or proof logic in the main text when readers need it to understand the mechanism. Mark formal results as new, adapted, specialized, or inherited when provenance matters, and cite the source directly for a reused result. Use inline proofs when the user or target format prefers them. Never replace proof with intuition.
11. Generate figures and tables from the final formulas or data. Explain each visual's objects, feasible regions or comparison baselines, optimum, and economic use in the surrounding text. Map every panel, boundary, slope, jump, plateau, and no-trade region to the proposition or corollary that establishes it. When figures represent paired environments, explain the cross-figure comparison explicitly rather than leaving readers to infer it. Use comparison tables when conditions, instruments, policies, decision owners, or equilibrium strategies repeat across regimes. State whether a visual is analytical, numerical, illustrative, or empirical; never use it as proof.
12. Use extensions to test whether the headline mechanism survives removal of a component, heterogeneity, imperfect discipline, alternative distributions, or another consequential relaxation. Also test whether an extension changes the feasible policy, preferred instrument, or allocation of decision rights. When closed-form joint optimization is unavailable, state the analytical frontier, explain the source of intractability, solve every relevant regime and boundary computationally, and distinguish numerical characterization from proof. State the proof obligation, mechanism verdict, and institutional-scope implication.
13. Reuse the user's existing LaTeX source and style assets when supplied. Otherwise start from `assets/theory-paper-template.tex` and adapt minimally.
14. Compile the LaTeX project, resolve errors and meaningful warnings, rerun bibliography and cross-references as needed, and inspect the rendered PDF page by page. Use the PDF workflow when available.
15. Run the release checklist and a final claim-trace audit. Deliver only files that agree on notation, proposition numbering, citations, figures, and conclusions.


## Mandatory proposition-to-architecture reconstruction

When restructuring an existing theory paper, do not treat the manuscript's current model hierarchy as fixed. Run the reconstruction protocol in `references/model-promotion-and-paper-reconstruction-protocol.md`.

The required sequence is:

`proposition-level novelty audit -> headline-result identification -> main-model promotion/demotion -> paper restructuring`.

### Result hierarchy

Classify verified results as:

- `Headline`;
- `Core mechanism lemma`;
- `Equilibrium consequence`;
- `Benchmark`;
- `Design implication`;
- `Extension`;
- `Robustness`;
- `Appendix`;
- `Merge / Delete`.

Do not give equal narrative weight to every proposition. Prefer a paper with two to four headline results and a visible dependency chain.

### Main-model promotion rule

Promote a benchmark, extension, or robustness model to the main model when it is the first model that directly represents the paper's claimed mechanism. This is especially important when the original main model holds the key behavioral object fixed or produces the headline pattern only through entry, funding, participation, or selection.

### Main-model demotion rule

Demote the current main model to benchmark, closed-form specialization, or appendix when it is retained mainly for tractability, closely reproduces prior logic, suppresses the central behavioral response, or is a special case of the mechanism-faithful model.

The main model should be the simplest model that directly contains the core mechanism, not necessarily the model with the cleanest closed form.

### Main-model / closed-form duality

When a richer model carries the mechanism but a simpler model gives useful closed forms, use both:

- **Main model:** mechanism-faithful and behaviorally correct.
- **Closed-form benchmark/specialization:** used for exact thresholds, intuition, figures, and comparative statics.

Do not sacrifice conceptual accuracy to preserve closed-form convenience.

### Conditional-versus-aggregate discipline

Keep conditional operational outcomes separate from extensive-margin and aggregate outcomes. If the prose claims that a policy changes postdecision effort, quality, delivery, service, or execution ability, that conditional object must be endogenous in the main model.

### Benchmark jobs

Every benchmark must isolate a specific familiar force, such as insurance without moral hazard, incentives without financing friction, full information, fixed decision rights, or a nested closest-paper case. A benchmark should establish the familiar intuition that the main mechanism later overturns or qualifies.

### Closest-paper as benchmark design

A close prior paper may be converted from a novelty threat into a theoretically motivated benchmark when its institutional design deliberately removes the focal conflict. Compare what resource, decision right, or state-contingent claim the prior mechanism protects or separates, and then show what changes when the present setting forces those objects to interact.


## Venue calibration

- For MSOM/POM-oriented drafts, make the operational problem, institutional realism, mechanism, comparative statics, and managerial implications visible without weakening analytical rigor.
- For Management Science-oriented drafts, sharpen the broader theoretical conversation and the general decision insight beyond the immediate setting.
- For Operations Research-oriented drafts, emphasize formal novelty, generality, characterization, algorithmic or analytical depth, and proof completeness.
- Treat these as positioning heuristics, not current journal rules. Verify submission requirements from official sources when the user requests venue compliance.

## Writing rules

- Default to polished academic English for journal manuscripts unless the user requests another language.
- Explain each result as `what happens`, `relative to which benchmark`, `why it happens`, `under which conditions`, and `how it changes the focal decision`.
- Separate equilibrium description, formal mechanism, literature distinction, managerial implication, and proof conceptually, but integrate them into natural prose unless separate labels improve navigation.
- Treat the formal results as a cumulative argument rather than isolated findings. State how each result uses, changes, reverses, or contrasts with an earlier result and why the next result is needed. If a comparative static is only a reverse traversal or reparameterization of an earlier policy map, say so instead of presenting it as a new information-design mechanism.
- When a conclusion matches or opposes prior work, name the shared or reversed conclusion, compare the active constraints or marginal trade-offs, and explain why the mechanisms agree or differ. Do not force a literature comparison when no verified close analogue exists.
- Introduce figures before they appear and interpret them afterward. The surrounding prose should tell the reader which formal result each panel displays, how movement along each axis maps into primitives, and what economic consequence the visual adds beyond the proposition statement.
- Give each paragraph one dominant analytical function. Start with the claim, then supply the causal or comparative support; do not make the reader infer the point from algebra.
- Use threshold language qualitatively in the introduction and exactly in propositions and the analysis. Do not overload the opening pages with formulas.
- Preserve meaningful tension: when a parameter has opposing direct and strategic effects, state both before reporting the net equilibrium effect.
- For information design, explain the causal chain as `state/prior -> posterior experiment -> receiver action -> sender payoff`; do not describe disclosure as merely “more” or “less” information when the active result is belief management or action matching.
- When several levers interact, state whether substitution or complementarity refers to local marginal responses, a discrete regime switch, or the globally optimal policy path.
- For a headline proposition, provide the mathematical trade-off, the economic mechanism, and a distinct behavioral interpretation when each adds information. Anticipate and answer the strongest plausible objection to a new instrument or mechanism.
- Treat `optimal`, `preferred`, `dominates`, and `win-win` as audited terms. Name the objective, selection criterion, stakeholders, and parameter scope supporting them.
- Use the strongest accurate claim, not the strongest rhetorically attractive claim.
- Keep notation stable and define each symbol before use.
- Avoid repetitive proposition summaries, mechanical `what/why/managerial implication` headings, generic transitions, unsupported institutional facts, and invented citations.
- Preserve author choices and existing valid content when revising; provide a change map for structural rewrites.


## Narrative continuity, model narration, and analytical-depth standard

Apply these requirements whenever building or structurally reconstructing a theory working paper.

### Heading-independence test
- Section and subsection headings are navigation aids, not substitutes for argument.
- A reader who temporarily ignores the headings should still be able to follow why each paragraph and result follows from the previous one.
- Insert substantive transition paragraphs at major analytical turns. A transition should state what the previous result establishes, what remains unresolved, and why the next model/result is needed.
- Do not stack `heading -> formula -> proposition -> new heading` without prose that closes one analytical question and opens the next.

### Model section: narrative first, formulas second
- Introduce the institutional setting, actors, timing, decisions, information, and economic friction in prose before presenting notation.
- For every consequential primitive or assumption, provide: (i) its real-world interpretation, (ii) the institutional observation or verified literature that supports using it, (iii) the modeling role it plays, and (iv) what would change if it were relaxed.
- Do not let the Model section read like a notation dictionary. Equations should formalize an already explained economic object.
- When a reduced-form primitive compresses several real objects, explain that compression explicitly and identify which comparative statics inherit that interpretation.
- Prefer a complete verbal event timeline before a formal timeline or payoff system.

### Main-text analytical depth
- Main analysis must contain more than theorem statements and proof-adjacent algebra. Before each headline result, motivate the unresolved economic question and identify the competing forces.
- After a headline proposition, normally provide enough prose to cover: the equilibrium content, the causal mechanism, the comparison to the relevant benchmark or predecessor, the role of binding constraints/boundaries, and the managerial/empirical implication.
- Use one to three substantive follow-up paragraphs as needed; do not force a fixed template when a continuous argument reads better.
- Explain why a threshold exists before emphasizing its closed form. Explain why a comparative static can reverse before reporting the derivative sign.
- When two results share a parameter but arise from different mechanisms, explicitly separate those mechanisms rather than relying on different subsection titles.
- Keep proof details in the appendix when they interrupt the economic narrative, but retain the key inequality, envelope argument, or binding-constraint logic required to understand the result.

### Bridge-paragraph protocol
At the end of each major subsection, write a short bridge that answers:
1. What did this subsection establish?
2. Which maintained assumption or missing mechanism limits that result?
3. What question does the next subsection answer?

Do not use generic transitions such as "We next consider..." unless the analytical dependency has already been stated.

### Main-text thickness gate
Before release, flag a manuscript as narratively underdeveloped if any headline result is supported mainly by a title, displayed equation, proposition, and a single short interpretation paragraph. Expand the economic argument before adding more propositions.

### Reality-and-literature anchoring rule
Institutional claims and model justifications must be source-backed when they are externally verifiable. Use literature to justify modeling choices, not merely to decorate the introduction. Never invent an institutional fact to rationalize a convenient assumption.


## Re-entry rules

Return to `om-theory-model-auditor` when drafting reveals a new result, changed assumption, missing equilibrium region, altered threshold, or proof gap. Return to `om-literature-positioning` when the mechanism, headline result, target conversation, or closest-paper set changes materially.

## Deliverables

When requested, deliver:

- a complete `.tex` manuscript and bibliography;
- a compiled, visually inspected PDF;
- source files for figures and tables;
- appendices containing proofs, notation, robustness, and computational details;
- a compact change map and unresolved-item list;
- for structural rewrites, a promotion/demotion map showing which existing results became headlines, mechanism lemmas, benchmarks, extensions, appendices, or were merged/deleted;
- the final claim ledger and citation-verification status.
- when relevant, the policy-instrument-decision-rights map and stakeholder outcome ledger.
- when relevant, the information-design contract, preference-alignment map, benchmark portfolio, formal-result provenance ledger, and analytical-versus-numerical status map.

Do not label a manuscript submission-ready while critical proof, citation, compilation, or consistency issues remain.
