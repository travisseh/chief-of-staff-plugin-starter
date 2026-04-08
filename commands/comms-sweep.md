---
description: "Comms sweep. Finds messages that are likely waiting on the user's reply across configured channels."
argument-hint: optional time horizon
---

# Comms Sweep

Find the conversations that are waiting on the user, not just the ones that are unread.

## Read First

1. Read `state/insights.local.md` if it exists, otherwise `state/insights.template.md`.
2. Read `skills/executive-assistant/references/integration-registry.md`.
3. Read `skills/writing-style/SKILL.md` before drafting replies.

## Rules

- Use only configured channels.
- Exclude spam, automated notifications, newsletters, and cold outreach unless the user explicitly wants them.
- Prefer direct asks, pending decisions, or unanswered threads.
- Read the actual thread before drafting a reply.
- Draft first. Send only with approval.

## Channels

Check any of these that are enabled:

- Gmail or equivalent email tool
- Slack or equivalent workspace messaging tool
- iMessage
- LinkedIn messages

## Output Format

```text
## Comms Sweep - [Date]

### Urgent
- [channel] [person] - [what they need]
  Suggested reply: [draft]

### Normal Priority
- [channel] [person] - [what they need]
  Suggested reply: [draft]

### Can Wait
- [channel] [person] - [why]
```
