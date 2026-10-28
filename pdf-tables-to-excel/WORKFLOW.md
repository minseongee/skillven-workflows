---
name: pdf-tables-to-excel
description: Turn the tables in PDF reports into a clean Excel workbook, one sheet per table plus a summary sheet, with totals checked against the source.
when_to_use: Someone hands over PDF reports or statements and wants the numbers in a spreadsheet they can work with.
steps:
  - id: brief
    title: Agree on which tables matter
    checkpoint: true
  - id: extract
    title: Extract the tables from the PDFs
    skill: anthropics/skills/skills/pdf
    output: one CSV per table, with the page it came from
  - id: workbook
    title: Build the Excel workbook
    skill: anthropics/skills/skills/xlsx
    output: a workbook with a summary sheet and one sheet per table
  - id: check
    title: Check the numbers against the PDFs
---
## brief
Ask which tables matter, which pages they are on, what units and currency they use, and how
the workbook will be used (reading, charting, further analysis). Confirm the list before
extracting anything.

## extract
Extract only the agreed tables. Keep headers, keep negative numbers and footnote markers
distinct, and note the source page for every table.

## workbook
Put a summary sheet first, then one sheet per table named after it. Store numbers as
numbers, not text, use one number format per column, and freeze the header row.

## check
Recompute every total and subtotal in the workbook and compare it with the figure printed in
the PDF. List any mismatch with its sheet, row and the PDF page, and fix extraction errors
before handing the workbook over.
