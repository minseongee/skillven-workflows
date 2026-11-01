---
name: systematic-bug-fix
description: Fix a bug by finding its root cause first, locking it in with a failing regression test, then fixing, verifying and committing.
when_to_use: A bug report, a failing test or unexpected behavior whose cause is not yet known.
steps:
  - id: reproduce
    title: Reproduce the bug
    checkpoint: true
  - id: debug
    title: Find the root cause
    skill: obra/superpowers/skills/systematic-debugging
    output: the root cause, with the evidence for it
  - id: fix
    title: Write a failing test, then fix
    skill: obra/superpowers/skills/test-driven-development
    output: a regression test that failed before the fix and passes after
  - id: verify
    title: Verify the fix
    skill: obra/superpowers/skills/verification-before-completion
  - id: commit
    title: Commit the fix
    skill: getsentry/skills/skills/commit
---
## reproduce
Collect the exact steps, inputs, error messages and versions. Reproduce the bug yourself
and write down the shortest way to trigger it. If it cannot be reproduced, say so and ask
the user for more detail before going further.

## debug
Do not change code to see what happens. Trace the bad value or state back to where it
first goes wrong, form one hypothesis at a time and test it.

## commit
Explain in the commit message what was wrong, why, and how the test guards against it.
