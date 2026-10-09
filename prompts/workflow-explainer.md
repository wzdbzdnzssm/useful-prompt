# Explain a core workflow / 核心流程图解

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

- ID: `workflow-explainer`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Reset site original
- Author / 作者: Reset maintainers

## English

Explain a real core workflow and its branches with a diagram that can be checked against evidence.

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/workflow-explainer/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=workflow_explainer_en)

**Tool / 工具:** Codex

**Input / 输入:** Material:
[Paste code, logs, API notes, or process notes]

**Expected result / 预期结果:** A code- or material-backed flowchart, step notes, branch evidence, and open questions.

**When to use / 使用时机:** Explain a real core workflow and its branches with a diagram that can be checked against evidence.

**Completion / 完成标准:** A code- or material-backed flowchart, step notes, branch evidence, and open questions.

### Prompt / 提示词

```text
Using the code, logs, or process material below, explain how 【core workflow name】 runs from start to finish. List evidenced entry points, main steps, data changes, external calls, success path, and failure branches; then create a saveable Mermaid flowchart and short explanation. Every key node must trace to the supplied material; mark unsupported parts as “To confirm.”

Material:
[Paste code, logs, API notes, or process notes]
```

## 中文

用可核对的图解说明一个真实核心流程及其分支。

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/workflow-explainer/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=workflow_explainer_zh)

**Tool / 工具:** Codex

**Input / 输入:** 材料：
[粘贴代码、日志、接口说明或流程笔记]

**Expected result / 预期结果:** 基于代码或资料的流程图、步骤说明、分支依据和待确认项。

**When to use / 使用时机:** 用可核对的图解说明一个真实核心流程及其分支。

**Completion / 完成标准:** 基于代码或资料的流程图、步骤说明、分支依据和待确认项。

### Prompt / 提示词

```text
根据下面的代码、日志或流程材料，解释【核心流程名称】如何从开始走到结束。先列出能够证实的入口、主要步骤、数据变化、外部调用、成功路径和失败分支；再生成可保存的 Mermaid 流程图和简短说明。图中的关键节点都要能追溯到提供材料，缺少依据的地方标为待确认。

材料：
[粘贴代码、日志、接口说明或流程笔记]
```
