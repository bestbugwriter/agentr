# Package Tree Draft

```text
software-rewrite-studio-local/
├── README.md
├── instruction.md
├── memory/
│   └── memory-spec.md
├── commands/
│   ├── rewrite-research.md
│   ├── rewrite-evaluate.md
│   ├── rewrite-plan.md
│   ├── rewrite-package-codex.md
│   └── rewrite-package-claude-code.md
├── skills/
│   ├── platform-aware-research-router/
│   │   ├── SKILL.md
│   │   └── references/
│   │       └── source-routing-cheatsheet.md
│   ├── software-opportunity-evaluator/
│   │   ├── SKILL.md
│   │   └── references/
│   │       ├── platform-source-guide.md
│   │       ├── source-log-template.md
│   │       ├── opportunity-candidates-template.md
│   │       ├── opportunity-scorecard-template.csv
│   │       └── initial-assessment-report-template.md
│   ├── software-implementation-planner/
│   │   ├── SKILL.md
│   │   └── references/
│   │       └── mvp-planning-guide.md
│   └── multi-shell-task-packager/
│       ├── SKILL.md
│       ├── references/
│       │   └── task-package-guidelines.md
│       └── assets/
│           └── task-package-template.md
├── templates/
│   ├── 01_research/
│   │   ├── source_log.md
│   │   ├── opportunity_candidates.md
│   │   ├── opportunity_scorecard.csv
│   │   └── initial_assessment_report.md
│   ├── 02_planning/
│   │   ├── transition_brief.md
│   │   ├── mvp_scope.md
│   │   └── architecture_outline.md
│   └── 03_delivery/
│       ├── shell_neutral_task_package.md
│       ├── codex_prompt.md
│       └── claude_code_prompt.md
├── examples/
│   └── personal-finance-android-gap/
│       ├── 01_research/
│       ├── 02_planning/
│       └── 03_delivery/
└── docs/
    ├── output-order.md
    ├── evidence-status.md
    └── host-usage.md
```

## 关键设计原则
- `commands/` 负责阶段入口，而不是把所有事情都堆进一条长 prompt
- `skills/` 负责可复用动作
- `templates/` 负责稳定工件形态
- `examples/` 负责给 Codex / Claude Code 一个可参考的真实样本
- `memory/` 单独抽出，方便在不同 host 里做兼容说明