# Apple Notes Setup

## What You Need

- macOS
- Notes app syncing the content you want to use
- Local access to the Notes database

## Credentials

No API key is required.

## Expected Access Pattern

This starter assumes a small local script or MCP that can:

```bash
python3 ~/.claude/tools/apple-notes.py read <id>
python3 ~/.claude/tools/apple-notes.py search "query"
```

## Notes

- This is macOS-specific.
- Keep note IDs out of public shared files if they reveal private structure.
- Good use cases: weekly plans, recurring checklists, private reference notes.

## Verification

Read one safe note first and confirm the formatting is usable in Claude Code.
