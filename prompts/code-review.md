# Code review / 代码审查

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

- ID: `code-review`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Reset site original
- Author / 作者: Reset maintainers

## English

Find correctness, edge-case, and maintainability issues

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/code-review/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=code_review_en)

**Tool / 工具:** Codex

**Input / 输入:** Changes:
[Paste a diff or files]

**Expected result / 预期结果:** Issues ranked by severity, with evidence and minimal fixes

**When to use / 使用时机:** Find correctness, edge-case, and maintainability issues

**Completion / 完成标准:** Issues ranked by severity, with evidence and minimal fixes

### Prompt / 提示词

```text
Review the changes below. Prioritize correctness, security, edge cases, error handling, concurrency, and compatibility. Rank findings from P0 to P3. For each finding, identify the file/location, trigger, why it fails, and the smallest viable fix. Do not comment on unrelated style. If you find no blocking issues, state the risks that still require manual verification.

Changes:
[Paste a diff or files]
```

## 中文

找出正确性、边界和可维护性问题

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/code-review/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=code_review_zh)

**Tool / 工具:** Codex

**Input / 输入:** 改动：
[粘贴 diff 或文件]

**Expected result / 预期结果:** 按严重度列出问题、证据和最小修复建议

**When to use / 使用时机:** 找出正确性、边界和可维护性问题

**Completion / 完成标准:** 按严重度列出问题、证据和最小修复建议

### Prompt / 提示词

```text
请审查以下改动。优先检查正确性、安全性、边界条件、错误处理、并发与兼容性。请按 P0 到 P3 排序，每项写明文件/位置、触发条件、为何会出错，以及最小修复方案。不要评价无关风格；若未发现阻塞问题，请说明仍需人工验证的风险。

改动：
[粘贴 diff 或文件]
```
