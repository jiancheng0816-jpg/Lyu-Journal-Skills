---
name: om-journal-calibrator
description: Use only for explicit journal/venue decisions after the OM research core is stable: e.g., 投哪个期刊、MS还是M&SOM/POM/OR/Marketing Science/ISR、venue routing、department ownership、desk-reject risk、投稿前审计、submission audit. Do not implicitly invoke for ordinary model checking, literature review, paper restructuring, reviewer responses, or general publication-potential discussion unless the user explicitly asks for journal selection/calibration.
---

# OM Journal Calibrator

# Invocation policy

This skill is intentionally **manual / conservative**. Do not auto-trigger it from generic phrases such as “发表潜力”, “顶刊标准”, “论文评价”, or “适合发表吗”. Invoke it only when the user explicitly asks for one or more of:

- 投哪个期刊 / 期刊选择 / journal selection;
- MS vs. M&SOM vs. POM vs. OR vs. Marketing Science vs. ISR;
- venue routing / department ownership;
- desk-reject risk by venue;
- target-journal contribution calibration;
- pre-submission / submission audit.

When journal calibration is requested together with model verification, novelty audit, or reconstruction, run the research-core task first and calibrate only after those gates are stable.

## Purpose

This skill is the **journal-calibration and venue-routing layer** for rigorous analytical OM / quantitative-management research.

It should normally run **after** the research core has established that the paper is mathematically correct, substantively novel, and organized as a coherent working paper.

Recommended research-core sequence:

1. `om-theory-model-auditor` → Is the model and derivation correct?
2. `om-literature-positioning` → Is the contribution genuinely new relative to the closest literature?
3. `om-working-paper-builder` → Can the verified results be organized into a coherent paper?
4. `om-journal-calibrator` → Which journal/department owns the paper, and how should it be calibrated for submission?

Do **not** use this skill to replace proof checking, equilibrium verification, novelty red-teaming, closest-paper comparisons, or full-paper reconstruction.

---

## Core questions

The calibrator answers four questions:

1. **Venue routing:** Which of MS, M&SOM, POM, OR, Marketing Science, and ISR is the best structural fit?
2. **Department/area ownership:** Which department, area, or scholarly audience should clearly “own” the paper?
3. **Contribution-bar calibration:** What type of contribution must be foregrounded for that venue?
4. **Pre-submission audit:** What venue-specific risks, policies, and live submission rules must be checked before submission?

---

## Required inputs

Use the latest available paper version or a sufficiently detailed model/result summary.

At minimum identify:

- research question and institutional setting;
- decision makers and timing;
- core primitives and strategic/operational mechanism;
- benchmark(s);
- 2–4 headline results;
- closest literature and novelty claim;
- method type (analytical model, optimization, stochastic model, empirical IO, structural, causal empirical, behavioral, design science);
- intended journal(s), if any.

If a research-core audit already exists, inherit its verified findings instead of recomputing them.

---

# Stage 1 — Research-core gate

Before venue calibration, verify that the paper is ready to be calibrated.

## Gate A: correctness status

Accept the paper for venue calibration only if the latest model audit says the core results are verified or conditionally verified under clearly stated assumptions.

If a headline result is mathematically unresolved, label it:
- `UNVERIFIED — venue calibration provisional`.

Do not improve journal fit by hiding unresolved mathematics.

## Gate B: novelty status

Use the latest novelty audit to classify each major result as:

- `Headline`
- `Mechanism`
- `Robustness / Extension`
- `Delete / Merge`

Do not promote a result to “headline” merely because a target journal values that type of result.

## Gate C: paper architecture

Check that the main analytical sequence is intelligible:

`Primitive / assumption → lemma / equilibrium structure → proposition → mechanism → managerial/economic implication`

Journal calibration may change emphasis and ordering, but must not distort the logical dependency of the model.

---

# Stage 2 — Venue routing

Evaluate all six venues unless the user explicitly limits the candidate set.

Do **not** assign a numerical score. Use structured fit diagnostics instead.

For each venue report:

- **Ownership test**
- **Contribution-bar test**
- **Main strength**
- **Main mismatch**
- **Desk-reject risk**
- **What must change in framing**
- **Re-route logic**

Then identify the most structurally compatible venue(s) without presenting a ranked league table.

---

