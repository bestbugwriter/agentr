# Release Checklist

Use this before sharing the repo, zipping it, or merging it into a larger codebase.

## Structure
- [ ] `instruction.md` exists and matches current workflow behavior
- [ ] `commands/` contains all intended stage entrypoints
- [ ] `skills/` and `templates/` use stable relative paths
- [ ] `examples/` contains at least one understandable sample skeleton

## Content quality
- [ ] `docs/output-order.md` matches current expected artifact order
- [ ] `docs/evidence-status.md` matches current validation standard
- [ ] host-specific prompts still depend on a shell-neutral package first
- [ ] no placeholder text remains in public-facing repo docs

## Repo hygiene
- [ ] `.gitignore` is present
- [ ] `.editorconfig` is present
- [ ] `LICENSE` is present
- [ ] no local scratch outputs or exported reports are committed unintentionally

## Before first real use
- [ ] run one research example
- [ ] run one planning example
- [ ] verify Codex and Claude Code prompts still align with the same task package
