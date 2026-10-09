# Diagnose a failure / 故障定位

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

- ID: `diagnose-failure`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Reset site original
- Author / 作者: Reset maintainers

## English

Build a path from symptoms to root cause

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/diagnose-failure/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=diagnose_failure_en)

**Tool / 工具:** Codex

**Input / 输入:** Symptoms, logs, and recent changes:
[Paste]

**Expected result / 预期结果:** Prioritized hypotheses, diagnostic steps, and fix verification

**When to use / 使用时机:** Build a path from symptoms to root cause

**Completion / 完成标准:** Prioritized hypotheses, diagnostic steps, and fix verification

### Prompt / 提示词

```text
Help diagnose the failure below. First separate known facts from assumptions, then rank root-cause hypotheses by likelihood and impact. For each hypothesis, design the lowest-cost diagnostic step that can distinguish its outcome. Do not jump directly to speculative code changes. Once the root cause is established, provide the smallest fix, regression risks, and verification commands.

Symptoms, logs, and recent changes:
[Paste]
```

## 中文

从症状到根因建立排查路径

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/diagnose-failure/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=diagnose_failure_zh)

**Tool / 工具:** Codex

**Input / 输入:** 症状、日志、近期改动：
[粘贴]

**Expected result / 预期结果:** 假设优先级、诊断步骤和修复验证

**When to use / 使用时机:** 从症状到根因建立排查路径

**Completion / 完成标准:** 假设优先级、诊断步骤和修复验证

### Prompt / 提示词

```text
请协助定位以下故障。先区分已知事实与推测，按可能性和影响排序列出根因假设。为每个假设设计一个成本最低、能区分结果的诊断步骤；不要直接猜测修改。得到根因后，给出最小修复、回归风险和验证命令。

症状、日志、近期改动：
[粘贴]
```
