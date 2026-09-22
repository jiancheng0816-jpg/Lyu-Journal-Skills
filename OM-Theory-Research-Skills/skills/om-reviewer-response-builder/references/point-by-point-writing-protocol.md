# Point-by-point writing protocol

## 1. Letter architecture

Use this hierarchy when the review package contains all roles:

1. title identifying the manuscript and revision round;
2. response to the editor or department editor;
3. concise summary of major structural changes;
4. response to the associate editor;
5. separate response to each reviewer;
6. references or supplementary evidence used only in the response package.

Retype each comment verbatim in the final response unless journal instructions or the user specify otherwise. Visually distinguish comments and responses consistently; color is optional and must not be the only distinguishing device.

## 2. Editor-facing major-revision summary

Use three to five bullets organized by decision significance. Each bullet should state:

- the problem exposed by the review team;
- the structural action taken;
- the resulting change in model, results, or contribution;
- the main manuscript location.

Do not list every small edit. Do not claim improvement without identifying what changed.

For a later round, summarize only changes since the immediately preceding version. Lead with the remaining editorial hurdle and explain how the current revision closes it. Do not reproduce the full first-round change list unless the editor explicitly asks for a cumulative history.

## 3. Anatomy of a substantive response

Use the following order flexibly:

1. **Acknowledge the issue:** one sentence identifying why the concern matters.
2. **Lead with the disposition:** “We removed…,” “We revised the base model…,” “We agree in part…,” or “We retain this assumption because…”.
3. **Explain the scientific reasoning:** show the information structure, derivation, comparison, institutional evidence, or scope logic.
4. **State the verified finding:** explain what changes and what does not.
5. **Identify the manuscript action and location.**
6. **Calibrate the remaining boundary:** state any limitation or implementation requirement.

Lead with action. A reviewer should not need to read several paragraphs before learning whether the manuscript changed.

## 4. Response patterns

### Accept and remove

Use when the challenged element is infeasible, redundant, or weakly motivated:

> We agree that the mechanism is inconsistent with the platform's information structure. We therefore removed it and now focus on [coherent alternatives]. This change does not eliminate the central comparison because [reason].

Explain the consequence of removal; do not present deletion as self-justifying.

### Clarify a proposed mechanism

State explicitly that the mechanism is proposed rather than observed. Identify who sets each parameter, what is publicly observable, how commitment is enforced, and which implementation costs are outside the model. Use `may`, `can under`, or `provides a rationale` rather than `should implement` unless implementation evidence is strong.

### Defend a stylized assumption

Give the assumption's economic and mathematical roles. Then show one of the following:

- the omitted force is inactive in the baseline equilibrium;
- a targeted extension activates it but preserves the mechanism;
- relaxing it changes a boundary but not the headline result;
- relaxing it overturns the result, requiring a narrower claim.

Saying only that stylized models require assumptions is not a sufficient defense.

### Address an omitted mechanism

If the reviewer raises refunds, moral hazard, production failure, search, competition, or another omitted force:

1. write the affected payoff or constraint;
2. identify the regime in which it binds;
3. explain why it is inactive or consequential in the base case;
4. use an extension or model revision if it can change the result;
5. narrow the manuscript claim accordingly.

### Answer a contribution objection

Name the closest paper or stream and compare mechanisms, not titles. State what is inherited, what decision or instrument is new, what result changes, and whether the earlier model is recovered under an exact restriction. Avoid declaring novelty from a different application context alone.

When one closest paper controls the decision, use a compact side-by-side table of conditions, decision rights, active instruments, equilibrium strategies, signaling cost, and stakeholder outcomes. Then explain why apparently similar choices are or are not the same mechanism. Read [closest-paper-and-welfare-protocol.md](closest-paper-and-welfare-protocol.md).

### Correct a welfare overclaim

If the earlier manuscript treated separation as consumer welfare, acknowledge the distinction and replace the claim. Provide the full-information benchmark, define consumer surplus, and state whether the policy improves information, surplus, participation, or efficiency. These are not interchangeable.

### Reorganize an overgrown analysis

If a correct comparative-static result is too complex to interpret, keep the managerial pattern, switching condition, or finite candidate set in the main paper and move the exhaustive case structure to the appendix. Explain what decision becomes easier because of the condensed result.

### Rename ambiguous constructs

Prefer names that reveal the economic choice and owner: `mandatory` versus `voluntary`, `platform-determined` versus `creator-determined`, and `private information` versus `hidden action` when that is the actual distinction. Apply a global terminology audit across text, equations, figures, tables, captions, appendices, supplements, and the response letter.

### Partially accept or disagree

Separate agreement from disagreement:

> We agree that [valid concern]. We therefore [change]. We do not adopt [requested remedy], because [verified reason]. Instead, [alternative action] addresses the underlying issue while preserving [scope or validity].

Never attribute motives to the reviewer. Do not use authority or preference as the sole reason.

## 5. Analytical explanation standard

When a response contains a new or revised result, include enough information to verify:

- changed primitives or constraints;
- affected equilibrium candidates;
- selection or refinement rule;
- parameter region;
- economic mechanism;
- relation to the original result.
- relation to the prior-round claim and the closest benchmark, when applicable.

If the full proof is in an appendix or supplement, summarize the decisive inequality or deviation in the response. For complex comparative statics, report the shape, switching logic, and economic cause rather than only saying a sensitivity analysis was added.

## 6. Location and quotation discipline

- Use sections before pagination stabilizes.
- Add page and line numbers only after the final response-version PDF exists.
- Verify every location against that version.
- Quote only the sentence or short paragraph needed to show the revision.
- Do not substitute a long manuscript quotation for an explanation of why the change resolves the concern.

## 7. Tone and claims

Prefer precise verbs: `removed`, `reformulated`, `derived`, `verified`, `restricted`, `repositioned`, `clarified`, and `added`.

Avoid:

- repeated ceremonial thanks;
- “the reviewer misunderstood”;
- “obviously” or “clearly” when the point was disputed;
- “fully addressed” without audit evidence;
- “robust” without identifying dimensions and exceptions;
- “win-win,” “dominates,” or “optimal” without stakeholder objectives and regions;
- implementation prescriptions from an unvalidated stylized mechanism.
- claiming a policy protects consumers merely because it expands the separating region.

The best tone is calm, specific, and evidence-led.