# Stage 3 — Venue-specific profiles

## A. Management Science (MS)

### Ownership test
Ask:

> Which Management Science department clearly owns this paper?

Map:
`phenomenon → primary decision problem → mechanism → literature → department`.

A paper that cannot identify a plausible department is not ready for MS calibration.

### Contribution bar
The contribution should be a **generalizable management/economic insight**, not only a context-specific observation or a technically correct comparative static.

Analytical work should have:
- correct non-trivial results;
- a mechanism that travels beyond the immediate setting;
- defensible assumptions;
- clear managerial/economic significance.

### Calibration priorities
- make the general management question visible early;
- write for a broad quantitative-management readership;
- signal the target department in framing and literature positioning;
- compare with recent work from the target MS department;
- move long derivations and secondary robustness to the electronic companion.

### Key desk-reject risks
- wrong department;
- niche application with no general insight;
- correct but managerially uninteresting model;
- unrealistic assumptions with no defense;
- method paper with no management payoff.

### Diagnostic
`MS ownership = department clarity + generalizable mechanism + broad management relevance`.

---

## B. Manufacturing & Service Operations Management (M&SOM)

### Ownership test
Ask:

> Is the operational mechanism central rather than incidental?

### Operational Centrality Test

Evaluate:

1. **Operational primitive:** Are key primitives operational (capacity, inventory, production timing, service, fulfillment, sourcing, supply chain, demand learning, revenue management, etc.)?
2. **Operational mechanism:** Does the core result depend on an operations-specific tradeoff?
3. **Operational decision consequence:** Does the headline result change an operational decision or performance outcome?
4. **Context-removal test:** If the OM context were replaced by a generic market/game setting, would the main theory remain essentially unchanged?

If the context-removal test is “yes,” M&SOM fit is weakened.

### Contribution bar
A rigorous model or empirical design must **advance OM understanding**. Technical novelty alone is insufficient.

### Calibration priorities
- lead with the operations problem;
- articulate the operational mechanism before the mathematics;
- interpret effects using operational outcomes;
- connect propositions to operational decisions and OM theory;
- keep assumptions operationally defensible.

### Key desk-reject risks
- OM is only a setting or label;
- technically sound model without operational insight;
- implausible operational assumptions;
- pure OR methodology with no OM payoff;
- broad-management story better suited to MS.

### Diagnostic
`M&SOM ownership = operational centrality + rigorous OM mechanism + generalizable operational insight`.

---

## C. Production and Operations Management (POM)

### Ownership test
Ask:

> Is this an important OM problem for the broad POMS community, including OM-interface questions?

### Contribution bar
POM is methods-broad. The paper should combine:
- an important operations problem;
- rigorous analytical or empirical work;
- generalizable operations insight.

POM is especially plausible for:
- sustainability operations;
- healthcare/service operations;
- broad supply-chain problems;
- OM–marketing, OM–finance, and OM–IS interfaces.

### Calibration priorities
- frame for a broad OM readership;
- make the operations contribution explicit even in interface work;
- show both theory and practice relevance;
- identify the appropriate POM area/section where relevant.

### Key desk-reject risks
- non-OM paper framed as operations;
- descriptive/atheoretical contribution;
- pure methodology without OM payoff;
- model result with weak managerial interpretation.

### Diagnostic
`POM ownership = important broad OM phenomenon + rigorous contribution + clear OM/interface payoff`.

---

## D. Operations Research (OR)

### Ownership test
Ask:

> What is the genuine methodological or theoretical advance?

### OR Contribution Gate

At least one core contribution should plausibly be:

- a new model/framework with methodological significance;
- a new structural theorem/result;
- a new optimization/stochastic/control result;
- a new algorithm with rigorous analysis;
- a new theoretical mechanism that advances OR methodology.

Managerial insight alone does not satisfy the OR bar.

### Contribution bar
Depth, correctness, and theoretical significance are central.

For algorithmic work, require where relevant:
- convergence or complexity analysis;
- provable guarantees;
- computational evidence supporting rather than substituting for theory.

### Calibration priorities
- state the methodological gap precisely;
- elevate the theorem/structural contribution;
- make assumptions explicit and discuss necessity;
- position against OR methodology, not only application-area literature;
- keep notation and theorem dependencies rigorous.

