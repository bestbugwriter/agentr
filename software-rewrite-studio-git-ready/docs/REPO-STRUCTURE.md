# Repo Structure

```text
software-rewrite-studio/
├── README.md
├── LICENSE
├── .gitignore
├── instruction.md
├── memory/
├── commands/
├── skills/
├── templates/
├── docs/
└── examples/
```

## Design intent
- `commands/` defines stage entrypoints
- `skills/` defines reusable execution modules
- `templates/` defines stable artifact formats
- `docs/` explains host behavior and repo usage
- `examples/` shows how to organize a real run

## Git guidance
Treat this repo as a workflow repo, not just a prompt dump.
Each stage should leave behind explicit artifacts that can be reviewed, versioned, and handed off.
