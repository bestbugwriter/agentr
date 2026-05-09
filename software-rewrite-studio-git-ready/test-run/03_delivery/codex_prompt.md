# Codex Prompt

Use the attached files as the source of truth:
- `01_research/selected_opportunity_evaluation.md`
- `02_planning/transition_brief.md`
- `02_planning/mvp_scope.md`
- `02_planning/architecture_outline.md`
- `03_delivery/shell_neutral_task_package.md`

Start with task `BUG-BOOT-001`, then continue into `BUG-CAP-002` only if the foundation stays within MVP scope.

## Objective
Bootstrap an AI-first visual bug reporting copilot for small software teams and agencies. The product should begin as a Chrome-extension-led workflow that captures website bugs and turns them into developer-ready GitHub issues with AI assistance.

## Required outputs
Create or update:
- `README.md`
- `docs/product-overview.md`
- `docs/architecture.md`
- `web/`
- `extension/`
- `shared/`

## MVP scope
Include support for:
- screenshot capture from the active tab
- page metadata collection
- optional console log capture
- structured AI report generation foundation
- report review UI foundation
- GitHub export foundation

## Constraints
- Keep the scope MVP-only
- Prioritize screenshot capture over recording
- Support GitHub before any other tracker
- Default to conservative privacy behavior
- Use structured output for AI-generated reports

## Acceptance criteria
- project foundation exists
- boundaries between web, extension, shared, and server logic are clear
- report schema is documented
- in-scope versus deferred work is explicit
- assumptions are stated briefly before implementation

## Output style
- Be direct
- Prefer concrete file creation over long explanation
- Keep implementation aligned with the task package
