# Integration Registry

This file describes the integrations the starter plugin expects. Replace placeholders with your own setup as you personalize the system.

## Google Calendar

Recommended approach: MCP server via Claude Code.

- Anthropic MCP docs: https://docs.anthropic.com/en/docs/claude-code/mcp
- Package used in this starter: https://www.npmjs.com/package/%40cocal/google-calendar-mcp
- Google Calendar quickstart: https://developers.google.com/workspace/calendar/api/quickstart/go

Example add command:

```bash
claude mcp add google-calendar --scope user --env GOOGLE_OAUTH_CREDENTIALS=$HOME/.config/google-calendar-mcp/gcp-oauth.keys.json -- npx -y @cocal/google-calendar-mcp
```

Core tools:

- `list-calendars`
- `list-events`
- `search-events`
- `create-event`
- `update-event`

## Gmail

This starter assumes a small local CLI for Gmail. You can keep the same command shape or replace it with your own equivalent.

- Google Gmail quickstart: https://developers.google.com/workspace/gmail/api/quickstart/go
- Google Workspace API enablement: https://developers.google.com/workspace/guides/enable-apis

Expected command shape:

```bash
node ~/.config/gmail-tools/gmail.js unread <account> 20
node ~/.config/gmail-tools/gmail.js search <account> "query" 20
node ~/.config/gmail-tools/gmail.js read <account> "query"
node ~/.config/gmail-tools/gmail.js reply <account> "query" "body"
```

Expected credentials:

- Google OAuth desktop client JSON
- Per-account OAuth tokens stored locally

## Slack

- Slack auth docs: https://api.slack.com/authentication
- Slack token types: https://api.slack.com/concepts/token-types

Expected command shape:

```bash
node ~/.config/slack-tools/slack.js summary
node ~/.config/slack-tools/slack.js unreads <workspace>
node ~/.config/slack-tools/slack.js messages <workspace> "<channel>" 20
node ~/.config/slack-tools/slack.js send <workspace> "<channel-or-user>" "message"
```

Expected credential:

- Slack user OAuth token (`xoxp-...`) per workspace

## Notion

Recommended approach: official hosted Notion MCP.

- Notion MCP overview: https://developers.notion.com/docs/mcp
- Claude Code connection guide: https://developers.notion.com/guides/mcp/get-started-with-mcp

Example add command:

```bash
claude mcp add --transport http notion https://mcp.notion.com/mcp
```

Expected auth:

- OAuth inside Claude Code via `/mcp`

Optional self-hosted path:

- Notion local MCP notes: https://developers.notion.com/guides/mcp/hosting-open-source-mcp

## Apple Notes

Expected access pattern:

```bash
python3 ~/.claude/tools/apple-notes.py read <id>
python3 ~/.claude/tools/apple-notes.py search "query"
```

Credential:

- No API key
- macOS local database access

## iMessage

Expected access pattern:

```bash
node ~/.config/imessage-tools/imessage.js unreads 20
node ~/.config/imessage-tools/imessage.js messages "Person" 20
node ~/.config/imessage-tools/imessage.js send "+1XXXXXXXXXX" "message"
```

Credential:

- No API key
- macOS local database access
- Full Disk Access for your terminal app

## LinkedIn

Expected access pattern:

- Browser automation only
- Logged-in browser session

Credential:

- No API key in this starter
- Active browser session

## Personalization Notes

As you customize this starter, add:

- Real account nicknames
- Real workspaces
- Real note IDs
- Any custom CLIs you build
- Any channels or people that always matter
