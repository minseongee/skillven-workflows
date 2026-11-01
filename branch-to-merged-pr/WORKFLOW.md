---
name: branch-to-merged-pr
description: Take a change from a fresh branch to a green, review-ready pull request, the way Sentry's engineers do - find bugs, simplify, commit, write the PR and iterate until CI passes.
when_to_use: A change is ready to become a pull request and should arrive clean, described and passing CI.
steps:
  - id: branch
    title: Create the branch
    skill: getsentry/skills/skills/create-branch
  - id: implement
    title: Make the change
  - id: bugs
    title: Find bugs in the change
    skill: getsentry/skills/skills/find-bugs
  - id: simplify
    title: Simplify the code
    skill: getsentry/skills/skills/code-simplifier
  - id: commit
    title: Commit
    skill: getsentry/skills/skills/commit
  - id: pr
    title: Open the pull request
    skill: getsentry/skills/skills/pr-writer
    checkpoint: true
  - id: iterate
    title: Iterate until CI and review pass
    skill: getsentry/skills/skills/iterate-pr
---
## implement
Make the change the user asked for, with tests, following the conventions already in the
repository. Run the tests before moving on.

## pr
Show the user the title and description before opening the pull request, and only push or
open it once they agree.
