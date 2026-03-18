# Setup Overview

The safest rollout is incremental.

## Step 0: Decide How You Want To Run It

- Fastest path for development and personalization: run `claude --plugin-dir /absolute/path/to/chief-of-staff-plugin-starter`.
- If you want it installed inside Claude Code's plugin system, use a local marketplace plus `/plugin install`. Cloning the repo into `~/.claude/plugins/` by itself is not the full install flow.
- Never edit `~/.claude/plugins/installed_plugins.json` manually.
- Before install or update, run `/plugin validate .` if that command is available.
- If you change tracked plugin files after install, bump `.claude-plugin/plugin.json`, update or reinstall the plugin, and restart Claude Code because installed plugins are cached copies.

## Step 1: Personalize The Memory

- Open the repo in Claude Code.
- Paste [01-personalize-chief-of-staff.md](./prompts/01-personalize-chief-of-staff.md).
- Let Claude create `state/insights.local.md`.

## Step 2: Add Read-Only Integrations First

Recommended order:

1. Google Calendar
2. Gmail
3. Slack
4. Notion
5. Apple Notes
6. iMessage
7. LinkedIn browser automation

Start with read-only checks before you enable send, write, or create actions.

## Step 3: Update The Integration Registry

Replace the placeholders in [integration-registry.md](../skills/executive-assistant/references/integration-registry.md) with:

- your account nicknames
- your real command paths
- your enabled tools
- your note IDs or database IDs

If this repo is running as an installed plugin instead of via `claude --plugin-dir`, remember that edits to tracked files can require a version bump, plugin update or reinstall, and a Claude Code restart before they take effect.

## Step 4: Run A First Brief

Paste [03-first-brief.md](./prompts/03-first-brief.md) into Claude Code and let it tell you what is missing.

## Step 5: Tighten

Improve the system only after the first real run:

- refine filters
- refine priority tiers
- add important people and channels
- add writing-style rules
- add stronger send / scheduling guardrails
- tailor `skills/notion-backlog`, `skills/writing-style`, and `skills/linkedin-voice`