### Key desk-reject risks
- known method applied to a new context;
- incremental extension with trivial structural results;
- computational benchmarking without theory;
- managerially interesting OM result with no OR advance.

### Diagnostic
`OR ownership = methodological novelty + rigorous structural contribution + problem significance`.

---

## E. Marketing Science

### Ownership test
Ask:

> What non-obvious marketing or market mechanism does the model reveal?

### Non-obviousness Test

For every proposed headline result ask:

> Would a knowledgeable researcher expect this result without solving the model?

If yes, the result should normally be demoted unless the model reveals a surprising mechanism, boundary, or strategic reversal.

### Contribution bar
Analytical papers should offer:
- clean formal modeling;
- correct derivations/proofs;
- non-trivial strategic implications for pricing, advertising, targeting, product design, channels, platforms, competition, or consumer/firm interaction.

The model should teach something that intuition or prior models did not already imply.

For structural/empirical work, require credible identification, attention to endogeneity, validation, and meaningful counterfactuals.

### Calibration priorities
- foreground the strategic/market question;
- position against recent quantitative-marketing literature;
- emphasize strategic reversals, valuation crossings, endogenous targeting/pricing, market-design effects, or non-obvious comparative statics;
- make marketing interpretation follow directly from formal results.

### Key desk-reject risks
- mechanical analytical result;
- formal model with no marketing-strategy payoff;
- unaddressed endogeneity / unidentified structural parameters;
- model that is really OM, economics, or generic management with marketing labels.

### Diagnostic
`Marketing Science ownership = non-obvious market mechanism + quantitative-marketing relevance + formal/identification rigor`.

---

## F. Information Systems Research (ISR)

### Ownership test
Ask:

> What is intrinsically information-systems about the mechanism?

### IS Phenomenon Test

Check whether the main mechanism depends materially on one or more of:

- digital artifact / IT-enabled capability;
- information system architecture;
- platform/data infrastructure;
- digital information rights or access rights;
- algorithm/recommendation/automation as an IS artifact;
- IT-enabled organizational or market interaction.

Then run the removal test:

> If the digital/IS artifact is removed, does the central mechanism still survive essentially unchanged?

If yes, ISR fit is weakened.

### Contribution bar
Technical sophistication is not sufficient. The paper must make an **IS theoretical contribution**.

Analytical work requires correct non-trivial results plus a genuine IS insight.

### Calibration priorities
- frame the IS phenomenon and artifact explicitly;
- explain why the mechanism is not merely economics/marketing/OM in digital clothing;
- articulate IS boundary conditions;
- position against ISR/quantitative IS literature;
- interpret results as IS theory, not predictive accuracy alone.

### Key desk-reject risks
- analytics/ML application without IS theory;
- generic economics or marketing model relabeled as digital;
- correct analytical model with no IS insight;
- empirical endogeneity without credible identification.

### Diagnostic
`ISR ownership = intrinsic IS artifact/mechanism + IS theoretical contribution + quantitative rigor`.

---

# Stage 4 — Cross-venue discrimination tests

Use these when two or more venues remain plausible.

## MS vs M&SOM

Choose the framing direction by asking:

- Is the main contribution a **general management/economic mechanism** that travels across contexts? → MS direction.
- Is the mechanism specifically **operational** and advances OM theory/practice? → M&SOM direction.

## M&SOM vs POM

- Analytical OM mechanism with strong INFORMS-style theory emphasis → M&SOM direction.
- Broad OM, interface, sustainability, healthcare, or mixed-method appeal → POM direction.

## MS vs OR

- Generalizable managerial/economic insight is the main contribution → MS direction.
- Methodological/theoretical advance is the main contribution → OR direction.

## MS vs Marketing Science

- Broad management question owned by an MS department → MS direction.
- Core theory is specifically about marketing strategy / consumer-market interaction and non-obvious quantitative-marketing mechanism → Marketing Science direction.

## MS vs ISR

- General quantitative-management insight with IS as one setting → MS direction.
- Mechanism fundamentally relies on IS artifacts, digital rights, digital architecture, or IT-enabled behavior → ISR direction.

## Marketing Science vs ISR

Ask what breaks if the data/platform/algorithm layer is removed:

