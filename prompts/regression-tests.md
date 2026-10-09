# Add regression tests / 补齐回归测试

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

- ID: `regression-tests`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Reset site original
- Author / 作者: Reset maintainers

## English

Add valuable tests for a change

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/regression-tests/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=regression_tests_en)

**Tool / 工具:** Codex

**Input / 输入:** Requirement/change:
[Paste content]

**Expected result / 预期结果:** Test checklist, minimal implementation, and coverage notes

**When to use / 使用时机:** Add valuable tests for a change

**Completion / 完成标准:** Test checklist, minimal implementation, and coverage notes

### Prompt / 提示词

```text
Based on the requirements and current implementation below, add a minimal but effective regression test suite. First explain the critical paths, failure boundaries, and parts that should not be mocked, then provide test code that fits the project's existing test stack. The tests should fail before the fix and pass afterward. Do not write tests that merely mirror the implementation to raise coverage.

Requirement/change:
[Paste content]
```

## 中文

为改动补充有价值的测试

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/regression-tests/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=regression_tests_zh)

**Tool / 工具:** Codex

**Input / 输入:** 需求/改动：
[粘贴内容]

**Expected result / 预期结果:** 测试清单、最小实现和覆盖说明

**When to use / 使用时机:** 为改动补充有价值的测试

**Completion / 完成标准:** 测试清单、最小实现和覆盖说明

### Prompt / 提示词

```text
基于以下需求与现有实现，补充最小但有效的回归测试。先说明关键路径、失败边界和不该 mock 的部分，再给出符合项目测试栈的测试代码。测试应在修复前失败、修复后通过；不要为了覆盖率写镜像实现测试。

需求/改动：
[粘贴内容]
```
