# Skillven workflows

Step-by-step recipes for coding agents, published through [Skillven](https://skillven.com).
Each folder holds a `WORKFLOW.md`: ordered steps that each use a security-reviewed skill or
give the agent instructions. Skillven reviews every workflow and its skills before offering
it, and the agent runs it one step at a time.

| Workflow | Steps |
|---|---|
| [pdf-tables-to-excel](pdf-tables-to-excel/WORKFLOW.md) | brief → pdf → xlsx → check |
| [landing-page-launch](landing-page-launch/WORKFLOW.md) | brief → frontend-design → webapp-testing → launch |
| [mcp-server-from-api](mcp-server-from-api/WORKFLOW.md) | scope → mcp-builder → test → docs |
| [feature-tdd-review-commit](feature-tdd-review-commit/WORKFLOW.md) | plan → tdd → code-review → commit |
| [quarterly-report-deck](quarterly-report-deck/WORKFLOW.md) | gather → xlsx → pptx → internal-comms |

To write your own, ask Claude with the Skillven plugin to "turn this into a Skillven
workflow" (the `workflow-author` skill), or follow the format in any file here.
