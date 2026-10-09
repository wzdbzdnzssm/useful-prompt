# Audit AGENTS and Skills / 优化 AGENTS 和 Skill

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

- ID: `audit-agent-instructions`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Reset site original
- Author / 作者: Reset maintainers

## English

Find agent instructions that cause unnecessary pauses, confirmations, or incomplete work.

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/audit-agent-instructions/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=audit_agent_instructions_en)

**Tool / 工具:** 通用

**Input / 输入:** The AGENTS.md file and related Skills to review.

**Expected result / 预期结果:** A file-referenced issue list, behavioral impact, concrete edits, and disclosure of any permission expansion.

**When to use / 使用时机:** Use when a Skill or project rule needs clearer trigger boundaries, required input, and stopping conditions.

**Completion / 完成标准:** A file-referenced issue list, behavioral impact, concrete edits, and disclosure of any permission expansion.

### Prompt / 提示词

```text
Review my AGENTS.md files and Skills for unclear, conflicting, or overlapping instructions that may cause you to stop unnecessarily, request redundant confirmation, or leave work incomplete. Pay special attention to rules about autonomy, clarification, approval, and task completion. Distinguish safeguards that were set intentionally from wording that accidentally makes routine work require confirmation.

For each issue, quote the relevant instruction, identify the file, explain how it could affect your behavior, and propose a specific edit. Preserve explicit approval requirements, and flag any proposed change that would expand your permissions. Prioritize changes that would make the greatest practical difference. Present the proposed edits for review before changing any files.
```

## 中文

识别会造成不必要停顿、确认或任务不完整的代理指令问题。

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/audit-agent-instructions/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=audit_agent_instructions_zh)

**Tool / 工具:** 通用

**Input / 输入:** 要审阅的 AGENTS.md 文件和相关 Skill。

**Expected result / 预期结果:** 按文件引用的问题清单、行为影响、具体编辑建议及权限扩展说明。

**When to use / 使用时机:** 需要收紧一个 Skill 或项目规则的触发边界、输入要求与结束条件时使用。

**Completion / 完成标准:** 按文件引用的问题清单、行为影响、具体编辑建议及权限扩展说明。

### Prompt / 提示词

```text
审阅我的 AGENTS.md 文件和Skill，寻找不清晰的、冲突的或重叠的指令，这些指令可能会让你不必要地停止、要求多余的确认，或者让工作不完整。特别注意关于自主性、澄清、批准和任务完成的规则。将有意设置的保障措施与那些意外地让常规工作需要确认的措辞区分开来。

对于每个问题，引用相关的指令，识别文件，解释它们如何可能影响你的行为，并提出具体的编辑建议。保留明确的批准要求，并指出任何提议的变更会扩展你的权限。优先考虑那些会带来最大实际差异的变更。在更改任何文件之前，提出供审阅的编辑建议。
```
