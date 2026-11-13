# rivé documentation

This is the **entry point for product and engineering knowledge**. The Git repository is the canonical versioned record. Obsidian may be used as a visual editor over **these same Markdown files**, not as a separate source of truth.

| Document | Purpose |
| --- | --- |
| [Product vision](product/vision.md) | Product intent, outcomes and boundaries; not a feature specification |
| [Design system v0.1](design/design-system.md) | Draft brand palette, interface principles, accessibility, and change management |
| [Product capability map](product/capability-map.md) | Business areas, feature ideas, IDs, status and open dependencies |
| [Visual discovery board](maps/README.md) | Obsidian Canvas with grouped capabilities and relations |
| [Discovery notes](discovery.md) | Structured interview findings, unknowns and research leads |
| [Decisions](decisions/README.md) | ADR-style record of approved technical and product trade-offs |
| [Agent instructions](../AGENTS.md) | AI collaboration, quality and safety rules |

## How knowledge progresses

1. **Explore:** discuss real workflows and collect facts, questions, hypotheses and external evidence in discovery notes.
2. **Clarify:** identify actors, process variants, exceptions, existing systems, data ownership and dependencies. Use visual maps where helpful.
3. **Evaluate:** compare build-vs-buy choices and document risks, costs and alternatives.
4. **Decide:** promote confirmed outcomes into product/domain documents; record important trade-offs as decisions.
5. **Deliver (later):** pick a small end-to-end user outcome, approve its requirements, then create an Issue and a reviewed implementation specification. Specification tooling remains undecided.
6. **Verify:** require relevant automated tests, review and acceptance checks before pushing changes that affect the product.

Map the complete business at a coarse level; only detail the current process or next deliverable. Do not create hundreds of feature files or duplicate status tracking.

## Labels used in documents

- **Confirmed:** explicitly stated by the owner or independently verified; where useful, identify the source.
- **Proposed:** an option to evaluate; not a commitment.
- **Open question:** information or a decision still needed.

Separate what Rivé does **today** from what the **future platform should do**. Do not upgrade guesses into facts.

## Editing and visualization

Use relative Markdown links, descriptive headings and small files when a topic justifies a dedicated document. An Obsidian vault can point to the checked-out repository root; keep local Obsidian settings out of Git. Canvas/Excalidraw maps are helpful for exploration, but agreed rules and decisions must also be readable in Markdown.

During discovery, commit and push completed routine documentation directly to `main`. Fetch first and preserve local work; resolve conflicts safely before continuing. Production code requires appropriate tests and verification before pushing.

This repository is public: use anonymized business examples only.
