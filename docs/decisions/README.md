# Decision records

Use a short Architecture/Product Decision Record (ADR) for **meaningful, approved trade-offs**: boundaries between domains, integration-vs-build choices, reliability guarantees, major libraries, infrastructure, and consequential product behavior.

Do **not** write an ADR for every idea, temporary experiment, formatting change or routine implementation detail.

Suggested filenames: `0001-short-decision-title.md`, `0002-next-decision.md`. Assign numbers when an actual decision is proposed.

## Small decision template

```markdown
# ADR-0001: [Title]

- Status: Proposed | Accepted | Superseded
- Date: YYYY-MM-DD
- Owner: [Decision maker]

## Context
What problem or constraint requires this decision?

## Options and trade-offs
What realistic alternatives were considered, and why?

## Decision
What exactly is approved? (Leave blank until accepted.)

## Consequences and risks
What improves, what becomes harder, and what must be tested?

## Follow-up
Links to relevant requirements, issues or other decisions.
```

Changes to accepted decisions require a new linked record or a clearly reviewed update; don't silently rewrite history. Keep sensitive details out of this public repository.
