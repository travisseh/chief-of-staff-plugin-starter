---
name: imessage
description: "Read and send iMessages using local tools. Use for unread texts, contact lookup, message history, and sending messages."
---

# iMessage

Use local iMessage tools for text-message workflows.

## Expected Tooling

This starter assumes commands similar to:

```bash
node ~/.config/imessage-tools/imessage.js unreads [limit]
node ~/.config/imessage-tools/imessage.js search-contacts "query"
node ~/.config/imessage-tools/imessage.js messages "Person or Group" [limit]
node ~/.config/imessage-tools/imessage.js groups
node ~/.config/imessage-tools/imessage.js send "+1XXXXXXXXXX" "message"
```

## Getting Started

If this skill is invoked and the tool does not exist yet:

1. Tell the user iMessage tools are not configured yet.
2. Point them to `docs/integrations/imessage.md`.
3. Explain they will usually need:
   - macOS
   - Messages configured
   - Full Disk Access for the terminal app
   - a local CLI at `~/.config/imessage-tools/imessage.js` or equivalent
4. Help them set up read-only commands before enabling sends.

## Why Local Tools

Local database-backed tools are usually more reliable than flaky AppleScript or MCP-only approaches.

## Rules

- Always resolve the right contact before sending.
- Prefer sending by phone number or exact contact identifier if your local tool requires it.
- Do not send the same message twice if delivery is uncertain.
- Draft first, send second.

## Permissions

The terminal app may need:

- Full Disk Access
- Automation permission for Messages

## Writing Style

When drafting texts, also read `skills/writing-style/SKILL.md`.
