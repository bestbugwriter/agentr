# Migration Plan Draft

## 从当前 agent 回灌到你现有项目的重点

### 1. instruction.md
把当前 agent 里已经验证有效的几条规则并回去：
- 研究先做平台路由，再下结论
- 扫描类请求固定聊天输出顺序
- Evidence status 必须单独成节
- 高分候选进入实施规划前，必须有 transition brief

### 2. research 阶段模板
把以下模板正式加入你们本地包：
- source_log.md
- opportunity_candidates.md
- opportunity_scorecard.csv
- initial_assessment_report.md

### 3. delivery 阶段模板
保留 shell-neutral task package 作为共享层，再分 Codex / Claude Code 渲染。

### 4. Memory 约定
如果你们本地 host 没有原生 Memory，就把它显式做成：
- `memory/memory-spec.md`
- 或在项目目录中使用 `00_meta/knowledge/` 类似目录代替

## 推荐迁移顺序
1. 先迁移 research 阶段模板和输出顺序
2. 再迁移 Evidence status 和 transition brief
3. 再迁移 package-codex / package-claude-code
4. 最后再考虑是否把整个 studio 目录全面替换

## 原因
你现在最需要验证的是：
- 本地 research 能不能跑通
- 本地产出的工件是不是可审阅
- 这些工件能不能顺滑接到后续开发

所以先迁移研究阶段最值。