- If the core mechanism is still fundamentally about pricing/advertising/targeting/consumer-market interaction → Marketing Science direction.
- If the mechanism is fundamentally about digital information rights, system architecture, recommendation/algorithmic artifacts, or IT-enabled interaction → ISR direction.

---

# Stage 5 — Contribution-bar calibration

For the selected venue, rewrite the contribution hierarchy without changing the underlying verified results.

For each headline result produce:

### Result
What is formally established?

### Mechanism
Why does it occur?

### Journal-specific significance
Why does this matter **for the target venue's intellectual audience**?

### Boundary
Under what assumptions/regimes does it hold?

### Closest-literature contrast
What does this result add beyond the nearest paper(s)?

### Required framing change
What wording, ordering, or interpretation should change for the target venue?

Do not invent stronger novelty than the prior novelty audit supports.

---

# Stage 6 — Desk-reject red-team

For the target venue, identify the **single most likely desk-reject reason** first.

Then audit:

- topic/department/area mismatch;
- contribution too narrow;
- mechanism too obvious;
- technical depth below venue bar;
- assumptions not defensible for the venue;
- paper framed in the wrong literature;
- context not central to the theoretical mechanism;
- paper is actually owned by another field;
- insufficient broad relevance;
- proofs/identification unresolved;
- excessive mathematical detail in the main text;
- headline result actually only an extension.

Use concrete paper-specific evidence rather than generic warnings.

---

# Stage 7 — Pre-submission live audit

Before declaring a manuscript submission-ready, **re-check current official journal sources**.

Verify, as applicable:

- current journal scope;
- current departments / areas / editors;
- submission system;
- abstract/length requirements;
- anonymization / double-blind rules;
- manuscript and reference style;
- LaTeX/style-file requirements;
- electronic companion / online appendix policies;
- data/code/replication/open-science requirements;
- disclosure/ethics/AI-use requirements;
- special issue / department-specific constraints.

If current official instructions conflict with this skill, the official instructions control.

Never rely on remembered submission rules when preparing final submission advice.

---

# Output format

Use this structure by default.

## 1. Paper identity
- Research question:
- Core mechanism:
- Verified headline results:
- Closest-literature novelty:

## 2. Venue diagnostics

### Management Science
- Ownership:
- Contribution-bar fit:
- Main mismatch:
- Desk-reject risk:
- Required reframing:

### M&SOM
- Ownership:
- Contribution-bar fit:
- Main mismatch:
- Desk-reject risk:
- Required reframing:

### POM
- Ownership:
- Contribution-bar fit:
- Main mismatch:
- Desk-reject risk:
- Required reframing:

### Operations Research
- Ownership:
- Contribution-bar fit:
- Main mismatch:
- Desk-reject risk:
- Required reframing:

### Marketing Science
- Ownership:
- Contribution-bar fit:
- Main mismatch:
- Desk-reject risk:
- Required reframing:

### ISR
- Ownership:
- Contribution-bar fit:
- Main mismatch:
- Desk-reject risk:
- Required reframing:

## 3. Structural venue conclusion
State:
- the venue(s) whose intellectual ownership is strongest;
- why the paper belongs there;
- the main alternative route;
- what would have to change for the alternative venue to become plausible.

Do not use numerical scores or cosmetic rankings.

## 4. Target-journal calibration
- Target department/area:
- Target audience:
- Contribution language:
- Headline result order:
- What to move to appendix:
- Literature set to emphasize:
- Main desk-reject risk:
- Required revision before submission:

## 5. Pre-submission audit
- Official sources checked:
- Current formatting/blinding requirements:
- EC/appendix policy:
- Data/code/open-science policy:
- Any current policy conflicts or uncertainties:

---

# Integration rule

This skill must remain distinct from the research core:

- `om-theory-model-auditor` owns correctness.
- `om-literature-positioning` owns novelty and closest-paper comparison.
- `om-working-paper-builder` owns paper architecture and the lemma → proposition → mechanism → implication narrative.
- `om-journal-calibrator` owns venue routing, department/area ownership, journal-specific contribution calibration, desk-reject red-teaming, and live pre-submission checks.

When a conflict arises:
1. mathematical truth overrides venue preference;
2. novelty evidence overrides framing ambition;
3. journal calibration may change emphasis, not the underlying verified result;
4. current official journal instructions override stored submission rules.
