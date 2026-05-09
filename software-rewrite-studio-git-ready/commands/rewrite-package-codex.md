# /rewrite-package-codex

## Goal
把规划结果转成 Codex 可执行交付。

## Default outputs
- `templates/03_delivery/shell_neutral_task_package.md`
- `templates/03_delivery/codex_prompt.md`

## Rendering rules
- 先 shell-neutral，再 Codex 渲染
- 强调 file targets
- 保持任务边界清晰
- 指令尽量短、直接、可执行