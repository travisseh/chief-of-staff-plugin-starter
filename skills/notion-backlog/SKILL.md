---
name: notion-backlog
description: "Manage a Notion task backlog for the chief-of-staff workflow. Use when reading tasks, creating follow-ups, updating task status, or syncing brief outputs into a task system."
---

# Notion Backlog

Use this skill when the chief-of-staff workflow needs a real task system.

## Recommended Setup

- Use the official Notion MCP connection described in `docs/integrations/notion.md`
- Store the real database URL or data source ID in local memory, not in shared public files, if it reveals private workspace structure

## Suggested Schema

This starter works best when the task database has fields similar to:

| Property | Type | Example |
| --- | --- | --- |
| Name | title | Follow up with design partner |
| Status | select | Backlog, To Do, In Progress, Review, Done |
| Assignee | select | Me, Chief of Staff, Marketing, Ops |
| Area | select | Work, Family, Health, Admin, Side Project |
| Initiative | select | Launch, Sales, Hiring, Personal Admin |
| Priority | select | P0 - Today, P1 - This Week, P2 - Soon, P3 - Later |
| Due | date | optional |
| Notes | rich text or page body | optional |

## Core Workflow

### Read Tasks

1. Find the backlog database or page using Notion MCP.
2. Pull active tasks first:
   - Backlog
   - To Do
   - In Progress
   - Review
3. Group tasks by status and priority before recommending what to do next.

### Create Tasks

Create backlog items for:

- follow-ups surfaced in a comms sweep
- meeting prep that should not be forgotten
- decisions that require a later action
- non-trivial admin work

At minimum set:

- Name
- Status
- Assignee
- Area

### Update Tasks

When work starts, move the task to `In Progress`.

When the work is complete, move it to `Done` or `Review`.

When new context matters, update the page body with:

- what changed
- what was decided
- what is still blocked

## Decision Rules

- Not every message becomes a task. Quick replies should stay quick replies.
- Create a task when the work is multi-step, time-sensitive, or easy to drop.
- Prefer one good task with clear notes over five vague tasks.
