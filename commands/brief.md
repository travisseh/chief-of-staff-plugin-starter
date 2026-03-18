---
description: "Daily brief. Pulls from configured calendar, comms, notes, and tasks to build a start-of-day action stack."
argument-hint: optional focus area or time horizon
---

# Daily Brief

Build a useful morning brief from the integrations that are actually configured.

## Read First

1. Read `state/insights.local.md` if it exists, otherwise `state/insights.template.md`.
2. Read yesterday's daily note if it exists.
3. Read `skills/executive-assistant/references/integration-registry.md`.
4. If Notion is enabled, read `skills/notion-backlog/SKILL.md`.
5. If drafting replies, read `skills/writing-style/SKILL.md`.

## Preflight

Before the sweep, identify which integrations are available:

- Calendar
- Email
- Slack
- Tasks / Notion
- Notes
- iMessage
- LinkedIn

If any configured system appears unauthenticated or broken, note it clearly in the brief.

## Gather In Parallel

Only use the sources that are enabled:

1. Calendar for today and the next 2-3 days
2. Inbox / Slack / text channels for urgent items
3. Backlog / Notion for active tasks
4. Notes for durable context and checklists

## Analyze

Identify:

- What needs a response today
- Which meetings need prep
- Which tasks are truly time-sensitive
- Which work matters most given the user's actual constraints

## Write Before Ending

Create or update `state/daily/YYYY-MM-DD.md` with:

- Action stack
- Meeting prep
- follow-ups
- new durable patterns worth preserving

## Output Format

```text
## Daily Brief - [Date]

### Right Now
[single most important next action]

### Meetings That Need Prep
- [meeting] - [prep needed]

### Needs Response Today
- [channel/person/topic] - [recommended move]

### Active Backlog
- [task] - [priority / status]

### Suggested Action Stack
1. [action]
2. [action]
3. [action]

### Missing Or Broken Inputs
- [integration or gap]
```
