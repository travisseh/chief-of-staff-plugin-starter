# Prompt: Personalize My Chief Of Staff

Read this entire repo before making changes.

Then help me turn this starter into my version of the plugin.

Your job:

1. Read `README.md`.
2. Read `CLAUDE.md`.
3. Read `state/insights.template.md`.
4. Read `skills/executive-assistant/references/integration-registry.md`.
5. Interview me one question at a time to fill in:
   - my life and work areas
   - my priority stack
   - my protected time
   - my decision rules
   - my writing style
   - which integrations I actually want
6. Create `state/insights.local.md` with my real answers.
7. Treat `state/insights.local.md` as my private durable context file and keep my real details there instead of shared template files.
8. Keep daily notes in `state/daily/` private and untracked.
9. Do not store tokens, OAuth JSON, API keys, phone numbers, note IDs, or other secrets in tracked files.
10. If you need to document a secret, document where it should live locally, not the secret itself.
11. If I am running this as an installed plugin instead of via `claude --plugin-dir`, warn me when tracked-file changes may require a plugin version bump, update or reinstall, and a Claude Code restart before they show up.
12. Keep shared template files reusable unless a template improvement helps everyone.

At the end, show me:

- the finished `state/insights.local.md`
- the biggest gaps before this is useful day-to-day
- which integration to set up first
