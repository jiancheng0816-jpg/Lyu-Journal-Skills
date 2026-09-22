---
name: om-reviewer-response-builder
description: Build and audit single- or multi-round revision strategies, response matrices, editor summaries, and point-by-point response letters for analytical operations-management, management-science, information-systems, and quantitative-marketing papers. Use when reviewer comments challenge model validity, assumptions, equilibrium analysis, institutional realism, contribution, literature positioning, stakeholder outcomes, exposition, or implementation; keep every claimed revision traceable across review rounds and to verified manuscript evidence.
---

# OM Reviewer Response Builder

Turn a review package into a scientifically defensible revision and a response letter that makes the logic of that revision easy to verify. Treat the letter as an audit trail between each concern, the authors' disposition, the supporting analysis, and the revised manuscript.

## Choose the mode

- **Triage and revision plan:** diagnose the review package before drafting responses. Read [references/review-triage-and-revision-strategy.md](references/review-triage-and-revision-strategy.md).
- **Later-round or acceptance-oriented revision:** trace prior promises, isolate the remaining hurdle, and prevent scope drift using [references/multi-round-closure-protocol.md](references/multi-round-closure-protocol.md).
- **Response matrix:** build the traceability ledger in [references/response-matrix-template.md](references/response-matrix-template.md).
- **Point-by-point letter:** follow [references/point-by-point-writing-protocol.md](references/point-by-point-writing-protocol.md).
- **Closest-paper, instrument, or welfare challenge:** use [references/closest-paper-and-welfare-protocol.md](references/closest-paper-and-welfare-protocol.md).
- **Final audit:** reconcile the response, manuscript, appendix, supplement, figures, and citations using [references/reconciliation-checklist.md](references/reconciliation-checklist.md).

For a complete revise-and-resubmit package, use triage, the response matrix, point-by-point drafting, and the final audit; add the two specialized protocols when the round history or scientific issue requires them. If the user asks only for diagnosis or a revision plan, do not imply that manuscript changes have been implemented.

## Establish the revision record

Collect, when available:

- decision letter and reports from the editor, associate editor, and each reviewer;
- original and revised manuscripts, appendices, and supplements;
- previous response rounds;
- the manuscript and supplement associated with each previous response round;
- author notes describing actual revisions or nonnegotiable choices;
- target journal and stable page/line numbering.

Assign stable identifiers such as `DE-1`, `AE-2`, `R1-3`, and `R2-4b`. Preserve each original comment verbatim in the final letter unless the user requests a condensed internal matrix. Split a compound comment only when its subparts require distinct decisions or evidence.

For round two or later, maintain an issue genealogy: first round raised, prior disposition, promised change, reviewer assessment in the next round, current residual issue, and present action. Classify each current comment as new, residual, reopened, or execution-only. Do not make the reviewer reconstruct what changed across versions.

Never invent manuscript changes, proofs, computations, citations, institutional facts, editor preferences, or page and line locations. A planned change is not a completed change. Mark unavailable evidence as pending and state what would verify it.

## Diagnose before answering

For every comment, identify both the stated request and the underlying publishability risk. Typical root risks are:

- internal inconsistency or infeasible implementation;
- incorrect equilibrium, proof, comparative static, or welfare claim;
- mismatch between the institutional setting and the model;
- an assumption that mechanically drives the result;
- incremental or inaccurately stated contribution;
- an omitted mechanism that may overturn the headline result;
- excessive scope, weak organization, or unclear exposition.

Also identify the round-specific editorial hurdle. Two reviewers recommending minor revision does not override an editor or associate editor who identifies one unresolved contribution or correctness risk. Separate uncertainty about the **results** from deterministic work on **execution** such as terminology, organization, figures, and exposition.

Synthesize overlapping comments across the review team before choosing actions. Give priority to scientific correctness and the editor's or associate editor's integrative guidance, not to the order in which comments appear.

## Choose a defensible disposition

Use one of these dispositions and record it explicitly in the internal matrix:

- **Accept and revise** when the request improves correctness, realism, identification, or exposition.
- **Remove** when a mechanism, analysis, or claim is internally inconsistent, weakly motivated, duplicative, or not worth defending.
- **Rebuild or promote** when the comment exposes a flaw in the base model or a central contribution.
- **Move to extension or supplement** when an issue matters for scope or robustness but should not obscure the main mechanism.
- **Clarify and bound** when the model already accommodates the concern or the concern does not affect a specified equilibrium region.
- **Partially accept** when the concern is valid but the requested implementation is not the best scientific remedy.
- **Respectfully decline** only after testing the requested change and providing a precise theoretical, empirical, or scope-based reason.

