# Architecture Outline

## Recommended stack
- `Extension`: Chrome Manifest V3 + TypeScript + minimal React UI
- `Web app`: Next.js
- `Auth / DB / Storage`: Supabase
- `AI layer`: OpenAI Responses API or equivalent structured-output LLM path
- `Issue export`: GitHub Issues API
- `Hosting`: Vercel for web app, Supabase managed services for backend primitives

## System shape
1. User captures a bug from the extension.
2. Extension collects allowed artifacts and uploads them through signed URLs.
3. Backend stores raw artifacts and normalized metadata.
4. AI summarizer turns raw capture into a structured report.
5. Web app renders the report and offers edit, share, and GitHub export.

## Core modules
- `extension/capture`: screenshot, optional recording, user annotation
- `extension/context`: page metadata, console log collection, privacy filters
- `api/uploads`: signed upload URLs and artifact registration
- `api/reports`: report creation, retrieval, editing, sharing
- `ai/report-writer`: prompt assembly, structured output validation, retry policy
- `integrations/github`: repository connection and issue creation
- `web/workspace`: list view, detail view, export actions

## Data model
- `workspace`
- `project`
- `report`
- `artifact`
- `capture_context`
- `ai_report`
- `github_export`

## Key design decisions
- `GitHub first`: 先只服务一个工程出口，避免集成面失控。
- `Structured output`: AI 产物必须写入固定字段，不直接存自由文本。
- `Privacy before convenience`: 默认不采集 cookie、localStorage 和完整请求体。
- `Screenshot first`: 先把最稳定的 capture 模式跑通，再补录屏。

## Main architectural risks
- 大图片 / 录屏上传带来的存储与传输成本
- 控制台与网络日志噪声过大，影响 AI 摘要质量
- Manifest V3 权限边界与站点兼容性
