---
name: superpowers-feature
description: Build a feature the Superpowers way - brainstorm the design, plan it in small tasks, build it task by task with tests first, review, verify and finish the branch.
when_to_use: Building a feature or a change that takes more than a few edits, where getting the design right first matters.
steps:
  - id: brainstorm
    title: Brainstorm the design with the user
    skill: obra/superpowers/skills/brainstorming
    checkpoint: true
    output: an agreed design written down in the repository
  - id: worktree
    title: Set up an isolated worktree
    skill: obra/superpowers/skills/using-git-worktrees
  - id: plan
    title: Write the implementation plan
    skill: obra/superpowers/skills/writing-plans
    checkpoint: true
    output: a plan of small tasks, each with its tests and files
  - id: build
    title: Build the plan task by task
    skill: obra/superpowers/skills/subagent-driven-development
    output: every task done with passing tests
  - id: review
    title: Request a code review
    skill: obra/superpowers/skills/requesting-code-review
  - id: verify
    title: Verify before calling it done
    skill: obra/superpowers/skills/verification-before-completion
  - id: finish
    title: Finish the branch
    skill: obra/superpowers/skills/finishing-a-development-branch
    checkpoint: true
---
## brainstorm
Ask one question at a time until the goal, the constraints and what is out of scope are
clear. Offer two or three approaches with their trade-offs, then write down the one the user
picks. Do not write code in this step.

## build
Work through the plan in order. Each task starts with a failing test and ends with the test
passing and the change committed. If a task turns out wrong, stop and update the plan with
the user instead of improvising.

## verify
Run the full test suite and any linters or builds the project uses, and read their output.
Report what passed and what did not; never say done on the strength of a partial run.
