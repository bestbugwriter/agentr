# /rewrite-package-claude-code

## Goal
把规划结果转成 Claude Code 可执行交付。

## Default outputs
- `templates/03_delivery/shell_neutral_task_package.md`
- `templates/03_delivery/claude_code_prompt.md`

## Rendering rules
- 先 shell-neutral，再 Claude Code 渲染
- 保留更多上下文
- 允许更完整的步骤说明
- 适合多文件、文档优先的执行方式