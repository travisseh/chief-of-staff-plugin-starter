# Slack Setup

## What You Need

- A Slack app installed in each workspace you want to use
- A user OAuth token for each workspace
- A local CLI or MCP wrapper Claude can call

## Official References

- Slack auth overview: https://api.slack.com/authentication
- Slack token types: https://api.slack.com/concepts/token-types

## Token Type

This starter assumes **user tokens** so reads and sends happen as you.

Slack user tokens begin with:

```text
xoxp-
```

## Typical User Scopes

Choose the minimum set you actually need. A common starting set is:

- `channels:read`
- `channels:history`
- `groups:read`
- `groups:history`
- `im:read`
- `im:history`
- `mpim:read`
- `mpim:history`
- `chat:write`
- `search:read`
- `users:read`

## Suggested Local CLI Shape

```bash
node ~/.config/slack-tools/slack.js add-workspace <nickname> <xoxp-token>
node ~/.config/slack-tools/slack.js summary
node ~/.config/slack-tools/slack.js unreads <nickname>
node ~/.config/slack-tools/slack.js messages <nickname> "<channel>" 20
node ~/.config/slack-tools/slack.js send <nickname> "<channel-or-user>" "message"
```

## Verification

1. Connect one workspace first.
2. Run an unread summary.
3. Read a known DM or channel.
4. Draft a response.
5. Only then allow sends.
