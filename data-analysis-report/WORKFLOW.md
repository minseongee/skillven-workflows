---
name: data-analysis-report
description: Analyze a dataset end to end - profile it, run the statistics, chart the findings, check the analysis and share it as a dashboard.
when_to_use: Someone hands over a dataset or a query result and wants findings they can trust and share.
steps:
  - id: questions
    title: Agree on the questions
    checkpoint: true
  - id: explore
    title: Profile the data
    skill: anthropics/knowledge-work-plugins/data/skills/explore-data
  - id: analyze
    title: Run the analysis
    skill: anthropics/knowledge-work-plugins/data/skills/statistical-analysis
  - id: charts
    title: Chart the findings
    skill: anthropics/knowledge-work-plugins/data/skills/create-viz
  - id: validate
    title: Check the analysis
    skill: anthropics/knowledge-work-plugins/data/skills/validate-data
  - id: dashboard
    title: Build the dashboard
    skill: anthropics/knowledge-work-plugins/data/skills/build-dashboard
    output: a self-contained HTML dashboard
---
## questions
Ask what decision the analysis should support, which questions it must answer and who will
read it. Agree on these before touching the data.
