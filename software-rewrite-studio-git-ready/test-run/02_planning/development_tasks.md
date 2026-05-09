# Development Task List

## DEV-001 Product skeleton
- Goal: 建立 web app、extension、shared types 的基础工程结构。
- Main modules: `web/`, `extension/`, `shared/`
- Constraints: 保持单仓结构简单，不要为了未来扩展过度设计。
- Acceptance: 本地可以分别启动 web app 和 extension 开发环境。

## DEV-002 Report ingestion pipeline
- Goal: 打通 extension 到后端的 report 创建与 artifact 上传。
- Main modules: `api/uploads`, `api/reports`, `shared/report`
- Constraints: 先支持 screenshot；录屏可延后。
- Acceptance: 一次捕获可以生成一条包含基础元数据的 report 记录。

## DEV-003 AI report writer
- Goal: 把原始 capture 转成结构化 bug report。
- Main modules: `ai/report-writer`, `shared/ai-schema`
- Constraints: 输出必须结构化，可编辑，可重试。
- Acceptance: 系统能返回标题、摘要、复现步骤和 severity hint。

## DEV-004 Workspace UI
- Goal: 提供报告列表、详情页和分享页。
- Main modules: `web/app/reports`, `web/components`
- Constraints: 先做单工作区模型，不做复杂权限。
- Acceptance: 用户能查看历史报告、打开详情、复制分享链接。

## DEV-005 GitHub export
- Goal: 把结构化报告导出为 GitHub issue。
- Main modules: `integrations/github`, `web/actions/export`
- Constraints: 只做 GitHub，不做 Jira/Linear。
- Acceptance: 用户能选择仓库并成功创建 issue。

## DEV-006 Privacy guardrails
- Goal: 增加默认保守的采集与脱敏控制。
- Main modules: `extension/privacy`, `web/settings`
- Constraints: 默认不采集高风险字段；所有高风险采集都需要显式开启。
- Acceptance: 用户能看到并控制采集范围，报告中不会默认包含敏感高风险字段。
