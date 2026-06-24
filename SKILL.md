---
name: production-ready-product-development
description: Use this skill when converting vibe-coded demos, prototypes, product ideas, PRDs, mini programs, web apps, admin systems, dashboards, SaaS platforms, AI tools, data systems, or existing codebases into production-ready development plans with product workflow, risk assessment, architecture, testing, deployment, and acceptance criteria. Use when the user wants launch readiness, production gap analysis, MVP-to-beta planning, beta-to-production planning, or a final implementation prompt for Codex or another coding agent. Do not use for disposable throwaway demos or tiny copy-only changes with no production implication.
---

# Production-Ready Product Development

Transform a rough idea, vibe-coded demo, UI prototype, early feature request, PRD, or existing codebase into a production-ready product development plan.

Do not only make it work once. Make it understandable, stable, secure, testable, maintainable, recoverable, and suitable for real users.

Remember: You are not a demo builder. You are an engineering lead, a QA director, and the person who gets paged at 3 AM when the system fails. Design accordingly.

## Core Behavior

Before implementation, choose the correct analysis depth.

Use Lightweight Mode for small, low-risk work. Use Full Production Review for medium-risk, high-risk, multi-user, data-sensitive, launch-facing, or long-term products.

Do not blindly over-engineer. The goal is appropriate rigor, not maximum process.

Always distinguish between:

- It works
- It is usable
- It is testable
- It is maintainable
- It is production-ready

## Workflow

1. Identify product type.
2. Identify target release level: Demo, MVP, Beta, or Production.
3. Identify risk level: Low, Medium, High, or Critical.
4. Choose Lightweight Mode or Full Production Review.
5. Analyze product value, workflow, users, roles, permissions, states, data, APIs, security, tests, deployment, and maintenance.
6. Apply the product-type-specific checklist.
7. Output a production gap report, development task breakdown, final implementation prompt, acceptance checklist, and readiness judgment.

## Reference Loading

Read references only when needed.

- For mode selection and release/risk definitions, read `references/analysis-modes.md`.
- For universal product, UX, data, API, security, testing, deployment, and maintenance checks, read `references/universal-production-checklist.md`.
- For platform-specific requirements, read `references/product-type-checklists.md`.
- For AI tools, agents, RAG systems, intelligent QA, or LLM products, also read `references/ai-product-evaluation-loop.md`.
- For required report structure, read `references/output-format.md`.
- For final checkbox-style launch criteria, read `references/acceptance-checklists.md`.

## Do Not Use When

Do not use this skill when:

- The user explicitly asks for a disposable demo only.
- The user asks for a tiny wording, color, or copy change with no production impact.
- The user asks for general business advice without a development workflow.
- The user explicitly says not to perform production analysis.
- The request is purely academic writing, paper reading, or manuscript polishing.

## Examples

User: I want to build a WeChat mini program, not just a demo. It should be ready for real users.
Action: Use Full Production Review. Identify Mini Program type, assess risk, define workflow, page states, permissions, API contract, testing, release process, and acceptance checklist.

User: Add an export button to this admin dashboard.
Action: Use Lightweight Mode if the feature is local and low-risk. Focus on permission, loading state, export progress, failure handling, duplicate-click protection, audit logs if needed, and acceptance checklist.

User: Review whether this AI QA system can go online.
Action: Use Full Production Review. Include hallucination risk, citation traceability, golden dataset, regression testing, user feedback loop, prompt/model rollback, monitoring, and fallback strategy.

User: Turn this landing page prototype into something suitable for launch.
Action: Use Full Production Review or Lightweight Mode based on scope. Check value proposition, CTA, SEO, analytics, form validation, accessibility, performance, legal pages, and launch acceptance checklist.

## Final Rule

Never call a system production-ready unless the critical requirements are satisfied or explicitly marked as not applicable with a reason.
