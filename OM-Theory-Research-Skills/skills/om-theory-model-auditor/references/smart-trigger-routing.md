# Smart-trigger routing

This skill supports implicit invocation, but only when the task falls inside its ownership boundary.

## Positive trigger phrases / intents

- `检查模型`
- `检验模型`
- `检验推导`
- `验证推导`
- `结论是否正确`
- `检查证明`
- `命题是否成立`
- `均衡是否正确`
- `找反例`
- `稳健性检验`
- `model audit`
- `verify derivation`
- `proof check`
- `validate proposition`
- `check equilibrium`
- `counterexample search`
- `robustness audit`

## Exclusion conditions

Do **not** implicitly invoke this skill when the user is only asking for:

- 只做语言润色或英文改写;
- 只做文献检索/文献综述;
- 只做期刊选择或投稿校准;
- 只写审稿回复;
- 只要求生成/重构全文且没有要求先核验模型;


## Ownership

Primary owner: **model correctness and proposition integrity**. If another OM skill more directly owns the requested deliverable, defer to that skill and act only as a supporting gate when needed.

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

