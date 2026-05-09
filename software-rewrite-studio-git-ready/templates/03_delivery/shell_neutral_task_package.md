# SHELL-NEUTRAL TASK PACKAGE

## Task ID
FIN-BOOT-001

## Title
Bootstrap an Android-first personal finance assistant MVP

## Goal
Create the first working foundation for an Android-first personal finance assistant inspired by premium iOS finance apps, with a focus on net worth overview, budgeting insights, subscription tracking, billing reminders, and AI-generated summaries.

## Business context
The product is positioned as a premium Android personal finance assistant for users who want a clearer and more actionable view of their finances than basic expense trackers provide. The first release should validate whether users value unified financial visibility and AI-generated guidance enough to pay.

## Related documents
- `transition-brief.md`

## Target files or modules
Suggested structure:
- `README.md`
- `docs/product-overview.md`
- `docs/architecture.md`
- `app/` or equivalent Android app root
- `backend/` or equivalent API/service root
- `shared/` or equivalent common models

## Constraints
- Keep scope MVP-level
- Prefer a modular architecture that can support future bank aggregation, but do not overbuild upfront
- Optimize for a fast prototype over enterprise completeness
- Make privacy and security expectations explicit in product and architecture docs
- If a real financial data integration is not yet ready, allow mocked or manual data entry paths for the MVP

## Acceptance criteria
- A clear MVP structure exists for the Android-first finance assistant
- The project includes a documented product overview and technical architecture
- Core MVP modules are defined: accounts/assets, net worth, budgeting, subscriptions/bills, AI summary
- The implementation plan explicitly distinguishes in-scope vs out-of-scope work
- The foundation is suitable for further task splitting into frontend, backend, and AI summary work

## Expected evidence
- File tree or scaffolded project structure
- Product overview document
- Architecture summary document
- List of core modules and responsibilities
- Notes on assumptions and open risks

## Dependencies
- Transition brief approved as the working direction

---

## Recommended next tasks
### FIN-FEAT-002
Implement manual account and asset input flow

### FIN-FEAT-003
Implement net worth dashboard and trend view

### FIN-FEAT-004
Implement budgeting categories and overspend alerts

### FIN-FEAT-005
Implement subscription detection model and bill reminder flow

### FIN-FEAT-006
Implement AI weekly/monthly finance summary generation
