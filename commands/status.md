---
description: "Quick dashboard. Shows today's schedule, unread pressure, and current priorities at a glance."
argument-hint: optional focus area
---

# Status Dashboard

Run a quick scan using whichever sources are configured.

## Steps

1. Read `state/insights.local.md` if it exists, otherwise `state/insights.template.md`.
2. Check today's calendar if enabled.
3. Check email / Slack / iMessage unread summaries if enabled.
4. Check the current task list or notes for declared priorities.

## Output Format

```text
## Dashboard - [Date]

### Schedule
[today's events]

### Comms Pressure
- Email: [summary]
- Slack: [summary]
- Texts: [summary]

### Current Focus
[what memory says matters this week]

### Flagged
- [urgent item]
```
