# Gmail Setup

## What You Need

- Gmail enabled on the account you want Claude to inspect
- A Google Cloud project
- Gmail API enabled
- OAuth 2.0 Desktop App credentials JSON
- A local CLI or MCP wrapper that Claude can call

## Official References

- Gmail quickstart: https://developers.google.com/workspace/gmail/api/quickstart/go
- Google Workspace API enablement: https://developers.google.com/workspace/guides/enable-apis

## Credentials

This starter assumes the same Google OAuth desktop credentials JSON can be reused for Gmail and Calendar.

Save the JSON to:

```bash
~/.config/google-calendar-mcp/gcp-oauth.keys.json
```

## Suggested Local CLI Shape

This repo does not bundle your Gmail CLI, but it assumes commands like:

```bash
node ~/.config/gmail-tools/gmail.js add <nickname>
node ~/.config/gmail-tools/gmail.js unread <nickname> 20
node ~/.config/gmail-tools/gmail.js search <nickname> "query" 20
node ~/.config/gmail-tools/gmail.js read <nickname> "query"
node ~/.config/gmail-tools/gmail.js reply <nickname> "query" "body"
```

## Recommended Scopes

Your local Gmail tool will usually need scopes equivalent to:

- `gmail.readonly`
- `gmail.send`
- `gmail.modify`

## Verification

Test in this order:

1. List unread email read-only.
2. Search for a known thread.
3. Read a full thread.
4. Draft a reply.
5. Only after that, enable actual send or reply commands.

## Important Rule

If your tool supports threaded replies, use the reply command for existing threads instead of creating a brand-new email.
