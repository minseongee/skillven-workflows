---
name: stripe-payments
description: Add Stripe payments to an app the way Stripe recommends - pick the right integration, build it, handle webhooks and test it in test mode.
when_to_use: An app needs checkout, subscriptions or invoices with Stripe.
steps:
  - id: plan
    title: Agree on what to charge for and how
    checkpoint: true
  - id: design
    title: Choose the integration
    skill: stripe/ai/skills/stripe-best-practices
    output: the Stripe APIs and objects to use, and why
  - id: build
    title: Build the integration
    skill: stripe/ai/skills/stripe-docs
  - id: test
    title: Test it in test mode
---
## plan
Ask what is sold (one-off, subscription, usage), in which currencies and countries, and
whether Stripe Checkout or an embedded form is wanted.

## build
Create objects on the server, verify webhook signatures, and make webhook handlers safe to
run twice. Keep keys in environment variables, never in code.

## test
Use test mode keys and Stripe's test cards only: a successful payment, a declined card, a
card that needs authentication, and a cancelled subscription if there is one.
