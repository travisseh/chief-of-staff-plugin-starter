# Chief of Staff Plugin Starter

This repository is a starter template for a personal chief-of-staff workflow inside Claude Code.

## Your Job In This Repo

When a user opens this repo and asks for setup help:

1. Read [README.md](./README.md).
2. Read [state/insights.local.md](./state/insights.local.md) if it exists.
3. Otherwise read [state/insights.template.md](./state/insights.template.md).
4. Read [skills/executive-assistant/references/integration-registry.md](./skills/executive-assistant/references/integration-registry.md).
5. If the user is just getting started, use the prompt files in [docs/prompts](./docs/prompts).

## Behavioral Rules

- Treat this as a modular system. Do not assume every integration is configured.
- If a tool or credential is missing, say so plainly and continue with the sources that do exist.
- Keep secrets out of tracked files. Prefer local config files, environment variables, or user-scoped Claude settings.
- Before sending messages, posting publicly, purchasing something, or creating calendar events, get explicit approval.
- When personalizing the system, prefer editing `state/insights.local.md` over hard-coding private facts into command or skill files.
- Preserve the plugin as a reusable starter. Only replace placeholders in shared files when the change improves the template for everyone.

## Plugin Loading Rules

- If the user wants to run this as a Claude Code plugin, first distinguish between dev mode and installed mode.
- Recommend `claude --plugin-dir /absolute/path/to/repo` for fast iteration and first-time setup.
- Treat cloning into `~/.claude/plugins/...` as a location choice, not a full install.
- Never tell the user to edit `~/.claude/plugins/installed_plugins.json` manually.
- Run `/plugin validate .` before telling the user the plugin is ready, if that command is available.
- If the repo is being used via an installed plugin flow and tracked plugin files change, remind the user that installed plugins are cached copies. They may need to bump `.claude-plugin/plugin.json`, update or reinstall the plugin, and restart Claude Code before new commands, skills, or agents show up.
- If the user creates a local marketplace entry for this plugin, keep its version aligned with `.claude-plugin/plugin.json`.

## What “Good” Looks Like

- The user can paste one setup prompt and Claude can guide them through the next step.
- The user can run a daily brief even with only partial integrations configured.
- The plugin helps prioritize, not just summarize.
- The system reflects the user's real priorities and constraints instead of generic productivity advice.
- Prefer local repo skills over missing global skills when both could apply.
