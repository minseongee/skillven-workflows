---
name: react-quality-pass
description: Give a React or Next.js app a quality pass before release - Vercel's performance rules, interface guidelines, a web quality audit, browser tests, then a preview deploy.
when_to_use: A React or Next.js app is feature complete and needs to be fast, accessible and polished before it ships.
steps:
  - id: react
    title: Apply React and Next.js performance rules
    skill: vercel-labs/agent-skills/skills/react-best-practices
    output: fixes for waterfalls, bundle size and re-renders
  - id: ui
    title: Review the interface against the guidelines
    skill: vercel-labs/agent-skills/skills/web-design-guidelines
  - id: audit
    title: Audit performance, accessibility and SEO
    skill: addyosmani/web-quality-skills/skills/web-quality-audit
    output: an audit with the fixes applied and what is left
  - id: test
    title: Test the main flows in a browser
    skill: anthropics/skills/skills/webapp-testing
  - id: deploy
    title: Make a preview deployment
    skill: vercel-labs/agent-skills/skills/deploy-to-vercel
    checkpoint: true
---
## deploy
Ask before deploying, and make a preview deployment rather than a production one unless the
user says otherwise. Share the preview link and the list of fixes made.
