# Validation notes / 验证说明

These notes are not part of the scoring prompt. / 本文不属于默认评分指令。

## Interpretation / 结果解释

- This is a research aid based on Professor Bin Jiang’s Beautimeter paper and shared GPT instructions, not a validated objective measure of beauty. / 本工具依据教授的论文及其提供的指令实现，用于研究辅助，不是经过验证的客观美度量表。
- Model choice, API routing, image handling, and conversation context may affect results. A model name or relay alias alone does not establish the underlying model snapshot. / 模型、API 路由、图像处理及对话上下文可能影响结果；仅凭模型名称或中转别名不能确认底层模型快照。
- Agreement with the paper, agreement with Alexander’s judgments, and reproducing the original GPT are different evaluation questions. Agreement is not, by itself, proof of objective accuracy. / 与论文一致、与亚历山大原著判断一致、复现原 GPT 是不同的验证问题；一致率本身不等于客观准确率。
- Default output contains only totals. It does not expose evidence that all fifteen internal scores were correctly summed. / 默认只显示总分，无法仅凭输出审计十五项内部计分及求和。

## Evaluation workflow / 验证流程

1. Freeze the skill version, exact prompt, model/version, API route, and original image hashes before testing. / 测试前固定 skill 版本、完整提示词、模型版本、API 路由及原图哈希。
2. Use independent, authorized image pairs that were not used to tune the instructions. Do not send reference scores or expected winners to the model. / 使用有权使用且未参与调试的新图对，不向模型发送参考分数或预期偏向。
3. Prefer a fresh conversation per pair. If conversations are reused, report those results separately. / 优先每组独立对话；复用上下文的结果单独统计。
4. Keep original images unchanged. Randomize image order and map results back to image identities. / 保留原图，随机安排图序，并按图片身份还原结果。
5. Preserve first answers and failed attempts. Report ties, missing scores, coverage, and paired preference agreement with explicit denominators. Do not retry to select more agreeable scores. / 保留首答及失败记录，明确报告平局、缺失、覆盖率和排序一致率的分母，不重试筛选更合意的分数。
6. On a preselected subset, repeat requests and swap image order to assess stability. Keep audit details separate from the default two-total interface. / 在预先选定的子样本上重复调用并交换图序，检查稳定性；审计细节与默认双总分输出分开。

Exploratory run records are retained separately and are not used as reference answers in this skill. / 探索性测试记录单独保留，不作为本 skill 的评分参考答案。
