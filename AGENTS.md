# Agent instructions — rivé Platform

Read [docs/README.md](docs/README.md) before making changes. For product discovery, use [capability map](docs/product/capability-map.md) as the canonical inventory of candidate capabilities and [Obsidian Canvas](docs/maps/rive-product-map.canvas) as its editable visual overview; update both when confirmed business dependencies or feature categories change. Treat this repository as a real production-bound product, not a demo. The human owner is responsible for business requirements, scope, architecture approvals, and final review. AI agents assist with research, documentation, implementation, and verification.

## Authority and context

1. **Approved product facts, requirements and decisions** in this repository are authoritative for their scope.
2. **Discovery notes, research and proposals** are evidence or hypotheses, not approval.
3. A chat summary or generated draft must not silently override an approved document.
4. If sources conflict, note the conflict and ask for a decision. Never invent missing business rules.

Use the labels **Confirmed**, **Proposed**, and **Open question** in discovery documents. Identify the source/date of significant research findings. Clearly mark assumptions.

## Current phase: discovery

- Work directly on `main` for routine discovery documentation; commit and push completed changes without a feature branch or PR. Fetch first, preserve uncommitted work, and stop on conflicts or unsafe synchronization. Never force-push.
- GitHub Markdown is the canonical knowledge source; Obsidian and Canvas provide a visual interface to the same files. Keep both aligned when capabilities or dependencies change.
- Keep documentation concise and maintainable. Distinguish proposals and open questions from approved requirements; never invent requirements or architecture decisions.
- Do not introduce an application framework, database, CMS, monorepo tool, OpenSpec, or production infrastructure unless the owner explicitly approves the choice.
- Do not generate speculative database schemas, APIs, features or large planning documents.
- Work on one business area or question at a time, while keeping cross-domain dependencies visible.
- Preserve important existing facts when updating notes; replace outdated proposals only with an explicit explanation.
- Maintain readable, relative Markdown links that work on GitHub as well as in Obsidian.
- GitHub Issues/Projects will own delivery status when introduced; do not maintain a competing task-status system in Markdown.

## When development begins

Before an implementation task: read relevant product rules and decisions, define expected behavior, exceptions, dependencies, tests and acceptance criteria. Agree the appropriate review workflow for production code and verify it with relevant tests before pushing. Keep changes within the approved scope. Do not remove or rewrite existing behavior, data contracts or permissions as an incidental refactor.

Prefer supported stable runtimes, **LTS where the project offers an LTS line**. Do not automatically choose the newest library versions. Once approved, pin dependencies appropriately, commit the package-manager lockfile and require review for major version changes. Do not add tools or services merely for convenience.

For high-risk behavior (availability, booking, payments, personal data, access control), require relevant tests, migration review and explicit sign-off. Agent instructions are not a substitute for automated checks, code review, backups or operational controls.

## Public repository safeguards

Never place credentials, .env files, personal data, real customer/employee data, confidential pricing or accounting details in code, documents, issues, PRs, examples, screenshots or commit history. Use synthetic examples. If a requested change might expose sensitive information, stop and flag it.

Do not force-push, rewrite shared history, deploy to production, merge PRs or perform destructive operations without explicit approval.
