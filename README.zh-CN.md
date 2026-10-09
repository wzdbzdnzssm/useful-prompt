# useful-prompt — 实用 AI 提示词

[English](README.md) · [简体中文](README.zh-CN.md)

来自 [Skill2Web](https://reset.skill2web.com/zh/prompts/) 的中英文实用 AI 提示词，覆盖编程、写作、研究、决策和电脑存储清理。带入代码、材料或问题，得到可检查的结果；先看输入与交付要求，再复制使用。

[浏览完整在线提示词库：搜索、选择语言并复制](https://reset.skill2web.com/zh/prompts/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=readme_zh)

共 33 个双语条目：20 个可复制正文、13 个来源链接索引。第三方正文各自保留许可；链接索引不包含未确认复用许可的正文。

## 使用方法

1. 按你需要的结果选模板，先看输入和预期结果。
2. 替换方括号或其他占位符，保留任务限制。
3. 复制对应语言的正文到你的助手；先核对输出证据，再用于真实工作。

工具或模型名称来自网站条目，仅提供使用背景，不代表跨模型兼容性测试。鹈鹕测试的中文条目有意保留固定英文试题。

## 快速入口

- [代码审查](prompts/code-review.md) — 找出正确性、边界和可维护性问题
- [故障定位](prompts/diagnose-failure.md) — 从症状到根因建立排查路径
- [文档整理](prompts/documentation-organizer.md) — 把零散技术信息整理成可执行文档
- [研究分析](prompts/research-analysis.md) — 从资料中提取结论与证据链
- [核心流程图解](prompts/workflow-explainer.md) — 用可核对的图解说明一个真实核心流程及其分支。
- [电脑存储空间清理（Windows / macOS）](prompts/computer-storage-cleanup.md) — 空间不足时，深入调查磁盘占用，逐项确认后移入回收站，并核对恢复方式和实际空间变化。

## 完整分类目录

### 工程开发

| 模板 | 用途 | 收录 |
| --- | --- | --- |
| [代码审查](prompts/code-review.md) | 找出正确性、边界和可维护性问题 | 正文 |
| [补齐回归测试](prompts/regression-tests.md) | 为改动补充有价值的测试 | 正文 |
| [故障定位](prompts/diagnose-failure.md) | 从症状到根因建立排查路径 | 正文 |
| [安全重构](prompts/safe-refactor.md) | 在保持契约下分步改善代码结构 | 正文 |
| [补齐测试覆盖并修复](prompts/anthro-test-workflow.md) | 规划测试覆盖并排查失败测试。 | 来源索引 |
| [实现设计并视觉验收](prompts/design-visual-verification.md) | 实现设计并检查实际渲染效果。 | 来源索引 |
| [评估并改进 Skill](prompts/evaluate-skills.md) | 评估已有技能的实用性。 | 来源索引 |
| [核心流程图解](prompts/workflow-explainer.md) | 用可核对的图解说明一个真实核心流程及其分支。 | 正文 |
| [精简 CI，保留关键行为检查](prompts/ci-behavior-audit.md) | 去掉让正常文案、样式和重构频繁失败的测试限制，保留真正影响交付的检查。 | 正文 |
| [任务完成与回答质量复查](prompts/task-repro-check.md) | 复查 Codex 任务或 ChatGPT 回答中的遗漏、错误和未验证事项。 | 正文 |
| [鹈鹕骑自行车 SVG 测试](prompts/pelican-bicycle-test.md) | 参考 Simon Willison 的鹈鹕实验，使用本站补充了输出格式与工具限制的固定英文版本。 | 正文 |

### 写作与内容

| 模板 | 用途 | 收录 |
| --- | --- | --- |
| [文档整理](prompts/documentation-organizer.md) | 把零散技术信息整理成可执行文档 | 正文 |
| [个人作品集网页](prompts/portfolio-webpage.md) | 规划个人作品集页面。 | 来源索引 |
| [研究转 Canva 汇报](prompts/research-presentation.md) | 把研究材料组织为演示文稿。 | 来源索引 |
| [提取写作风格](prompts/extract-writing-style.md) | 描述写作样本中反复出现的风格特征。 | 来源索引 |
| [旧提示词改写](prompts/prompt-rewrite.md) | 保留原任务意图，消除旧提示词中会导致执行偏差的歧义。 | 正文 |
| [项目资料导航](prompts/knowledge-map.md) | 把散落的项目资料按读者问题整理成可用的导航入口。 | 正文 |
| [将创意转化为图像生成提示词](prompts/057fe2a6-793b-4c84-8eaa-c6607afe324d.md) | 把用户的艺术构想和视觉偏好整理成清晰、生动、可直接用于图像生成模型的提示词。 | 正文 |

### 研究分析

| 模板 | 用途 | 收录 |
| --- | --- | --- |
| [研究分析](prompts/research-analysis.md) | 从资料中提取结论与证据链 | 正文 |
| [用户反馈主题工作簿](prompts/user-feedback-workbook.md) | 将用户反馈归类为工作簿主题。 | 来源索引 |
| [苏格拉底式导师](prompts/socratic-tutor.md) | 通过引导式提问学习。 | 来源索引 |

### 决策与规划

| 模板 | 用途 | 收录 |
| --- | --- | --- |
| [方案比较](prompts/compare-options.md) | 在约束下选择实现方案 | 正文 |
| [反方质询](prompts/devils-advocate.md) | 探索针对观点的反对意见。 | 来源索引 |
| [开发者成长分析](prompts/developer-growth.md) | 回顾开发习惯和学习需求。 | 来源索引 |
| [提前找出计划风险并制定应对办法](prompts/58cc2c73-3a7c-4741-986c-38df7b105f30.md) | 通过循序渐进的对话，识别计划风险、评估影响并思考应对办法，最后汇总你提出的内容。 | 正文 |
| [练习谈判并获得反馈](prompts/34e7fbdc-e0ce-4c3b-b144-97b6977c4772.md) | 根据你的经验和目标设计真实的谈判练习，并在结束后提供具体、均衡且实用的反馈。 | 正文 |

### 工作流与交付

| 模板 | 用途 | 收录 |
| --- | --- | --- |
| [交付检查](prompts/delivery-check.md) | 上线或交付前核对真实完成度 | 正文 |
| [从会话提炼可复用 Skill](prompts/extract-reusable-skills.md) | 识别适合保存为技能的重复步骤。 | 来源索引 |
| [补充项目规则](prompts/improve-project-rules.md) | 审视项目协作指令。 | 来源索引 |
| [保存已验证项目经验](prompts/capture-project-learning.md) | 记录项目实践支持的经验。 | 来源索引 |
| [SEO 逐轮改进](prompts/seo-improvement-cycle.md) | 以真实排名数据为依据，每轮只改进一个接近第一的关键词。 | 正文 |
| [优化 AGENTS 和 Skill](prompts/audit-agent-instructions.md) | 识别会造成不必要停顿、确认或任务不完整的代理指令问题。 | 正文 |
| [电脑存储空间清理（Windows / macOS）](prompts/computer-storage-cleanup.md) | 空间不足时，深入调查磁盘占用，逐项确认后移入回收站，并核对恢复方式和实际空间变化。 | 正文 |

## 在线浏览

[Reset](https://reset.skill2web.com/zh/) 支持浏览、搜索和复制提示词，也提供 Codex / Claude 的公开重置消息。需要快速查找时可直接使用网站；本仓库便于离线查阅、追踪修改和贡献。

## 来源、许可与维护

公开快照日期：2026-10-09。正文保持网站对应语言的现有文本，不承诺自动同步。结构化单源为 [data/prompts.json](data/prompts.json)。

[MIT LICENSE](LICENSE) 适用于仓库原创文档和标识为本站原创的提示词版本。Mollick 精选改编保留 CC BY 4.0，Fabric 改编保留其 MIT 通知；详情见 [第三方许可](THIRD_PARTY_NOTICES.md)。其他来源仅收录链接，不授予来源文本许可。

欢迎通过 [Issues](https://github.com/wzdbzdnzssm/useful-prompt/issues) 提供新提示词、翻译改进或来源许可证明。
