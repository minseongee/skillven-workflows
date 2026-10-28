---
name: quarterly-report-deck
description: Turn a quarter's spreadsheet data into an analysis workbook, a presentation deck, and a short summary note for the team.
when_to_use: Preparing a quarterly or monthly business review from exported data.
steps:
  - id: gather
    title: Agree on the questions and the data
    checkpoint: true
  - id: analyze
    title: Analyze the data
    skill: anthropics/skills/skills/xlsx
    output: a workbook with the key metrics and charts
  - id: deck
    title: Build the presentation
    skill: anthropics/skills/skills/pptx
    output: a deck of about ten slides
  - id: summary
    title: Write the summary note
    skill: anthropics/skills/skills/internal-comms
---
## gather
Ask which questions the review must answer, which files hold the data, the comparison
period, and who the audience is. Agree on three to five headline metrics.

## analyze
Compute the agreed metrics with formulas rather than pasted values, compare them with the
previous period, and chart each headline metric.

## deck
One idea per slide: the headline numbers first, then one slide per question, then risks and
next steps. Use the charts from the workbook and keep text short.

## summary
Write a short note for the team with the three most important findings and the decisions
needed, linking to the deck and workbook.
