---
name: stripe
description: "Query Stripe for revenue, payments, subscriptions, customers, and checkout activity in the chief-of-staff workflow."
---

# Stripe

Use this skill when the user wants revenue, customer, payment, or signup data from Stripe.

## Good Use Cases

- Revenue snapshots
- Recent payments
- Failed payments
- Subscription status
- Checkout session analysis
- Customer lookups
- Affiliate or referral revenue reviews

## Keep This Generic

Do not store:

- real Stripe secret keys
- project-specific product IDs
- internal file paths
- customer emails
- private business metrics

Put those in local environment files or `state/insights.local.md`.

## Common Setup Pattern

Most projects use one of these approaches:

1. A local app repo with `STRIPE_SECRET_KEY` in an env file
2. A local CLI wrapper
3. A direct MCP or API integration

## Getting Started

If this skill is invoked and Stripe access does not exist yet:

1. Tell the user Stripe is not configured yet.
2. Ask which codebase or environment owns Stripe access.
3. Look for:
   - `STRIPE_SECRET_KEY`
   - an existing Stripe client
   - scripts or routes already querying Stripe
4. Keep all real keys and project-specific identifiers in local env files or local memory, not tracked files.
5. Start with a safe read-only query like recent checkout sessions or payment totals.

## Typical Queries

- List recent completed checkout sessions
- Count customers by product or plan
- Summarize MRR or recent one-time revenue
- Find customers by email
- Review affiliate/referral metadata

## Workflow

1. Find the Stripe access path for the current project.
2. Confirm which account or environment you are querying.
3. Pull the smallest useful set of records first.
4. Summarize clearly.
5. Avoid exposing sensitive customer or payment details unless the user asks.
