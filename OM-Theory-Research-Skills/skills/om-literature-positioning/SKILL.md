---
name: om-literature-positioning
description: Position analytical OM, management-science, IS, and quantitative-marketing research against verified closest literature using mechanism-level comparisons. Implicitly trigger for 文献定位、查找相关文献、closest paper、novelty comparison、贡献比较、与某篇文章相比、是否重复、研究缺口、literature positioning, related-work comparison, citation verification, or requests to assess whether a theory idea is incremental. Do not trigger for model-proof verification, prose-only polishing, reviewer-response drafting, or journal selection when no literature/novelty comparison is requested.
---

# OM Literature Positioning

Identify the nearest intellectual neighbors and define the paper's contribution without exaggeration. Compare mechanisms and decision structures, not only keywords or application settings.


# Smart-trigger routing

This skill supports implicit invocation, but only when the task falls inside its ownership boundary.

## Positive trigger phrases / intents

- `文献定位`
- `查找相关文献`
- `最接近文献`
- `closest paper`
- `novelty comparison`
- `贡献比较`
- `与XX比较`
- `是否重复`
- `研究缺口`
- `文献综述`
- `literature positioning`
- `related work`
- `citation verification`
- `incremental or novel`

## Exclusion conditions

Do **not** implicitly invoke this skill when the user is only asking for:

- 只检查公式、证明或均衡;
- 只做语言润色;
- 只写审稿回复且不需要新增文献;
- 只问投哪个期刊且不要求文献定位;


## Ownership

Primary owner: **closest-literature search and novelty substantiation**. If another OM skill more directly owns the requested deliverable, defer to that skill and act only as a supporting gate when needed.

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

## Required inputs

Request or reconstruct:

- the research question and intended unit of analysis;
- players, timing, information, decisions, frictions, and equilibrium outcomes;
- headline results and their verified conditions;
- target conversation or journals, if any;
- seed papers, existing bibliography, Zotero collection, and desired search cutoff.

If the model is still changing, label the positioning provisional and identify which changes would invalidate it.

## Workflow

1. Read `references/search-and-verification-protocol.md` before searching and `references/literature-writing-protocol.md` before drafting literature or contribution prose. For forecasting, information sharing, cheap talk, signaling, screening, Bayesian persuasion, disclosure, or data-acquisition papers, also read `references/information-design-positioning.md`.
2. Convert the paper into a mechanism signature: setting, actors, decision ownership, policy adoption and intensity, available instruments, information lifecycle, commitment and experiment set, operational friction, strategic interaction, equilibrium object, stakeholder outcomes, and headline comparative static.
3. Generate search families for: exact mechanism, closest decision problem, theoretical foundation, institutional application, alternative mechanism producing a similar result, and recent papers citing key seeds.
4. Search the user's Zotero library first when the Zotero connection is available. If it is unavailable, ask for a relevant collection export or `.bib` file when personal-library coverage matters.
5. Search current scholarly sources and authoritative metadata. Use connected academic-search tools when available and web browsing otherwise. Prefer publisher pages, DOI/Crossref records, journal pages, working-paper repositories, and author-hosted manuscripts.
6. Maintain a candidate ledger with title, authors, year, outlet, DOI or stable URL, evidence level, search family, and reason for inclusion. Deduplicate by DOI and normalized title.
7. Triage candidates in two passes: screen metadata and abstracts broadly, then inspect the strongest nearest neighbors deeply. Do not infer a paper's model or result from its title alone.
8. Build the comparison matrix in `references/contribution-matrix-template.md`. Rank papers by structural proximity, not prestige or citation count. Give special attention to papers with the same endogenous instruments but a different active mechanism, the same policy with a different decision owner, or the same information-design method with a different receiver action, preference geometry, experiment set, or interaction with monetary levers.
9. Identify the strongest overlap, the exact structural difference, the changed payoff, constraint, information technology, or preference geometry, why that change alters the equilibrium or managerial problem, and which verified result depends on it. For every material result-level comparison, state whether the focal conclusion agrees with, reverses, or qualifies the prior conclusion and explain the active mechanism behind that relationship. When the focal paper claims to extend or subsume a closest model, specify and verify the parameter, policy, experiment-set, or decision restriction that recovers it.
10. Draft contribution claims only after the matrix is stable. Organize the review into mechanism-based streams, identify the closest paper within each stream, and end with a cross-stream synthesis. Use calibrated language such as “differs by,” “introduces,” “endogenizes,” or “shows that.” Avoid “first,” “novel,” or “unexplored” unless an explicit, current, reproducible search supports it.
11. Audit every positioning sentence against a source record and an evidence excerpt or precise locator. Mark unsupported statements instead of filling gaps from memory.
12. Deliver a source-backed positioning package and disclose search date, databases or tools, queries, screening limits, and inaccessible full texts.

