# SHELL-NEUTRAL TASK PACKAGE

## Task ID
BUG-BOOT-001

## Title
Bootstrap an AI-first visual bug reporting copilot MVP

## Goal
Create the first working foundation for a browser-extension-led SaaS that captures website bugs and turns them into developer-ready reports with AI assistance.

## Business context
The product targets small software teams and agencies that repeatedly lose time turning screenshots, recordings, and vague QA feedback into reproducible engineering tickets. The MVP should validate whether users will pay for a lighter, faster, GitHub-first alternative to broader visual feedback tools.

## Related documents
- `02_planning/transition_brief.md`
- `02_planning/mvp_scope.md`
- `02_planning/architecture_outline.md`

## Target files or modules
- `README.md`
- `web/`
- `extension/`
- `shared/`
- `docs/product-overview.md`
- `docs/architecture.md`

## Constraints
- Keep scope MVP-only
- Prioritize screenshot capture before recording
- Support GitHub export only
- Default to conservative privacy settings
- Use structured AI output, not free-form summary blobs

## Acceptance criteria
- Monorepo or equivalent project foundation exists
- Web app, extension, and shared type boundaries are clear
- Report ingestion flow is defined
- AI report schema is defined
- In-scope versus deferred scope is explicit in docs

## Expected evidence
- Scaffolded project structure
- Product overview document
- Architecture document
- Shared schema for reports
- Working notes on assumptions and privacy limits

## Dependencies
- Transition brief accepted as the working direction

---

# BUG-CAP-002 Extension capture MVP

## Goal
Implement Chrome extension capture for screenshot, note entry, and basic page metadata.

## Business context
This is the product's front door. If capture feels slow or confusing, the rest of the workflow does not matter.

## Related documents
- `02_planning/mvp_scope.md`
- `02_planning/architecture_outline.md`

## Target files or modules
- `extension/src/background`
- `extension/src/content`
- `extension/src/popup`
- `shared/report-schema`

## Constraints
- Start with screenshot only
- Capture URL, viewport, browser info, and optional console logs
- Avoid collecting cookies, localStorage, or full request bodies

## Acceptance criteria
- User can trigger capture from the active tab
- User can attach a short note
- Extension produces a normalized payload for upload

## Expected evidence
- Extension UI flow
- Example normalized payload
- Screenshot artifact upload or local mock

## Dependencies
- `BUG-BOOT-001`

---

# BUG-AI-003 Structured AI writer

## Goal
Generate a structured bug report from the uploaded artifacts and metadata.

## Business context
The AI layer is the product wedge. It must produce cleaner tickets than manual reporting, not just a verbose summary.

## Related documents
- `01_research/selected_opportunity_evaluation.md`
- `02_planning/architecture_outline.md`

## Target files or modules
- `server/ai`
- `shared/ai-schema`
- `web/app/reports/[id]`

## Constraints
- Use a fixed output schema
- Include title, summary, repro steps, expected result, actual result, severity hint
- Allow human edits after generation

## Acceptance criteria
- Uploaded capture can be transformed into the fixed report schema
- Invalid model output is retried or rejected safely
- User can review and edit the generated fields

## Expected evidence
- Prompt template
- Structured schema definition
- Example generated report JSON

## Dependencies
- `BUG-CAP-002`

---

# BUG-EXP-004 GitHub-first export

## Goal
Export a finalized structured bug report into a GitHub issue.

## Business context
A GitHub-first workflow keeps the MVP tightly aligned with engineering teams and avoids early integration sprawl.

## Related documents
- `02_planning/transition_brief.md`

## Target files or modules
- `server/integrations/github`
- `web/app/reports/[id]/export`

## Constraints
- GitHub only
- Use a deterministic issue template
- Keep auth and repo selection simple

## Acceptance criteria
- User can connect a repository
- User can preview the issue body
- System creates the issue successfully and stores the export result

## Expected evidence
- Export UI
- Issue template mapping
- Successful issue creation log or screenshot

## Dependencies
- `BUG-AI-003`

---

# BUG-PRIV-005 Privacy controls

## Goal
Add opt-in capture controls and baseline redaction so the product is usable on semi-sensitive pages.

## Business context
Privacy concerns are one of the fastest ways to lose trust in this category. Guardrails are part of the core product, not polish.

## Related documents
- `02_planning/mvp_scope.md`
- `01_research/selected_opportunity_evaluation.md`

## Target files or modules
- `extension/src/settings`
- `server/redaction`
- `web/app/settings`

## Constraints
- Ship with conservative defaults
- Make every high-risk field explicitly opt-in
- Do not promise enterprise-grade compliance in the MVP

## Acceptance criteria
- User can see what is captured
- High-risk data collection is disabled by default
- Stored reports reflect the enabled capture policy

## Expected evidence
- Settings UI
- Redaction policy doc
- Before/after sample payload

## Dependencies
- `BUG-CAP-002`
