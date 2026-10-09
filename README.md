# useful-prompt — Useful AI prompts

[English](README.md) · [简体中文](README.zh-CN.md)

Useful English and Chinese AI prompts from [Skill2Web](https://reset.skill2web.com/en/prompts/) for coding, writing, research, decisions and computer storage cleanup. Bring your code, notes or question and get results you can check; read the inputs and deliverables before copying.

[Browse the complete online prompt library: search, choose a language and copy](https://reset.skill2web.com/en/prompts/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=readme_en)

33 bilingual entries: 20 copyable full-text prompts and 13 source references. Third-party texts retain their own licenses; references omit texts whose reuse permission has not been established.

## How to use

1. Choose a template by the result you need; read its inputs and expected result.
2. Replace bracketed or other placeholders while keeping the task constraints.
3. Copy the prompt in your preferred language into your assistant; check its evidence before using the result.

Tool and model names are context from the site entries, not cross-model compatibility test results. The Chinese Pelican test entry intentionally keeps the fixed English test prompt.

## Start here

- [Code review](prompts/code-review.md) — Find correctness, edge-case, and maintainability issues
- [Diagnose a failure](prompts/diagnose-failure.md) — Build a path from symptoms to root cause
- [Organize documentation](prompts/documentation-organizer.md) — Turn scattered technical information into actionable documentation
- [Research analysis](prompts/research-analysis.md) — Extract conclusions and evidence chains from source material
- [Explain a core workflow](prompts/workflow-explainer.md) — Explain a real core workflow and its branches with a diagram that can be checked against evidence.
- [Safe computer storage cleanup for Windows and macOS](prompts/computer-storage-cleanup.md) — Investigate disk usage and review cleanup candidates before confirmed moves to the Recycle Bin or Trash.

## Complete catalog

### Engineering

| Template | Use | Included |
| --- | --- | --- |
| [Code review](prompts/code-review.md) | Find correctness, edge-case, and maintainability issues | Full text |
| [Add regression tests](prompts/regression-tests.md) | Add valuable tests for a change | Full text |
| [Diagnose a failure](prompts/diagnose-failure.md) | Build a path from symptoms to root cause | Full text |
| [Safe refactoring](prompts/safe-refactor.md) | Improve code structure incrementally while preserving its contract | Full text |
| [Fill test coverage and fix failures](prompts/anthro-test-workflow.md) | Plan test coverage and investigate failing tests. | Reference |
| [Implement and verify a design](prompts/design-visual-verification.md) | Build a design and check the rendered result. | Reference |
| [Evaluate and Improve Skills](prompts/evaluate-skills.md) | Assess the usefulness of existing skills. | Reference |
| [Explain a core workflow](prompts/workflow-explainer.md) | Explain a real core workflow and its branches with a diagram that can be checked against evidence. | Full text |
| [Simplify CI around essential behavior](prompts/ci-behavior-audit.md) | Remove test restrictions that break routine copy, style, and refactoring changes while preserving checks that protect delivery. | Full text |
| [Task completion and answer quality review](prompts/task-repro-check.md) | Review omissions, errors, and unverified work in Codex tasks or ChatGPT answers. | Full text |
| [Pelican test prompt: fixed bicycle SVG prompt](prompts/pelican-bicycle-test.md) | Copy the fixed English SVG prompt, check its source, and follow the linked guide to run the Pelican bicycle test. | Full text |

### Writing and content

| Template | Use | Included |
| --- | --- | --- |
| [Organize documentation](prompts/documentation-organizer.md) | Turn scattered technical information into actionable documentation | Full text |
| [Personal portfolio webpage](prompts/portfolio-webpage.md) | Plan a personal portfolio page. | Reference |
| [Turn research into a Canva presentation](prompts/research-presentation.md) | Organize research into a presentation. | Reference |
| [Extract a Writing Style](prompts/extract-writing-style.md) | Describe recurring features in writing samples. | Reference |
| [Rewrite an old prompt](prompts/prompt-rewrite.md) | Keep the original intent while removing ambiguity that can cause an old prompt to drift. | Full text |
| [Project knowledge map](prompts/knowledge-map.md) | Organize scattered project material into navigation that answers a reader’s real questions. | Full text |
| [Turn an Art Idea into an Image Prompt](prompts/057fe2a6-793b-4c84-8eaa-c6607afe324d.md) | Shape an art concept and visual preferences into a clear, evocative prompt ready for an image-generation model. | Full text |

### Research

| Template | Use | Included |
| --- | --- | --- |
| [Research analysis](prompts/research-analysis.md) | Extract conclusions and evidence chains from source material | Full text |
| [User feedback theme workbook](prompts/user-feedback-workbook.md) | Group feedback into themes for a workbook. | Reference |
| [Socratic tutor](prompts/socratic-tutor.md) | Learn through guided questions. | Reference |

### Decisions and planning

| Template | Use | Included |
| --- | --- | --- |
| [Compare approaches](prompts/compare-options.md) | Choose an implementation approach within stated constraints | Full text |
| [Devil’s advocate](prompts/devils-advocate.md) | Explore objections to a proposed argument. | Reference |
| [Analyze Developer Growth](prompts/developer-growth.md) | Reflect on development habits and learning needs. | Reference |
| [Identify Plan Risks and Develop Responses](prompts/58cc2c73-3a7c-4741-986c-38df7b105f30.md) | Identify risks in a plan, assess their impact, and develop responses through a step-by-step conversation, then summarize your contributions. | Full text |
| [Practice a Negotiation and Get Feedback](prompts/34e7fbdc-e0ce-4c3b-b144-97b6977c4772.md) | Practice a realistic negotiation tailored to your experience and goals, then receive specific, balanced, practical feedback. | Full text |

### Workflows and delivery

| Template | Use | Included |
| --- | --- | --- |
| [Delivery check](prompts/delivery-check.md) | Verify actual readiness before release or handoff | Full text |
| [Extract Reusable Skills](prompts/extract-reusable-skills.md) | Identify repeatable steps worth saving as a skill. | Reference |
| [Improve Project Rules](prompts/improve-project-rules.md) | Review a project’s working instructions. | Reference |
| [Capture Proven Project Learning](prompts/capture-project-learning.md) | Record lessons supported by project experience. | Reference |
| [Iterative SEO Improvement](prompts/seo-improvement-cycle.md) | Use real ranking data to improve one keyword near the top position in each cycle. | Full text |
| [Audit AGENTS and Skills](prompts/audit-agent-instructions.md) | Find agent instructions that cause unnecessary pauses, confirmations, or incomplete work. | Full text |
| [Safe computer storage cleanup for Windows and macOS](prompts/computer-storage-cleanup.md) | Investigate disk usage and review cleanup candidates before confirmed moves to the Recycle Bin or Trash. | Full text |

## Browse online

[Reset](https://reset.skill2web.com/en/) lets you browse, search and copy prompts, and also provides public reset messages for Codex and Claude. Use the site for quick discovery and this repository for offline reference, change tracking and contributions.

## Sources, licenses and maintenance

Public snapshot: 2026-10-09. Full texts preserve the site's language versions; updates are maintained manually, without an automatic-sync promise. The structured source of truth is [data/prompts.json](data/prompts.json).

[MIT LICENSE](LICENSE) covers original repository documentation and prompt versions identified as site originals. Mollick adaptations retain CC BY 4.0; the Fabric adaptation retains its MIT notice. See [third-party notices](THIRD_PARTY_NOTICES.md). Other sources are linked only, with no license granted for their source texts.

Suggest new prompts, translation improvements or source-license evidence through [Issues](https://github.com/wzdbzdnzssm/useful-prompt/issues).