Do not preserve a weak element merely because it required substantial prior work. Conversely, do not add every requested extension; protect the paper's central question and explain why a bounded robustness test is sufficient.

## Require a closed response loop

Each substantive response must close this chain:

1. **Concern:** what risk the reviewer identified.
2. **Disposition:** what the authors did or why they declined.
3. **Evidence:** derivation, model comparison, computation, institutional evidence, literature, or calibrated scope argument.
4. **Manuscript consequence:** exact change to assumptions, model, result, exposition, figure, table, appendix, or claim.
5. **Verified location:** stable section and, only when final, page/line references.
6. **Boundary:** what remains outside the paper and why it does not invalidate the revised claim.
7. **Round linkage:** for later rounds, how this action completes, changes, or supersedes the prior response.

A long answer is not a closed answer if one of these links is missing.

## Handle analytical OM comments

- For a model-validity objection, reconstruct who observes, chooses, commits, enforces, and pays before defending the mechanism.
- For a realism objection, distinguish a practice-motivated mechanism from a newly proposed mechanism. State implementation requirements and use conditional language for unimplemented designs.
- For a strong assumption, identify its economic role, mathematical role, and whether relaxing it changes feasibility, equilibrium form, mechanism, or only algebra.
- For an omitted mechanism, first test whether it is inactive in the baseline region. If so, explain why and show where it becomes active; otherwise revise the model.
- For a contribution objection, compare the closest work at the mechanism level and recover any claimed special case exactly. Do not rely on context alone.
- When a reviewer argues that the result is equivalent to the closest paper, first test that factual premise. Decompose the choices into policy-induced constraints, strategic instruments, and transferred decision rights; then use exact restrictions or counterfactual regions to establish equivalence or difference.
- Distinguish a mechanical change in a variable from using that variable as a strategic signal. Similar equilibrium coordinates do not establish identical mechanisms.
- Define instrument effectiveness before comparing instruments: feasible separation region, signaling cost, equilibrium profit, stakeholder surplus, or another explicit metric.
- Do not equate a larger separating-equilibrium region with higher consumer welfare. Add the relevant full-information benchmark and calculate stakeholder outcomes whenever a welfare claim is made.
- When a policy parameter may be platform- or firm-chosen, justify decision ownership by institutional practice and equilibrium feasibility. Promote the practically relevant ownership structure to the main model; retain an alternative as an appendix step only if it clarifies feasibility or mechanism.
- For a request that would overload the main model, use the minimal extension that tests the threatened mechanism and report both what survives and what changes.
- For equilibrium refinement or selection, explain the profitable deviation and the type for which it is not profitable; do not cite the criterion as a black box.
- Audit terms such as `optimal`, `preferred`, `dominates`, `necessary`, `robust`, and `win-win` against explicit objectives, stakeholders, parameter regions, and selection rules.

When the underlying work requires a fresh model audit, literature search, or manuscript reconstruction, hand off to the applicable OM skill and import only verified results into the response letter.

## Build the letter at two levels

Start with a concise editor-facing summary of the major revisions. Organize it around the few changes that altered the paper's validity, contribution, or scope, not around manuscript sections. Then respond separately to the editor, associate editor, and each reviewer.

In later rounds, summarize only the incremental changes made since the immediately preceding version and explicitly state how they resolve the remaining editorial hurdle. Do not repeat the entire first-round revision story. When the revision is near acceptance, prefer sharper benchmarking, welfare calibration, terminology, organization, and proof completion over adding loosely connected results.

Within each response, lead with the disposition. Use appreciation briefly, then spend the paragraph on the scientific issue. Quote only short revised passages when they materially help verification. Adapt repeated explanations to the recipient's concern; do not paste the same generic block without showing why it answers that comment.

Use professional, non-defensive language. Avoid claiming that every concern is “fully addressed” unless the reconciliation audit supports it. Calibrate proposals from stylized models as potential mechanisms or conditional guidance, not as implementation-ready prescriptions.

## Deliverables

Depending on the request, provide:

- a cross-reviewer issue map and prioritized revision plan;
- a response matrix with status, evidence, manuscript action, and unresolved decisions;
- an editor-facing major-revision summary;
- a complete point-by-point response letter;
- a list of manuscript edits still required before the response can be truthful;
- a final consistency and claim-calibration audit.

Keep scientific decisions visible. If a comment cannot be answered without author judgment, new analysis, new data, or a change in contribution, flag it rather than silently choosing for the author.
