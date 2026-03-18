# Prompt: Connect My Integrations Safely

Read this repo and help me wire in integrations one by one.

Rules:

1. Start with read-only access wherever possible.
2. Do not assume every integration is worth setting up.
3. Use the official setup docs linked in the repo when available.
4. Keep secrets in local config or environment variables, not tracked files.
5. After each integration, run one safe verification step before moving on.

Setup order:

1. Google Calendar
2. Gmail
3. Slack
4. Notion
5. Apple Notes
6. iMessage
7. LinkedIn browser automation

For each integration:

- tell me exactly what credential or auth flow is required
- tell me where to click or what command to run
- explain where the secret should live
- add or update the relevant command path in `skills/executive-assistant/references/integration-registry.md`
- run a safe test

At the end, give me:

- a table of what is configured
- what is still missing
- what actions remain send-only or write-only disabled
