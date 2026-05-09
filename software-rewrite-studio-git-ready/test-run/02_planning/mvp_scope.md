# MVP Scope

## Must have
- `Chrome extension capture`: 截图优先，录屏可作为第二步。
- `Context bundle`: URL、时间、浏览器、视口、控制台日志、用户注释。
- `AI report generation`: 标题、摘要、复现步骤、预期 / 实际结果、严重级别建议。
- `Report workspace`: Web 页面查看单条报告与历史列表。
- `Share + export`: 公开链接分享，GitHub issue 创建。
- `Privacy controls`: 禁用敏感字段、基础文本脱敏开关。

## Nice to have
- `Short video capture`
- `Network request summary`
- `Slack notification`
- `Project-level severity rules`

## Explicitly out of scope
- `Full PM replacement`
- `Deep analytics dashboard`
- `Session replay platform`
- `Jira/Linear/Asana multi-integration from day one`
- `Enterprise auth and permissions`

## Validation goal
+验证三个商业假设：
1. 小团队愿意为“更快写出可用 bug ticket”付费。
2. AI 自动整理能显著减少工程与产品之间的来回沟通。
3. GitHub-first 的轻量交付比大而全 QA 平台更容易拿到首批付费。
