# Simplify CI around essential behavior / 精简 CI，保留关键行为检查

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

- ID: `ci-behavior-audit`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Reset site original
- Author / 作者: Reset maintainers

## English

Remove test restrictions that break routine copy, style, and refactoring changes while preserving checks that protect delivery.

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/ci-behavior-audit/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=ci_behavior_audit_en)

**Tool / 工具:** Codex

**Input / 输入:** The current project, existing CI workflows, test entry points, and accessible recent failure records.

**Expected result / 预期结果:** Evidence-based minimal test changes, retained critical checks, the version actually verified and its results, and remaining blockers.

**When to use / 使用时机:** Remove test restrictions that break routine copy, style, and refactoring changes while preserving checks that protect delivery.

**Completion / 完成标准:** Evidence-based minimal test changes, retained critical checks, the version actually verified and its results, and remaining blockers.

### Prompt / 提示词

```text
Review and simplify this project's CI to address checks that are too broad and fail on normal copy, styling, or refactoring changes. Make the necessary changes directly.

First inspect the actual workflows, test entry points, and recent failures. Apply these principles:

- Keep essential checks: builds, types, critical business flows, data correctness, permissions, security, payments, and necessary accessibility checks.
- Remove unnecessary restrictions: exact marketing-copy matching, decorative styling, pixel dimensions with no business meaning, and dependencies on internal function names, source snippets, DOM nesting, or other implementation details. Valuable visual checks may remain as manual verification.
- Prefer behavior: search tests should check results and navigation; form tests should check submission and error handling. Do not merely replace old copy with new copy in tests and recreate the same problem.
- Distinguish content contracts: amounts, quotas, legal notices, and security warnings may be essential contracts and must not be removed alongside ordinary marketing copy.

Change only tests with evidence of excessive constraints. Do not skip whole test groups, swallow errors, weaken security validation, or substitute assertions with no verification value just to reduce failures. Identify genuine functional defects separately; do not label them overly strict tests.

Use the project's existing tools and isolated test environment. Do not connect to production databases, overwrite uncommitted work, make unrelated refactors, or introduce a new testing framework. Complete low-risk changes independently. Ask only when an important business contract cannot be resolved from project evidence.

Run verification relevant to the changes. Briefly report which unnecessary restrictions were removed, which critical checks remain, the exact version tested and results, and outstanding blockers. Never report an unexecuted check as passed.
```

## 中文

去掉让正常文案、样式和重构频繁失败的测试限制，保留真正影响交付的检查。

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/ci-behavior-audit/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=ci_behavior_audit_zh)

**Tool / 工具:** Codex

**Input / 输入:** 当前项目、现有 CI 工作流、测试入口及可访问的近期失败记录。

**Expected result / 预期结果:** 有证据的最小测试调整、保留的关键检查、实际验证版本与结果，以及剩余阻塞。

**When to use / 使用时机:** 去掉让正常文案、样式和重构频繁失败的测试限制，保留真正影响交付的检查。

**Completion / 完成标准:** 有证据的最小测试调整、保留的关键检查、实际验证版本与结果，以及剩余阻塞。

### Prompt / 提示词

```text
请审查并精简这个项目的 CI，解决“CI 管得太宽，正常改文案、样式或重构也会失败”的问题，并直接完成必要修改。

先查看实际工作流、测试入口和近期失败，按以下原则处理：

- **保留必要检查**：构建、类型、关键业务流程、数据正确性、权限、安全、支付及必要的可访问性检查。
- **取消非必要限制**：宣传文案逐字匹配、装饰性样式、无业务意义的像素尺寸，以及对内部函数名、源码片段、DOM 层级等实现细节的绑定。有价值的视觉检查可保留为手动验证。
- **优先验证行为**：例如搜索应检查结果和跳转，表单应检查提交与错误处理。不要仅把测试中的旧文案换成新文案，继续制造同类问题。
- **区分内容性质**：金额、额度、法律告知、安全提示等可能属于必要契约，不能与普通宣传文案一起删除。

只调整确有证据表明过度约束的测试，不为减少失败而跳过整组测试、吞掉错误、放宽安全校验或改成没有验证价值的断言。发现真实功能问题时如实区分，不把它当成测试过严。

使用项目现有工具和隔离测试环境，不连接生产数据库，不覆盖未提交的工作，不顺手重构或引入新的测试框架。低风险调整自主完成，只有涉及重要业务契约且无法从项目中判断时才询问。

完成后运行与改动相关的验证，简要报告：取消了哪些非必要限制、保留了哪些关键检查、实际验证的版本及结果、仍存在的阻塞。未执行的检查不得报告为通过。
```
