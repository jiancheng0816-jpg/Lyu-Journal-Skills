# Smart-trigger routing

This skill supports implicit invocation, but only when the task falls inside its ownership boundary.

## Positive trigger phrases / intents

- `审稿意见`
- `回复审稿人`
- `审稿回复`
- `response letter`
- `rebuttal`
- `revision memo`
- `R&R`
- `第二轮审稿`
- `多轮审稿`
- `point-by-point response`
- `reviewer comments`
- `editor comments`

## Exclusion conditions

Do **not** implicitly invoke this skill when the user is only asking for:

- 普通论文评价但没有审稿意见;
- 纯模型审计;
- 纯文献定位;
- 投稿期刊选择;
- 一般全文重构但没有review package;


## Ownership

Primary owner: **reviewer-response strategy and traceable revision closure**. If another OM skill more directly owns the requested deliverable, defer to that skill and act only as a supporting gate when needed.

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

