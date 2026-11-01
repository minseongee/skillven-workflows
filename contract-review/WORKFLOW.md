---
name: contract-review
description: Review an incoming contract or NDA - triage it, review clause by clause against your playbook, assess the risks and draft the response.
when_to_use: A vendor, customer or partner agreement arrives and needs a first legal review before counsel signs off.
steps:
  - id: triage
    title: Triage the agreement
    skill: anthropics/knowledge-work-plugins/legal/skills/triage-nda
  - id: review
    title: Review it clause by clause
    skill: anthropics/knowledge-work-plugins/legal/skills/review-contract
    output: deviations from the playbook with suggested redlines
  - id: risk
    title: Assess the risks
    skill: anthropics/knowledge-work-plugins/legal/skills/legal-risk-assessment
  - id: respond
    title: Draft the response
    checkpoint: true
---
## respond
Draft a reply to the other side with the requested changes and the reasons for each, and a
short internal note on what needs counsel's decision. This is not legal advice: make clear
that a lawyer should approve before anything is sent or signed.