## Evidence statuses

Assign one status to every source-specific assertion:

- `FULL TEXT CHECKED`: the relevant model, result, or limitation was verified in the paper.
- `ABSTRACT CHECKED`: only abstract-level claims are supported.
- `METADATA ONLY`: existence and bibliographic details are verified, but substantive claims are not.
- `UNVERIFIED`: the source or asserted content could not be confirmed.

Never promote an abstract or search snippet to full-text evidence.

## Contribution test

For each proposed contribution, answer:

1. Relative to which closest paper or stream?
2. What primitive, decision, information structure, or constraint differs?
3. Why does that difference create a new economic mechanism rather than a relabeled setting?
4. Which verified result depends on that mechanism?
5. What managerial or theoretical question becomes answerable only because of it?
6. Does the focal model nest the closest paper? If yes, what restriction recovers its result and where does the new result begin? If not, is the prose calibrated as a nonnested comparison?
7. Is the information contribution about acquisition, credibility, transmission, experiment design, receiver response, or interaction with another lever, and does the wording identify the correct stage?

Classify the contribution as `new mechanism`, `new strategic interaction`, `new endogenous decision`, `new boundary or reversal`, `generalization`, `empirical or institutional application`, or `setting-only`. Flag setting-only contributions as weak unless paired with a consequential mechanism.

## Output package

Produce:

- a one-paragraph positioning verdict;
- the search protocol and candidate ledger;
- a ranked list of closest papers with evidence statuses;
- the mechanism-level contribution matrix;
- a closest-model nesting or nonnesting verdict;
- defensible literature-gap and contribution paragraphs;
- a manuscript-ready stream architecture and cross-stream synthesis aligned with the paper's headline result groups;
- a list of claims that must be softened or removed;
- a BibTeX-ready reference list with unresolved metadata clearly marked;
- recommended additional searches and the conditions that would change the verdict.

Do not draft a full manuscript unless the user separately invokes `om-working-paper-builder`.


## Institutional anchoring and model-justification protocol

Literature positioning must support the model as well as the contribution claim.

### Primitive evidence map
For each consequential modeling primitive, build a compact evidence map with:
- primitive / institutional feature;
- real-world interpretation;
- strongest supporting literature or authoritative institutional source;
- what the source actually establishes;
- what remains a modeling abstraction.

Use this map to strengthen the Model section, not just the Related Literature section.

### Narrative use of literature
- Cite prior work at the point where it motivates an assumption, outside option, decision right, information structure, or pricing institution.
- Distinguish `evidence for the phenomenon` from `precedent for the modeling abstraction`; a paper can support one without supporting the other.
- Do not turn the Model section into a citation catalogue. One or two high-proximity sources are preferable to a long list when the modeling role is the same.
- When institutional facts come from firms, platforms, rate cards, contracts, or policy documents rather than academic papers, verify them from authoritative current sources and label them as institutional evidence.

### Contribution-to-model bridge
The literature review should end each major stream by explaining which unresolved modeling object enters the present model. Avoid a literature section that merely lists differences and then restarts the paper from scratch in the Model section.

### Closest-paper transition rule
When a closest paper becomes a benchmark or extension, state explicitly:
1. which decision right/instrument/information structure is shared;
2. which element is switched off in that paper or benchmark;
3. why restoring the focal element creates the next analytical question.

This bridge should later reappear naturally in the model/analysis rather than only in the novelty table.


## Handoff contract

Pass to `om-working-paper-builder`:

- verified citation metadata and citation keys;
- the closest-paper matrix;
- when relevant, the information-lifecycle and formal-result-provenance matrices;
- approved gap and contribution statements;
- evidence-status labels and inaccessible sources;
- the search date and declared coverage limits.

Do not hand off an unverified novelty superlative as approved prose.
