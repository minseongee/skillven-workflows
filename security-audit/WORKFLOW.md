---
name: security-audit
description: Audit a codebase for security bugs the way Trail of Bits does - build context first, run static analysis, look for footguns, hunt variants, then confirm each finding before reporting it.
when_to_use: A security review of a repository or service before a release, an acquisition or an external audit.
steps:
  - id: scope
    title: Agree on the scope and threat model
    checkpoint: true
  - id: context
    title: Build context on the code
    skill: trailofbits/skills/plugins/audit-context-building/skills/audit-context-building
    output: notes on each component's assumptions, guarantees and trust boundaries
  - id: static
    title: Run static analysis
    skill: trailofbits/skills/plugins/static-analysis/skills/semgrep
    output: Semgrep results triaged into likely and unlikely issues
  - id: sharp-edges
    title: Look for dangerous APIs and configurations
    skill: trailofbits/skills/plugins/sharp-edges/skills/sharp-edges
  - id: variants
    title: Hunt variants of each real bug
    skill: trailofbits/skills/plugins/variant-analysis/skills/variant-analysis
  - id: confirm
    title: Rule out false positives
    skill: trailofbits/skills/plugins/fp-check/skills/fp-check
    output: a true or false positive verdict with evidence for every finding
  - id: report
    title: Write the report
    checkpoint: true
---
## scope
Ask which components are in scope, who the attackers are (anonymous users, logged-in users,
insiders), what assets matter most, and any known past issues. Write this down as a short
threat model and agree on it.

## report
List confirmed findings by severity, each with where it is, how to trigger it, its impact
and a suggested fix. Keep unconfirmed leads in a separate section. Do not open issues or
pull requests unless the user asks.
