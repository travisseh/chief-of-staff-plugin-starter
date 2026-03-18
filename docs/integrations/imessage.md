# iMessage Setup

## What You Need

- macOS
- Messages app configured
- Full Disk Access for the terminal app running Claude Code
- A local CLI or script Claude can call

## Credentials

No API key is required.

## Important Permission

Give your terminal app Full Disk Access in:

`System Settings -> Privacy & Security -> Full Disk Access`

## Suggested Local CLI Shape

```bash
node ~/.config/imessage-tools/imessage.js unreads 20
node ~/.config/imessage-tools/imessage.js messages "Person Name" 20
node ~/.config/imessage-tools/imessage.js send "+1XXXXXXXXXX" "message"
```

## Notes

- Reading usually comes from the local Messages database.
- Sending usually relies on AppleScript or another automation layer.
- Start read-only, then add sending after you've verified safety.
