# Task completion and answer quality review / 任务完成与回答质量复查

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

- ID: `task-repro-check`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Reset site original
- Author / 作者: Reset maintainers

## English

Review omissions, errors, and unverified work in Codex tasks or ChatGPT answers.

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/task-repro-check/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=task_repro_check_en)

**Tool / 工具:** 通用

**Input / 输入:** Optional evidence:
[Sources, diffs, or complete logs; remove secrets and personal information first]

**Expected result / 预期结果:** An acceptance table, concrete evidence, minimal corrections, and reproducible checks.

**When to use / 使用时机:** Review omissions, errors, and unverified work in Codex tasks or ChatGPT answers.

**Completion / 完成标准:** An acceptance table, concrete evidence, minimal corrections, and reproducible checks.

### Prompt / 提示词

```text
Review the Codex task or ChatGPT answer below against the original request.

First identify a code/tool task, a question/writing task, or a mixture. Apply only relevant checks. Do not demand Git diffs for ordinary answers or report a test as passed when no execution environment is available.

1. Turn requirements into a checklist. Mark each as met, missing, incorrect, or unverified, with the exact sentence, file location, or log evidence.
2. For code/tool work, inspect changed files and the real user path for omissions, scope drift, tool failures, and premature completion. Report actual command completion, exit status, test totals, and failures.
3. For questions or writing, check relevance, coverage, requested format, and actionable steps. Separate facts, inferences, and advice; identify vague statements and contradictions.
4. Check factual claims against dated primary sources and their scope. Mark missing or inaccessible evidence as unverified. Never invent sources or turn a guess into a fact.
5. If context may interfere, propose a fresh-chat comparison using the same question and material. Change one factor at a time and record differences; one result does not establish product-wide ability.
6. Propose the smallest useful correction and explain how to verify it. Do not weaken assertions, hide failures, or hardcode results to pass a check.
7. Use only material this task authorizes you to access. State permission gaps and unverified items. A test that merely started, has truncated output, or is still running has not passed.

Return a table of requirement / actual result / evidence / status, then prioritized issues, minimal corrections, and repeatable verification steps. Judge this result only; do not invent an intelligence score.

Original request:
[Paste requirements]

AI answer or actual work:
[Paste the result]

Optional evidence:
[Sources, diffs, or complete logs; remove secrets and personal information first]
```

## 中文

复查 Codex 任务或 ChatGPT 回答中的遗漏、错误和未验证事项。

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/task-repro-check/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=task_repro_check_zh)

**Tool / 工具:** 通用

**Input / 输入:** 可选证据：
[相关资料、差异或完整日志；先移除密钥与私人信息]

**Expected result / 预期结果:** 逐项验收表、问题证据、最小修正建议和可复现的检查步骤。

**When to use / 使用时机:** 复查 Codex 任务或 ChatGPT 回答中的遗漏、错误和未验证事项。

**Completion / 完成标准:** 逐项验收表、问题证据、最小修正建议和可复现的检查步骤。

### Prompt / 提示词

```text
请复核下面的 Codex 任务或 ChatGPT 回答是否满足原始需求，用具体证据说明问题。

先判断这是代码/工具任务、问答/写作任务，还是两者混合。只执行适用的检查，不要求普通回答提供 Git diff，也不要把没有运行环境误写成测试通过。

1. 把原始需求拆成逐项验收清单。对照实际输出，标记已满足、遗漏、错误、无法确认；每项附对应原句、文件位置或日志证据。
2. 对代码/工具任务：核对改动文件和真实用户路径，查漏改、范围外变更、工具失败与提前结束。检查命令是否真的结束，列出退出状态、测试总数和失败数。
3. 对问答/写作任务：检查是否直接回答问题、覆盖关键点、遵守格式要求并给出可执行步骤。把事实、推断和建议分开，指出空泛表述与自相矛盾。
4. 对可核实的事实错误：核对一手来源的日期、适用范围和具体依据。缺少资料或无法访问时写明待核实，不捏造来源，不把合理猜测写成事实。
5. 若怀疑上下文干扰，给出使用同一问题、同一材料的新会话对照方法；一次只改变一个条件，记录前后差异，不凭一次结果推断产品整体能力。
6. 提出最小修正方案，优先处理会改变结果的问题；说明需要补充的输入，以及修正后怎样判断问题已解决。不要为了通过检查而弱化断言、隐藏失败或硬编码结果。
7. 只核对当前任务允许访问的资料，缺少权限时列出未验证项。无需运行的项目标为不适用；已启动、被截断或仍在等待的测试不能标记成功。

先输出“要求 / 实际结果 / 证据 / 状态”的表格，再列出按重要性排序的问题、最小修正与复验步骤。结论只针对提供的这份结果，不编造降智分数。

原始需求：
[粘贴需求]

AI 回答或实际产物：
[粘贴结果]

可选证据：
[相关资料、差异或完整日志；先移除密钥与私人信息]
```
