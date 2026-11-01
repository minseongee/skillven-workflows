---
name: terraform-module
description: Turn Terraform code into a clean, tested module with HashiCorp's style guide, module design rules and native tests.
when_to_use: Writing a new Terraform module, or pulling a reusable module out of a large configuration.
steps:
  - id: scope
    title: Agree on the module's inputs and outputs
    checkpoint: true
  - id: refactor
    title: Shape the module
    skill: hashicorp/agent-skills/plugins/terraform/skills/refactor-module
  - id: style
    title: Apply the style guide
    skill: hashicorp/agent-skills/plugins/terraform/skills/terraform-style-guide
  - id: test
    title: Write and run tests
    skill: hashicorp/agent-skills/plugins/terraform/skills/terraform-test
    output: .tftest.hcl files that pass with terraform test
---
## scope
List the resources the module manages, its variables with types and defaults, and its
outputs. Agree on them before moving code. Never run terraform apply in this workflow;
plan and test only.
