# Workflow Entrypoints Draft

## 1. rewrite-research
目标：从一个赛道、功能类别或平台空白出发，完成研究阶段工件。

### 输入示例
- 找 iOS 有、Android 没有、用户愿意付费的软件机会
- 扫描个人财务赛道里值得 AI 重写的软件

### 默认输出
1. Source strategy
2. Opportunity candidates
3. Source log
4. Opportunity scorecard
5. Initial assessment report
6. Evidence status
7. Top 3 与实施衔接建议

## 2. rewrite-evaluate
目标：对单个产品或多个候选做更明确的机会判断。

### 输入示例
- 评估 Copilot Money 是否值得做 Android 替代
- 对比 3 个个人财务产品，判断谁最值得先做

### 默认输出
- 结构化评分
- 风险与证据状态
- 是否进入实施规划

## 3. rewrite-plan
目标：把高分候选转成实施规划。

### 最小交接信息
- Target
- Why now
- Core wedge
- Target user
- MVP recommendation
- Key risks
- Evidence status

### 默认输出
- Transition brief
- MVP scope
- 技术方案
- 架构概要
- 开发任务清单

## 4. rewrite-package-codex
目标：把规划结果转成 Codex 可执行交付。

### 默认输出
- shell-neutral task package
- Codex prompt

## 5. rewrite-package-claude-code
目标：把规划结果转成 Claude Code 可执行交付。

### 默认输出
- shell-neutral task package
- Claude Code prompt

## 阶段衔接规则
- `rewrite-research` 结束后，只有当高分候选足够明确，才进入 `rewrite-plan`
- 如果证据状态里“未完全验证”会影响实施判断，应停留在 research / evaluate
- `rewrite-plan` 完成后，才能进入 `rewrite-package-codex` 或 `rewrite-package-claude-code`

## 为什么这样拆
因为你的目标不是只让本地工具接开发任务，而是让它们从研究阶段就能运行。把入口拆开后，Codex 和 Claude Code 都更容易在每个阶段保持上下文清晰。