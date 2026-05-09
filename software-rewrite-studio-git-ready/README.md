# Software Rewrite Studio

A git-ready local package for discovering, evaluating, planning, and packaging AI software rewrite opportunities.

## What this repo is for
- Research software categories worth rebuilding with AI
- Evaluate specific products and platform gaps
- Turn high-potential opportunities into MVP and implementation plans
- Package the result for Codex, Claude Code, or similar coding shells

## Repo structure
- `instruction.md`: core agent/system behavior for the local workflow
- `memory/`: reusable memory rules and durable research patterns
- `commands/`: stage entrypoints
- `skills/`: reusable workflow modules
- `templates/`: standard output artifacts by stage
- `docs/`: host compatibility, operating notes, and release guidance
- `examples/`: sample project skeletons

## Recommended flow
1. Read `instruction.md`
2. Pick one entry in `commands/`
3. Produce outputs using `skills/` and `templates/`
4. Check `docs/output-order.md` and `docs/evidence-status.md`
5. If ready, move from research -> evaluate -> plan -> package

## Fast start
- Start with `docs/GETTING-STARTED.md`
- Use `commands/rewrite-research.md` for category discovery
- Use `commands/rewrite-plan.md` once one target is clearly strong
- Use `commands/rewrite-package-codex.md` or `commands/rewrite-package-claude-code.md` for final delivery

## Git usage
This folder is structured to be dropped directly into a repository root.
If you already have a repo, copy the contents in and keep the same relative paths.

Recommended first commit shape:
1. repo scaffolding
2. instructions + commands + skills
3. templates + examples
4. first real research pass

## Repo hygiene included
- `.gitignore`
- `LICENSE`
- `.editorconfig`
- startup docs in `docs/`
- release checklist in `docs/RELEASE-CHECKLIST.md`
- working conventions in `docs/WORKING-CONVENTIONS.md`

## Suggested next step
If you want to use this as a real repository immediately:
1. initialize Git in this folder
2. make the first scaffold commit
3. run one end-to-end example from research to package
4. only then merge it into a larger existing repo if needed
