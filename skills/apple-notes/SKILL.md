---
name: apple-notes
description: "Access Apple Notes for personal context, goals, retrospectives, checklists, and private operating notes."
---

# Apple Notes

Use this skill when the user wants context from Apple Notes or when the chief-of-staff workflow depends on local notes.

## Expected Tooling

This starter assumes a local script or MCP that can:

```bash
python3 ~/.claude/tools/apple-notes.py search "query"
python3 ~/.claude/tools/apple-notes.py read <id>
python3 ~/.claude/tools/apple-notes.py list [limit]
```

## Getting Started

If this skill is invoked and the tool does not exist yet:

1. Tell the user Apple Notes access is not configured yet.
2. Point them to `docs/integrations/apple-notes.md`.
3. Ask Claude to help them create or connect a local Apple Notes reader.
4. Keep real note IDs in local memory, not in tracked files.

## Good Use Cases

- Reading current priorities
- Looking up goals or retrospectives
- Checking recurring planning notes
- Pulling private context into a daily brief

## Rules

- Keep real note IDs in `state/insights.local.md` or another private local file, not in tracked files.
- Treat note contents as private user data.
- Summarize what matters instead of dumping long note bodies unless the user asks.

## Suggested Workflow

1. Search or read the relevant note.
2. Extract the useful signal.
3. Move durable patterns into local memory if appropriate.
