# Chief of Staff Plugin Starter

This repo is a sanitized starter for building a personal chief-of-staff workflow in Claude Code.

It gives you:

- A plugin-style folder structure for commands, skills, and agents
- A reusable daily brief and comms sweep workflow
- Self-contained backlog and writing-style skills, so the repo does not depend on your global `.claude/skills` folder
- Setup docs for Google Calendar, Gmail, Slack, Notion, Apple Notes, iMessage, and LinkedIn
- Install and update guidance for the Claude Code plugin flow, including cache and version-bump gotchas
- Prompt files you can paste directly into Claude Code to personalize the system

It does **not** ship with your real data, tokens, phone numbers, note IDs, or account names.

## Fastest Path

1. Open this repo in Claude Code.
2. If you want to load it as a real Claude Code plugin, start with [00-install-or-update-plugin.md](./docs/prompts/00-install-or-update-plugin.md).
3. Read [CLAUDE.md](./CLAUDE.md).
4. Paste [01-personalize-chief-of-staff.md](./docs/prompts/01-personalize-chief-of-staff.md) into Claude Code.
5. Let Claude create your private `state/insights.local.md`.
6. Paste [02-connect-integrations.md](./docs/prompts/02-connect-integrations.md) to wire in the integrations you want.
7. Paste [03-first-brief.md](./docs/prompts/03-first-brief.md) to run your first real brief.

## Repo Structure

```text
chief-of-staff-plugin-starter/
├── .claude-plugin/plugin.json
├── CLAUDE.md
├── README.md
├── agents/
├── commands/
├── docs/
│   ├── integrations/
│   └── prompts/
├── skills/
│   ├── apple-notes/
│   ├── executive-assistant/
│   ├── errands/
│   ├── imessage/
│   ├── linkedin/
│   ├── linkedin-voice/
│   ├── notion-backlog/
│   ├── slack/
│   ├── stripe/
│   └── writing-style/
└── state/
    ├── daily/
    └── insights.template.md
```

## Required vs Optional

You can start with just Claude Code plus a personalized `state/insights.local.md`.

Optional integrations make it materially better:

| Integration | Needed For | Secret / Credential |
| --- | --- | --- |
| Google Calendar MCP | Schedule visibility and event creation | Google OAuth desktop credentials JSON |
| Gmail CLI or equivalent | Inbox scan, read, draft, reply | Google OAuth desktop credentials JSON |
| Slack CLI or equivalent | Multi-workspace scans and replies | Slack user OAuth token (`xoxp-...`) |
| Notion MCP | Task / backlog management | Usually OAuth via official Notion MCP; token only if self-hosting |
| Apple Notes | Personal context and recurring checklists | No API key; local macOS access |
| iMessage CLI | Text-message awareness and sending | No API key; local macOS access + Full Disk Access |
| LinkedIn via browser automation | Inbox follow-up and notifications | No API key; logged-in browser session |

## Setup Docs

- [Setup overview](./docs/setup.md)
- [Google Calendar](./docs/integrations/google-calendar.md)
- [Gmail](./docs/integrations/gmail.md)
- [Slack](./docs/integrations/slack.md)
- [Notion](./docs/integrations/notion.md)
- [Apple Notes](./docs/integrations/apple-notes.md)
- [iMessage](./docs/integrations/imessage.md)
- [LinkedIn](./docs/integrations/linkedin.md)

## Installation Notes

If you just want the prompts and file structure, you can keep this repo anywhere and open it as a normal repo in Claude Code.

If you want to run it as a real Claude Code plugin, keep these gotchas in mind:

- For the fastest iteration loop, use `claude --plugin-dir /absolute/path/to/chief-of-staff-plugin-starter`. That loads the source repo directly for that session.
- Cloning into `~/.claude/plugins/` is only a filesystem step. An installed plugin still needs the normal Claude Code `/plugin install` flow through a marketplace.
- Do not manually edit `~/.claude/plugins/installed_plugins.json`.
- Run `/plugin validate .` from the repo root before blaming the manifest.
- Installed plugins are cached copies. After changing commands, skills, agents, or other tracked plugin files, bump `.claude-plugin/plugin.json`, update or reinstall the plugin, and restart Claude Code.
- If you create a local marketplace entry for this plugin, keep the marketplace version in sync with `.claude-plugin/plugin.json`.

## Safety Rules

- Never commit real tokens, OAuth JSON files, or private daily notes.
- Treat outbound sending as privileged. Draft first, send second.
- Pause before purchases, scheduling commitments, or posting publicly.
- Keep your private state in `state/insights.local.md`, which is gitignored.

## Personalization Checklist

Before you rely on this day-to-day, make sure Claude knows:

- Your actual life and work areas
- Your protected time blocks
- Your priority hierarchy
- Your writing style
- Which integrations are enabled
- Which actions need approval
- What “urgent” means in your world
