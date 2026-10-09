# Safe refactoring / 安全重构

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

- ID: `safe-refactor`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Reset site original
- Author / 作者: Reset maintainers

## English

Improve code structure incrementally while preserving its contract

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/safe-refactor/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=safe_refactor_en)

**Tool / 工具:** Codex

**Input / 输入:** Code:
[Paste]

**Expected result / 预期结果:** Constraint checklist, incremental diffs, and verification plan

**When to use / 使用时机:** Improve code structure incrementally while preserving its contract

**Completion / 完成标准:** Constraint checklist, incremental diffs, and verification plan

### Prompt / 提示词

```text
Refactor the code below without changing externally observable behavior. First document the interfaces, data semantics, and error behavior that must remain unchanged, then identify duplication, coupling, and areas that are hard to test. Propose an order of changes that can be committed incrementally; for every step, include the change, its risks, and how to verify it. Do not introduce unnecessary frameworks or abstractions.

Code:
[Paste]
```

## 中文

在保持契约下分步改善代码结构

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/safe-refactor/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=safe_refactor_zh)

**Tool / 工具:** Codex

**Input / 输入:** 代码：
[粘贴]

**Expected result / 预期结果:** 约束清单、分步 diff 和验证方案

**When to use / 使用时机:** 在保持契约下分步改善代码结构

**Completion / 完成标准:** 约束清单、分步 diff 和验证方案

### Prompt / 提示词

```text
在不改变对外行为的前提下重构以下代码。先写出必须保持的接口、数据语义与错误行为，再识别重复、耦合或难测之处。给出可以逐步提交的改造顺序，每一步包含改动、风险与验证。不要引入无必要的新框架或抽象。

代码：
[粘贴]
```
