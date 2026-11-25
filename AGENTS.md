# Agent instructions — rivé Platform

At the start of a session, read the [project status](docs/PROJECT-STATUS.md), the [project roadmap](docs/PROJECT-ROADMAP.md), [docs/README.md](docs/README.md), and the relevant approved decisions and domain sources. For product discovery, use the [capability map](docs/product/capability-map.md) as the canonical inventory and [Obsidian Canvas](docs/maps/rive-product-map.canvas) as its editable visual overview. Update both when confirmed business dependencies or feature categories change. Treat this repository as a real production-bound product. The human owner is responsible for business requirements, scope, architecture approvals, and final review. AI agents assist with research, documentation, implementation, and verification.

## Authority and context

1. **Approved product facts, requirements and decisions** in this repository are authoritative for their scope.
2. **Discovery notes, research and proposals** are evidence or hypotheses, not approval.
3. A chat summary or generated draft must not silently override an approved document.
4. If sources conflict, note the conflict and ask for a decision. Never invent missing business rules.

Use the labels **Confirmed**, **Proposed**, and **Open question** in discovery documents. Identify the source/date of significant research findings. Clearly mark assumptions.

## Phase control and discovery workflow

- Use the project status for the active phase and next step. The roadmap defines dependencies and exit criteria for the whole platform. Update the point of resumption after each substantial session.
- Obtain explicit owner approval before changing phase, opening work from a later phase, starting a technical experiment or POC, or starting implementation. Record the approved scope, date and supporting links in the project status. Approval of a module's business rules applies to those rules.
- Work directly on `main` for routine discovery documentation. Commit and push completed changes at a planned publication step without a feature branch or PR. Fetch first, preserve uncommitted work, and stop on conflicts or unsafe synchronization. Never force-push.
- GitHub Markdown is the canonical knowledge source; Obsidian and Canvas provide a visual interface to the same files. Keep both aligned when capabilities or dependencies change.
- Keep documentation concise and maintainable. Distinguish proposals and open questions from approved requirements; never invent requirements or architecture decisions.
- Do not introduce an application framework, database, CMS, monorepo tool, OpenSpec, or production infrastructure unless the owner explicitly approves the choice.
- Do not generate speculative database schemas, APIs, features or large planning documents.
- Work on one business area or question at a time, while keeping cross-domain dependencies visible.
- Preserve important existing facts when updating notes; replace outdated proposals only with an explicit explanation.
- Maintain readable, relative Markdown links that work on GitHub as well as in Obsidian.
- GitHub Issues/Projects will own delivery status when introduced; do not maintain a competing task-status system in Markdown.

## Project Brain

- In sessions with repository access, capture significant ideas, questions, and takeaways by default unless the owner asks to skip capture. Read the [Project Brain guide](docs/README.md#project-brain) and search `docs/` for the topic first. Update the existing note when it covers the same topic, or create a new note and link related material. Report the note path.
- Save eligible notes locally on `main` when the edit does not conflict with ongoing work. On another branch, when edits conflict, or when the session has no repository access, return a draft for later. Do not switch branches, stash changes, or overwrite someone else's work to capture a note. Keep confidential drafts outside this public repository.
- Capture ends with a local edit. Publish only at a separate planned step, using the discovery workflow and including only the notes in scope for publication.
- Record sources, dates, and the reasons for decisions. Set `accepted` or `rejected` only after an explicit owner decision. An agent may capture or revise a note, but needs owner approval to approve requirements, change the roadmap, decide architecture, or create implementation tasks.

## When development begins

Use the [roadmap](docs/PROJECT-ROADMAP.md) for the phase and the [agent delivery plan](docs/product/agent-delivery-plan.md) to scope work and define acceptance. Track unanswered business rules in the [decision questions](docs/product/open-questions.md). A vendor claim or attached proposal is evidence to evaluate. The owner approves the delivery scope and architecture and separately opens implementation.

Before an implementation task: read relevant product rules and decisions, define expected behavior, exceptions, dependencies, tests and acceptance criteria. Agree the appropriate review workflow for production code and verify it with relevant tests before pushing. Keep changes within the approved scope. Do not remove or rewrite existing behavior, data contracts or permissions as an incidental refactor.

Prefer supported stable runtimes, **LTS where the project offers an LTS line**. Do not automatically choose the newest library versions. Once approved, pin dependencies appropriately, commit the package-manager lockfile and require review for major version changes. Do not add tools or services merely for convenience.

For high-risk behavior (availability, booking, payments, personal data, access control), require relevant tests, migration review and explicit sign-off. Agent instructions are not a substitute for automated checks, code review, backups or operational controls.

## Public repository safeguards

Never place credentials, .env files, personal data, real customer/employee data, confidential pricing or accounting details in code, documents, issues, PRs, examples, screenshots or commit history. Use synthetic examples. If a requested change might expose sensitive information, stop and flag it.

Do not force-push, rewrite shared history, deploy to production, merge PRs or perform destructive operations without explicit approval.
