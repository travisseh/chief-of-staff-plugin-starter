# Notion Setup

## Recommended Path

Use the official hosted Notion MCP server.

## Official References

- Notion MCP overview: https://developers.notion.com/docs/mcp
- Connect Notion MCP to Claude Code: https://developers.notion.com/guides/mcp/get-started-with-mcp
- Internal integration auth: https://developers.notion.com/docs/authorization

## Fastest Setup

Run:

```bash
claude mcp add --transport http notion https://mcp.notion.com/mcp
```

Then:

1. Run `/mcp` in Claude Code.
2. Authenticate through the OAuth flow.
3. Grant access to the workspace content you want Claude to use.

## Important Notes

- Notion's official docs recommend the hosted MCP for most users.
- If you use an internal integration instead, you must still share the specific pages or databases with that integration.
- For headless automation, a self-hosted server or direct Notion API integration may still be useful, but it adds more setup and secret management.

## Verification

Ask Claude Code:

```text
Search my Notion workspace for a page titled "Tasks" and summarize the open items.
```

Then wire the task conventions into [skills/notion-backlog/SKILL.md](../../skills/notion-backlog/SKILL.md) or keep the real database details in `state/insights.local.md`.
