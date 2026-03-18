---
name: slack
description: "Read and send Slack messages across one or more workspaces using local tools."
---

# Slack

Use local Slack tools for workspace summaries, message history, search, and replies.

## Expected Tooling

This starter assumes commands like:

```bash
node ~/.config/slack-tools/slack.js workspaces
node ~/.config/slack-tools/slack.js summary
node ~/.config/slack-tools/slack.js unreads [workspace]
node ~/.config/slack-tools/slack.js messages <workspace> "<channel>" [limit]
node ~/.config/slack-tools/slack.js thread <workspace> "<channel>" <ts>
node ~/.config/slack-tools/slack.js send <workspace> "<channel-or-user>" "message"
node ~/.config/slack-tools/slack.js search <workspace> "query"
```

## Getting Started

If this skill is invoked and the tool does not exist yet:

1. Tell the user Slack tools are not configured yet.
2. Point them to `docs/integrations/slack.md`.
3. Explain they will need:
   - a Slack app
   - user OAuth tokens for each workspace they want to use
   - a local CLI at `~/.config/slack-tools/slack.js` or equivalent
4. Start with `workspaces`, `summary`, and `unreads` before enabling sends.

## Recommended Workflow

1. Check `summary` first.
2. Drill into the workspace with activity.
3. Read full context before replying.
4. Draft the response.
5. Send only with approval.

## Rules

- Keep workspace nicknames and channel conventions in local memory, not hard-coded into shared files.
- Use `skills/writing-style/SKILL.md` for message tone.
- Be careful with thread replies vs top-level messages.
