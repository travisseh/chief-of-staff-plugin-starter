# Prompt: Install Or Update This Plugin Correctly

Help me install or update this repo as a Claude Code plugin without running into the common plugin gotchas.

Read:

- `README.md`
- `CLAUDE.md`
- `.claude-plugin/plugin.json`

Then:

1. Ask whether I want:
   - dev mode with `claude --plugin-dir`
   - installed mode through Claude Code's plugin installer and a local marketplace
2. If the repo is not on disk yet, clone it to `~/.claude/plugins/chief-of-staff` unless I choose a different path.
3. Validate the plugin from the repo root with `/plugin validate .` if that command is available. Otherwise confirm that `.claude-plugin/plugin.json` exists and is shaped correctly.
4. If I choose dev mode:
   - give me the exact `claude --plugin-dir ...` command to run
   - explain that this uses the source repo directly and avoids marketplace and cache issues while I personalize the plugin
5. If I choose installed mode:
   - do not edit `~/.claude/plugins/installed_plugins.json`
   - explain that install and update must go through `/plugin install` and `/plugin update`, usually via a local marketplace
   - if a local marketplace is needed, walk me through creating or updating it safely
6. If this plugin was already installed and I changed commands, skills, agents, or other tracked plugin files:
   - remind me installed plugins are cached copies
   - bump `.claude-plugin/plugin.json`
   - tell me the right update or reinstall step
   - tell me to restart Claude Code before expecting new files to load
7. If a local marketplace exists, keep its plugin version aligned with `.claude-plugin/plugin.json`.
8. At the end, tell me the best first setup prompt to run next.
