---
name: postgres-schema-change
description: Make a Postgres schema change safely - design it with Supabase's best practices, try the migration on a Neon branch, then plan the rollout.
when_to_use: Adding tables, columns or indexes to a Postgres database that already holds real data.
steps:
  - id: design
    title: Design the change
    skill: supabase/agent-skills/skills/supabase-postgres-best-practices
    checkpoint: true
    output: the migration SQL and the reasons for each choice
  - id: branch
    title: Try it on a database branch
    skill: neondatabase/agent-skills/skills/neon-postgres-branches
  - id: rollout
    title: Plan the rollout
    checkpoint: true
---
## rollout
Write the order of steps for production: backups, the migration, any backfill in batches,
the deploy of code that uses the change, and how to roll back. Run nothing against
production without the user's go-ahead.
