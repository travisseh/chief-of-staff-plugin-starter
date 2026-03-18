# Google Calendar Setup

## What You Need

- A Google account with Calendar enabled
- A Google Cloud project
- Calendar API enabled
- OAuth 2.0 Desktop App credentials JSON

## Official References

- Google Calendar quickstart: https://developers.google.com/workspace/calendar/api/quickstart/go
- Google Workspace API enablement: https://developers.google.com/workspace/guides/enable-apis
- Claude Code MCP docs: https://docs.anthropic.com/en/docs/claude-code/mcp
- MCP package used in this starter: https://www.npmjs.com/package/%40cocal/google-calendar-mcp

## Setup

1. In Google Cloud, create or pick a project.
2. Enable the Google Calendar API.
3. Configure the OAuth consent screen if prompted.
4. Create an OAuth client with application type `Desktop app`.
5. Download the credentials JSON.
6. Save it to:

```bash
~/.config/google-calendar-mcp/gcp-oauth.keys.json
```

7. Add the MCP server in Claude Code:

```bash
claude mcp add google-calendar --scope user --env GOOGLE_OAUTH_CREDENTIALS=$HOME/.config/google-calendar-mcp/gcp-oauth.keys.json -- npx -y @cocal/google-calendar-mcp
```

8. Complete the auth flow when Claude Code asks for it.

## Notes

- If your Google OAuth app is still in test mode, refresh tokens may expire quickly.
- The MCP package documentation notes that `GOOGLE_OAUTH_CREDENTIALS` is important when using `npx`.

## Verification

Ask Claude Code:

```text
List my calendars and show today's events.
```
