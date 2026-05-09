# Host Compatibility Draft

## Claude Code
更适合：
- 阶段内上下文较长
- 多文件改动
- 先读文档再执行
- 需要保留较完整 reasoning scaffolding 的任务

建议：
- 每个阶段入口用单独命令 markdown
- skills 与 references 保持目录化
- 让 Claude Code 先读 command，再读 skill，再读 template

## Codex
更适合：
- 边界清晰的单步或少量步骤任务
- 更短更直接的执行提示
- 先给明确文件目标，再给约束和验收标准

建议：
- `rewrite-package-codex` 输出里强调 file targets
- 使用 shell-neutral task package 作为中间层
- 避免把整个 studio 的上下文一次性全部塞给 Codex

## 共用层
为了兼容两者，建议把这些东西做成共享层：
- `skills/`
- `templates/`
- `memory/memory-spec.md`
- `docs/output-order.md`
- `docs/evidence-status.md`

## 不要直接共享的层
- Claude Code 最终 prompt
- Codex 最终 prompt

这两层应由 `multi-shell-task-packager` 或对应 command 在最后一层渲染。