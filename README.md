# Production-Ready Product Development Skill

An agent skill for turning demos, prototypes, PRDs, early feature ideas, and existing codebases into production-ready product development plans.

It helps Codex and other coding agents avoid stopping at demo quality by checking product workflow, release level, risk level, roles, permissions, page states, data models, API contracts, security, testing, deployment, operations, and acceptance criteria.

## What This Skill Does

- Identifies the product type before applying a checklist.
- Classifies the target release level as Demo, MVP, Beta, or Production.
- Classifies risk as Low, Medium, High, or Critical.
- Chooses Lightweight Mode for small low-risk changes.
- Uses Full Production Review for real-user, high-risk, or launch-facing work.
- Produces a final implementation prompt for Codex or another coding agent.
- Generates practical acceptance checklists for product, QA, and delivery review.

## Repository Structure

```text
production-ready-product-development/
|-- SKILL.md
|-- agents/
|   `-- openai.yaml
`-- references/
    |-- acceptance-checklists.md
    |-- ai-product-evaluation-loop.md
    |-- analysis-modes.md
    |-- output-format.md
    |-- product-type-checklists.md
    `-- universal-production-checklist.md
```

## When To Use

Use this skill when you want to:

- Turn a vibe-coded demo into a real product plan.
- Review whether an MVP is ready for beta or production.
- Check what is missing before launch.
- Convert a PRD or prototype into implementation tasks.
- Assess an admin system, SaaS app, dashboard, mini program, AI tool, or data system.
- Generate a production-grade implementation prompt for another coding agent.

## Example Prompts

```text
Use $production-ready-product-development to review whether this mini program is ready for real users.
```

```text
Use $production-ready-product-development to turn this admin dashboard prototype into a beta-ready development plan.
```

```text
Use $production-ready-product-development to assess whether this AI QA system can go online safely.
```

## Notes

This skill is intentionally split into a short `SKILL.md` and focused reference files. The main skill handles routing and workflow, while detailed checklists are loaded only when needed.
