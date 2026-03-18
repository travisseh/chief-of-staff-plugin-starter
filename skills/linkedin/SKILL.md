---
name: linkedin
description: "Check and respond to LinkedIn messages and notifications through browser automation."
---

# LinkedIn Messages

Use browser automation to inspect LinkedIn inboxes and notifications.

## Getting Started

If this skill is invoked and browser automation is not configured yet:

1. Tell the user LinkedIn browser automation is not configured yet.
2. Point them to `docs/integrations/linkedin.md`.
3. Explain they will usually need:
   - a browser automation tool connected to Claude Code
   - an active logged-in LinkedIn session
4. Start with reading the inbox before enabling replies.

## Read First

- `skills/writing-style/SKILL.md`
- `skills/linkedin-voice/SKILL.md` when the task is a post, comment, or longer-form LinkedIn writing

## Workflow

1. Open LinkedIn messages.
2. Read current conversations.
3. Identify anything waiting on the user's reply.
4. Draft responses in the user's style.
5. Pause for approval before sending.

## Output Format

```text
## LinkedIn

### Needs Response
- [person] - [summary]

### FYI
- [person] - [summary]

### Drafts
- [draft]
```
