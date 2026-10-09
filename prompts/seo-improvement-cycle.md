# Iterative SEO Improvement / SEO 逐轮改进

[English catalog](../README.md) · [中文目录](../README.zh-CN.md)

- ID: `seo-improvement-cycle`
- Status / 状态: `full-text`
- License / 许可: `MIT`
- Source / 来源: Reset site original
- Author / 作者: Reset maintainers

## English

Use real ranking data to improve one keyword near the top position in each cycle.

[View on Reset / 在网站查看](https://reset.skill2web.com/en/prompts/seo-improvement-cycle/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=seo_improvement_cycle_en)

**Tool / 工具:** 通用

**Input / 输入:** The target site, existing SEO data files, and Search Console access when available.

**Expected result / 预期结果:** Ranking records, one necessary page improvement, a seven-day observation state, and a concise report.

**When to use / 使用时机:** Use real ranking data to improve one keyword near the top position in each cycle.

**Completion / 完成标准:** Ranking records, one necessary page improvement, a seven-day observation state, and a concise report.

### Prompt / 提示词

```text
Continuously improve the target website's Google search rankings.

Goal: find a keyword with a realistic chance of reaching position 1, make one improvement that satisfies search needs, and observe it for 7 days. Repeat until position 1 is achieved.

Data
data/seo/watchwords.json — keyword / target page / priority
data/seo/rank-history.json — ranking history. Append only
data/seo/improvement-log.json — improvement history / status / next review date

Statuses:
active — candidate for improvement
observing — in the 7-day observation period after an improvement
achieved — reached position 1. Monitor only

Workflow
1. Measure rankings

Use Google Search Console by default.

node .claude/skills/seo-rank-watch/scripts/fetch_gsc_ranks.mjs \
  --repo <REPO_PATH> --append

Retrieve GSC average position, impressions, and clicks, and confirm the change from the previous ranking.
Use WebSearch only when GSC is unavailable or when checking today's ranking. WebSearch rankings are estimates; treat GSC as authoritative.
rank: null + impressions 0 does not necessarily mean the page is not indexed. Use WebSearch to confirm if needed.

2. Review improvements whose 7-day period has ended

Identify keywords where nextReviewDate <= today.

When evaluating an improvement, use 7-day GSC data rather than the 28-day average.

node .claude/skills/seo-rank-watch/scripts/fetch_gsc_ranks.mjs \
  --repo <REPO_PATH> --days 7

Reached position 1 → achieved

Improved but did not reach position 1 → active

No effect → active. Use a different improvement method next time

Record the decision in improvement-log.json.

3. Choose one keyword to improve today
Exclude observing and achieved.
Choose exactly one keyword in this order:
Positions 2–10 + has impressions — prioritize those closest to position 1

Positions 11–20 + higher impressions
Improved but did not reach position 1 / no effect
High-priority rank: null

Promising unregistered queries found in GSC

If there are no candidates, perform only the ranking check and report, then stop.

Do not manufacture a target merely to make an improvement.

4. Analyze search needs

Before making an improvement, always:

Define in one or two sentences “who is searching, and what do they want to know?”
Use WebSearch to inspect the current top 1–3 pages
Compare the top-ranking pages with the target page
Identify missing information as the gap relative to search needs.

Do not add article volume for SEO's sake. Add information search users want.

5. Improve one keyword

Based on the gap, implement only the necessary content.

Examples:

Improve title / description / intro / FAQ

Add missing content
Add internal links among article ↔ regional page ↔ detail page
Add missing real-world data
Internal links should do more than support SEO: guide search users to what they will want to know or do next.

Improve only one keyword per run.

Do not apply a noindex change or a major page structure change on your own. Propose it and obtain approval.

6. Record the improvement and wait 7 days

In improvement-log.json, record:

{
  "keyword": "...",
  "targetPath": "...",
  "status": "observing",
  "nextReviewDate": "today+7 days",
  "actions": [{
    "date": "...",
    "rankAtAction": 4.2,
    "needs": "search needs",
    "done": "improvement actually made"
  }]
}

Commit the changes to data/seo/*.json to Git.
Never improve an observing keyword again before nextReviewDate.

Report
End with a concise report covering:

Keywords that rose or fell significantly since the previous measurement

Effect assessments made in this run

The keyword selected today and why it was selected

The inferred search need

The improvement actually made

Keywords in observing and their nextReviewDate

Do not claim that rankings improved based on a prediction. Report what changed; determine the effect from the next actual measurement.

Guardrails
Do not scrape Google SERPs with a custom script. Use GSC or WebSearch
Improve only one keyword per run
Strictly observe the 7-day cooldown for observing
Do not rewrite historical data in rank-history.json
Do not output or commit authentication keys or secrets
Do not apply noindex or major structural changes without approval
Do not claim an improvement effect
If there is no improvement target, do nothing
“measure → choose one keyword near position 1 → investigate search intent → improve → observe for 7 days → evaluate with actual measurements”
Repeat this cycle until position 1 is achieved.
```

## 中文

以真实排名数据为依据，每轮只改进一个接近第一的关键词。

[View on Reset / 在网站查看](https://reset.skill2web.com/zh/prompts/seo-improvement-cycle/?utm_source=github&utm_medium=referral&utm_campaign=useful_prompt&utm_content=seo_improvement_cycle_zh)

**Tool / 工具:** 通用

**Input / 输入:** 目标网站及已有的 SEO 数据文件与 Search Console 访问条件。

**Expected result / 预期结果:** 排名记录、一次必要的页面改进、7 天观察状态及简洁报告。

**When to use / 使用时机:** 以真实排名数据为依据，每轮只改进一个接近第一的关键词。

**Completion / 完成标准:** 排名记录、一次必要的页面改进、7 天观察状态及简洁报告。

### Prompt / 提示词

```text
持续改善目标网站的Google搜索排名。

目的：找出有望获得第一的关键词，进行一个满足搜索需求的改善，观察7天。重复此过程直到获得第一。

数据
data/seo/watchwords.json — 关键词 / 目标页面 / 优先级
data/seo/rank-history.json — 排名历史。仅追加
data/seo/improvement-log.json — 改善历史 / 状态 / 下次审查日期

状态：
active — 改善候选
observing — 改善后7天观察中
achieved — 获得第一。只监控

工作流程
1. 测量排名

原则上使用Google Search Console。

node .claude/skills/seo-rank-watch/scripts/fetch_gsc_ranks.mjs \
  --repo <REPO_PATH> --append

获取GSC的平均排名、impressions、clicks，并确认与上次排名变动。
仅在无法使用GSC或想确认当天排名时使用WebSearch。WebSearch排名为概算，以GSC为准。
rank: null + impressions 0 不一定表示未索引。如有必要，使用WebSearch确认。

2. 审查已过7天的改善

确认 nextReviewDate <= 今天 的关键词。

查看改善效果时，不使用28天平均，而是使用7天GSC。

node .claude/skills/seo-rank-watch/scripts/fetch_gsc_ranks.mjs \
  --repo <REPO_PATH> --days 7

获得第一 → achieved

改善但未达第一 → active

无效果 → active。下次使用与上次不同的改善方法

将判定结果记录到 improvement-log.json 中。

3. 选择今天改善的1个关键词
排除 observing 和 achieved。
按以下顺序仅选择1个关键词。
2〜10位 + 有 impressions — 优先选择接近第一的

11〜20位 + impressions 较多
改善但未达第一 / 无效果
高优先级的 rank: null

GSC中发现的有前景的未注册查询

如果没有候选，则仅进行排名检查和报告后结束。

不要为了改善而勉强制造目标。

4. 分析搜索需求

改善前务必，

用1〜2句定义“谁·为了知道什么而搜索”
使用WebSearch确认当前上位1〜3页面
比较上位页面和目标页面
针对搜索需求，识别不足信息作为差距。

不是为了SEO而增加文章量，而是添加搜索用户想要的信息。

5. 改善1个关键词

根据差距，仅实现必要内容。

示例：

title / description / intro / FAQ 改善

添加不足内容
文章 ↔ 地区页面 ↔ 详情页面的内部链接
添加缺失的实际数据
内部链接不仅为了SEO，还引导搜索用户到“接下来想知道·想做的事”。

每次执行仅改善1个关键词。

noindex 变更或大的页面结构变更不要擅自应用，提出建议并获得批准。

6. 记录改善并等待7天

在 improvement-log.json 中，

{
  "keyword": "...",
  "targetPath": "...",
  "status": "observing",
  "nextReviewDate": "今天+7天",
  "actions": [{
    "date": "...",
    "rankAtAction": 4.2,
    "needs": "搜索需求",
    "done": "实际进行的改善"
  }]
}

记录此内容。

将 data/seo/*.json 的变更提交到Git。
observing 的关键词绝对不重新改善直到 nextReviewDate。
报告
最后简洁报告。

从上次大幅上升 / 下降的关键词

本次进行的成效判定

今天选择的关键词和选择理由

推测的搜索需求

实际进行的改善

observing 中的关键词和 nextReviewDate

不要用预测断定排名改善。报告做了什么变更，效果由下次实测判定。
防护栏
不要用自制脚本抓取Google SERP。使用GSC或WebSearch
每次仅改善1个关键词
严格遵守 observing 的7天冷却期
不要改写 rank-history.json 的过去数据
不要输出·提交认证密钥或秘密信息
noindex 或大的结构变更未经批准不要应用
不要断定改善效果
如果没有改善目标则什么都不做
“测量 → 选择1个接近第一的词 → 调查搜索意图 → 改善 → 7天观察 → 实测判定”
重复此循环，直到获得第一。
```
