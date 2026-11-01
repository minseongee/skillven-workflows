---
name: sales-call-cycle
description: Run one sales conversation well - research the account, prepare the call, summarize it and draft the follow-up.
when_to_use: A discovery or follow-up call with a prospect or customer is coming up.
steps:
  - id: research
    title: Research the account
    skill: anthropics/knowledge-work-plugins/sales/skills/account-research
  - id: prep
    title: Prepare the call
    skill: anthropics/knowledge-work-plugins/sales/skills/call-prep
    output: a one-page brief with discovery questions
  - id: summary
    title: Summarize the call
    skill: anthropics/knowledge-work-plugins/sales/skills/call-summary
    checkpoint: true
  - id: followup
    title: Draft the follow-up
    skill: anthropics/knowledge-work-plugins/sales/skills/draft-outreach
---
## summary
Wait for the user to share the call notes or transcript, then summarize them. Leave emails
as drafts: nothing is sent without the user.
