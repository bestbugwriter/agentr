# Repo File Map Draft

## 建议作为第一版真实仓库保留的目录

```text
software-rewrite-studio-local/
├── README.md
├── instruction.md
├── commands/
├── skills/
├── templates/
├── docs/
├── examples/
└── memory/
```

## 顶层文件
- `README.md`
  - 说明项目定位：从 research 开始即可在 Codex / Claude Code 中运行
- `instruction.md`
  - 主编排说明
  - 固定研究摘要顺序
  - 固定 evidence status
  - 固定高分候选到实施规划的衔接规则

## commands/
建议第一版至少保留：
- `rewrite-research.md`
- `rewrite-evaluate.md`
- `rewrite-plan.md`
- `rewrite-package-codex.md`
- `rewrite-package-claude-code.md`

## skills/
建议第一版至少保留：
- `platform-aware-research-router/`
- `software-opportunity-evaluator/`
- `software-implementation-planner/`
- `multi-shell-task-packager/`

## templates/
### 研究阶段
- `templates/01_research/source_log.md`
- `templates/01_research/opportunity_candidates.md`
- `templates/01_research/opportunity_scorecard.csv`
- `templates/01_research/initial_assessment_report.md`

### 规划阶段
- `templates/02_planning/transition_brief.md`
- `templates/02_planning/mvp_scope.md`
- `templates/02_planning/architecture_outline.md`

### 交付阶段
- `templates/03_delivery/shell_neutral_task_package.md`
- `templates/03_delivery/codex_prompt.md`
- `templates/03_delivery/claude_code_prompt.md`

## docs/
建议保留：
- `docs/output-order.md`
- `docs/evidence-status.md`
- `docs/host-usage.md`

## memory/
- `memory/memory-spec.md`
  - 作为 host 无原生 Memory 时的本地替代说明

## examples/
第一版建议只保留 1 个样例：
- `examples/personal-finance-android-gap/`
  - 让本地 Codex / Claude Code 从 research 到 package 都有参考路径
