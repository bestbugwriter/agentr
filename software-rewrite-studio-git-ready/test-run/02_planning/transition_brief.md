# Transition Brief

## Target
AI-first visual bug reporting copilot for browser-based product teams.

## Why now
- 多模态模型已经足够稳定，能把截图、录屏和页面元数据整理成结构化 ticket。
- Jam、Marker.io、BugHerd 的官方定价证明这个场景存在持续付费。
- 对个人开发者来说，浏览器扩展 + 轻量 SaaS 的交付边界清楚，不需要先做复杂底层平台。

## Core wedge
第一阶段不做完整 QA 管理系统，只做：
1. 一键捕获网页问题
2. 自动整理成可读、可转发、可导出的 bug report
3. 先接 GitHub，让工程团队能直接落地

## Target user
- 5 到 50 人的软件团队
- 接客户网站修改需求的设计 / 开发代理商
- 没有专职 QA、但经常需要收集和复现网页问题的独立 SaaS 团队

## MVP recommendation
### 必做
- Chrome 扩展捕获截图或短录屏
- 当前页面 URL、视口、浏览器信息、控制台日志采集
- AI 生成标题、摘要、复现步骤、预期结果、实际结果、严重级别建议
- Web 工作区查看报告与分享链接
- GitHub issue 导出

### 可选增强
- 网络请求采样
- Slack webhook
- 手工脱敏框选

### 暂不做
- Jira / Linear / Asana 全家桶
- 完整项目管理看板
- 移动端 SDK
- 企业权限、SSO、审计

## Key risks
1. 日志和页面内容采集可能触碰敏感数据，隐私设计必须默认保守。
2. 如果 AI 输出不够稳定，用户会觉得只是“更花哨的截图工具”。
3. 如果一开始就接太多集成，会把 MVP 拉成通用 QA 平台。

## Evidence status
- `已官方验证`：价格带、浏览器分发、核心形态。
- `部分验证`：最优收费层级和首个细分客群。
- `未完全验证`：首批客户更偏好截图流还是录屏流，是否愿意接受 AI 自动生成的严重级别建议。
