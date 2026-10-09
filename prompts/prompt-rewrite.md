# Rewrite an old prompt / 旧提示词改写

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

- ID: `prompt-rewrite`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Reset site original
- Author / 作者: Reset maintainers

## English

Keep the original intent while removing ambiguity that can cause an old prompt to drift.

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/prompt-rewrite/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=prompt_rewrite_en)

**Tool / 工具:** 通用

**Input / 输入:** Old prompt:
[Paste the original prompt]

**Expected result / 预期结果:** A rewritten prompt, a change rationale, and choices that still need the user.

**When to use / 使用时机:** Keep the original intent while removing ambiguity that can cause an old prompt to drift.

**Completion / 完成标准:** A rewritten prompt, a change rationale, and choices that still need the user.

### Prompt / 提示词

```text
Rewrite the old prompt below so it can be executed reliably, without expanding the authority of the original task. Identify unclear or conflicting goals, inputs, outputs, constraints, defaults, and stopping conditions; then provide a rewrite and explain each change. Leave choices that cannot be inferred as questions to confirm; do not invent requirements.

Old prompt:
[Paste the original prompt]
```

## 中文

保留原任务意图，消除旧提示词中会导致执行偏差的歧义。

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/prompt-rewrite/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=prompt_rewrite_zh)

**Tool / 工具:** 通用

**Input / 输入:** 旧提示词：
[粘贴原提示词]

**Expected result / 预期结果:** 改写后的提示词、修改说明，以及仍需用户决定的问题。

**When to use / 使用时机:** 保留原任务意图，消除旧提示词中会导致执行偏差的歧义。

**Completion / 完成标准:** 改写后的提示词、修改说明，以及仍需用户决定的问题。

### Prompt / 提示词

```text
改写下面这条旧提示词，使它更容易被可靠执行，但不要扩大原任务的授权范围。先找出目标、输入、输出、约束、默认选择和停止条件中不明确或冲突的地方；再给出改写版并说明修改理由。无法从原文推断的选择保留为待确认项，不要补造要求。

旧提示词：
[粘贴原提示词]
```
