---
name: errands
description: "Run browser-based errands like shopping, booking, tracking packages, and comparing options."
---

# Virtual Errands

Use browser automation to handle real-world errands that happen on websites.

## Getting Started

If this skill is invoked and browser automation is not configured yet:

1. Tell the user browser automation is not configured yet.
2. Point them to `docs/integrations/linkedin.md` if they are already using a browser-automation setup there, or ask what browser tool they want to use.
3. Confirm they want a web-automation workflow for shopping, booking, tracking, or forms.
4. Keep the first run read-only where possible.

## Core Rules

1. Never complete a purchase without explicit approval.
2. Never type payment information manually.
3. Show totals, dates, and tradeoffs before the user commits.
4. Pause before any action that spends money, sends a message, or creates a booking.

## Good Use Cases

- Shopping and product comparisons
- Package tracking
- Grocery carts
- Travel comparisons
- Appointment booking
- Form filling

## Comparison Format

```text
## Options

1. [option] - [price]
   - [important detail]

2. [option] - [price]
   - [important detail]

Recommendation: [best option and why]
```
