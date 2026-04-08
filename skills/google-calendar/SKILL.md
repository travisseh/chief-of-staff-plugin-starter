---
name: google-calendar
description: "Read and manage Google Calendar via MCP. Use when checking the day's schedule, finding free time, looking up upcoming events, creating or updating events, or pulling calendar context into a daily brief."
---

# Google Calendar

Use this skill when the chief-of-staff workflow needs calendar context — daily briefs, free-time lookups, scheduling, or event creation.

## Expected Tooling

This starter assumes the `@cocal/google-calendar-mcp` MCP server is connected. See `docs/integrations/google-calendar.md` and `skills/executive-assistant/references/integration-registry.md` for setup.

Core MCP tools:

- `list-calendars`
- `list-events`
- `search-events`
- `create-event`
- `update-event`

## Getting Started

If this skill is invoked and the MCP server is not configured yet:

1. Tell the user Google Calendar access is not configured yet.
2. Point them to `docs/integrations/google-calendar.md`.
3. Offer to walk them through `claude mcp add google-calendar ...`.

## Good Use Cases

- Today and next 2-3 days of events for a daily brief
- Finding free blocks for focused work
- Looking up a specific meeting or attendee
- Creating or rescheduling events on request

## Rules

- Never create, update, or delete events without explicit user confirmation.
- Show event title, time, attendees, and location before any change.
- Default to read-only when pulling context for a brief.
- Summarize the schedule instead of dumping every field unless asked.

## Suggested Workflow

1. List calendars once to confirm which to query.
2. Pull events for the relevant window.
3. Summarize conflicts, prep needs, and free blocks.
4. Only mutate the calendar after confirmation.
