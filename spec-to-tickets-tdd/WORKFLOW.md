---
name: spec-to-tickets-tdd
description: Matt Pocock's way from idea to code - get grilled on the plan, turn it into a spec and tracer-bullet tickets, build them test-first and review against the spec.
when_to_use: A feature idea that is still fuzzy and needs a sharp plan before anyone writes code.
steps:
  - id: grill
    title: Get grilled on the plan
    skill: mattpocock/skills/skills/productivity/grill-me
    checkpoint: true
  - id: spec
    title: Write the spec
    skill: mattpocock/skills/skills/engineering/to-spec
    output: a spec in the issue tracker or the repository
  - id: tickets
    title: Break the spec into tickets
    skill: mattpocock/skills/skills/engineering/to-tickets
    checkpoint: true
    output: tracer-bullet tickets with their blocking edges
  - id: build
    title: Build each ticket test-first
    skill: mattpocock/skills/skills/engineering/tdd
  - id: review
    title: Review against the spec
    skill: mattpocock/skills/skills/engineering/code-review
---
## grill
Answer the questions one at a time until the plan has no open decisions. Write down the
decisions as you go, so the spec step has them.

## tickets
Show the tickets and their order to the user before publishing them to a tracker.
