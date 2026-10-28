---
name: feature-tdd-review-commit
description: Ship a feature with tests first, a self code review, and a clean conventional commit.
when_to_use: Implementing a well-defined feature or bug fix in an existing codebase.
steps:
  - id: plan
    title: Agree on the behavior and test cases
    checkpoint: true
  - id: tdd
    title: Implement test-first
    skill: Asymmetric-al/core/.agents/skills/tdd
    output: passing tests that cover the agreed cases
  - id: review
    title: Review the change
    skill: Asymmetric-al/core/.agents/skills/code-review
  - id: commit
    title: Commit the change
    skill: Asymmetric-al/core/docs/ai/skills/commit
---
## plan
Restate the feature in a few sentences, list the test cases (normal, edge and failure), and
point out the files that will change. Agree on this before writing code.

## review
Read the full diff as a reviewer would: correctness first, then naming, duplication and
missing tests. Fix what you find and rerun the tests.

## commit
Commit only the files that belong to this change, with a message that says what changed and
why.
