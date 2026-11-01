# Skillven workflows

Step-by-step recipes for coding agents, published through [Skillven](https://skillven.com).
Each folder holds a `WORKFLOW.md`: ordered steps that each use a security-reviewed skill or
give the agent instructions. Many build on well-known collections such as
obra/superpowers, Trail of Bits, Sentry, Vercel, Hugging Face and Anthropic's own skills.
Skillven reviews every workflow and its skills before offering
it, and the agent runs it one step at a time.

| Workflow | Steps |
|---|---|
| [branch-to-merged-pr](branch-to-merged-pr/WORKFLOW.md) | branch → implement → bugs → simplify → commit → pr → iterate |
| [contract-review](contract-review/WORKFLOW.md) | triage → review → risk → respond |
| [data-analysis-report](data-analysis-report/WORKFLOW.md) | questions → explore → analyze → charts → validate → dashboard |
| [expo-app-to-store](expo-app-to-store/WORKFLOW.md) | plan → ui → data → test → release |
| [feature-tdd-review-commit](feature-tdd-review-commit/WORKFLOW.md) | plan → tdd → review → commit |
| [fine-tune-and-demo-model](fine-tune-and-demo-model/WORKFLOW.md) | goal → data → train → eval → demo |
| [landing-page-launch](landing-page-launch/WORKFLOW.md) | brief → build → test → launch |
| [marketing-site-audit](marketing-site-audit/WORKFLOW.md) | context → seo → ai-seo → cro → copy → plan |
| [mcp-server-from-api](mcp-server-from-api/WORKFLOW.md) | scope → build → test → docs |
| [pdf-tables-to-excel](pdf-tables-to-excel/WORKFLOW.md) | brief → extract → workbook → check |
| [postgres-schema-change](postgres-schema-change/WORKFLOW.md) | design → branch → rollout |
| [product-demo-video](product-demo-video/WORKFLOW.md) | script → create → scenes → captions → render |
| [product-launch-plan](product-launch-plan/WORKFLOW.md) | research → position → launch → emails → social → review |
| [quarterly-report-deck](quarterly-report-deck/WORKFLOW.md) | gather → analyze → deck → summary |
| [react-quality-pass](react-quality-pass/WORKFLOW.md) | react → ui → audit → test → deploy |
| [research-to-sprint](research-to-sprint/WORKFLOW.md) | synthesize → spec → sprint → update |
| [sales-call-cycle](sales-call-cycle/WORKFLOW.md) | research → prep → summary → followup |
| [security-audit](security-audit/WORKFLOW.md) | scope → context → static → sharp-edges → variants → confirm → report |
| [spec-to-tickets-tdd](spec-to-tickets-tdd/WORKFLOW.md) | grill → spec → tickets → build → review |
| [stripe-payments](stripe-payments/WORKFLOW.md) | plan → design → build → test |
| [superpowers-feature](superpowers-feature/WORKFLOW.md) | brainstorm → worktree → plan → build → review → verify → finish |
| [systematic-bug-fix](systematic-bug-fix/WORKFLOW.md) | reproduce → debug → fix → verify → commit |
| [terraform-module](terraform-module/WORKFLOW.md) | scope → refactor → style → test |

To write your own, ask Claude with the Skillven plugin to "turn this into a Skillven
workflow" (the `workflow-author` skill), or follow the format in any file here.
