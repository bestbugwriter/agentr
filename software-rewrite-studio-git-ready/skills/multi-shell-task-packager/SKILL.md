---
name: multi-shell-task-packager
description: Use when the user wants shell-neutral task packages and execution-ready prompts for Claude Code, Codex, or similar coding shells.
---

# 多壳任务打包

核心能力：
- 先生成 shell-neutral task package
- 再生成 Claude Code / Codex prompt
- 保持稳定的 Task ID

每个任务至少包含：
- Task ID
- Goal
- Business context
- Related documents
- Target files or modules
- Constraints
- Acceptance criteria
- Expected evidence
- Dependencies

当前规则：
- 先中立打包，再壳层渲染
- 每个任务必须独立可验证
- Claude Code 更适合上下文完整、多文件改动
- Codex 更适合目标清晰、边界明确、指令更短的任务