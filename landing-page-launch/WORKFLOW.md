---
name: landing-page-launch
description: Plan, design, build and test a product landing page, then hand over a deploy checklist.
when_to_use: Starting a marketing or launch page for a new product or feature.
steps:
  - id: brief
    title: Agree on the message and sections
    checkpoint: true
  - id: build
    title: Design and build the page
    skill: anthropics/skills/skills/frontend-design
    output: the page source in the repository
  - id: test
    title: Test the page in a browser
    skill: anthropics/skills/skills/webapp-testing
    output: passing checks for layout, links and forms
  - id: launch
    title: Prepare the launch
    checkpoint: true
---
## brief
Ask who the page is for, the one thing a visitor must understand, the call to action, and
any brand colors or fonts. Propose a section outline (hero, problem, how it works, proof,
call to action) and agree on it before writing code.

## build
Follow the agreed outline. Write real copy from the brief instead of placeholder text, and
make the page work on a phone first.

## test
Check the page at phone and desktop widths, every link and button, the form if there is
one, and that it loads without console errors.

## launch
Write a short checklist for the user: page title and description, social preview image,
analytics, a favicon, and where it will be deployed. Do not deploy without the user's
go-ahead.
