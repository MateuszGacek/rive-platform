# rivé documentation

This is the **entry point for product and engineering knowledge**. The Git repository is the canonical versioned record. Obsidian may be used as a visual editor over **these same Markdown files**, not as a separate source of truth.

| Document | Purpose |
| --- | --- |
| [Product vision](product/vision.md) | Product intent, outcomes and boundaries; not a feature specification |
| [Design system v0.1](design/design-system.md) | Draft brand palette, interface principles, accessibility, and change management |
| [Product capability map](product/capability-map.md) | Business areas, feature ideas, IDs, status and open dependencies |
| [Pytania i decyzje](product/open-questions.md) | Decisions to make and evidence needed across the 15 areas |
| [Słownik biznesowy](product/business-glossary.md) | Shared vocabulary for discovery, demos and acceptance tests |
| [Benchmark Hotel & SPA](research/hotel-spa-benchmark.md) | Vendor evidence, comparable demo script, compliance checks and cost model |
| [Cezar public web audit](audits/cezar/public-web/coverage.md) | Evidence-backed inventory of the existing public site, journeys, issues and gaps for rivé |
| [Plan pracy agentów](product/agent-delivery-plan.md) | Discovery sequence, deliverables and acceptance criteria for each area |
| [Warsztat recepcji](product/reception-discovery.md) | Day SPA and group settlement scenarios with open decisions |
| [Visual discovery board](maps/README.md) | Overview of 15 areas and a linked reception Canvas |
| [Discovery notes](discovery.md) | Structured interview findings, unknowns and research leads |
| [Project Brain](#project-brain) | Capture and find ideas, questions, and takeaways from agent sessions |
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

## Project Brain

W sesji agenta z dostępem do repozytorium możesz powiedzieć „Zapisz pomysł porównania sposobów pokazywania dostępności pokoi”. Agent szuka powiązanych notatek w `docs/`, aktualizuje istniejący temat lub zapisuje nowy. Istotne wnioski zapisuje domyślnie, chyba że poprosisz „nie zapisuj”. Zapis odbywa się lokalnie na `main`, a publikacja na GitHubie jest osobnym krokiem. Przy pracy na innej gałęzi, kolizji zmian lub braku dostępu do plików agent zwraca szkic. Treści poufne pozostają poza repozytorium.

- **Inbox** — szybki zapis pomysłu, pytania lub wniosku z rozmowy. Skopiuj [szablon](inbox/_template.md) do `docs/inbox/`, nadając kopii nazwę tematu.
- **Ideas** — uporządkowane pomysły w `docs/ideas/`. Rozwijając temat z Inbox, zachowaj treść, datę utworzenia i historię tej samej notatki oraz popraw odsyłacze przy przeniesieniu.
- **Research** — analizy w istniejącym `docs/research/`. Podlinkuj analizę z pomysłu, którego dotyczy. [Wcześniejsze notatki discovery](discovery.md) i pozostałe dokumenty zachowują swoje role.

Uzupełnij `type` (`idea`, `question`, `discussion` lub `research`), `status`, `area`, `source`, `created` i `updated`. Jako `area` wpisz w cudzysłowie pełną nazwę z [mapy możliwości](product/capability-map.md), np. `"03 Rezerwacje i dostępność"`, albo `"przekrojowe"`. Podaj źródło w krótkiej formie i wpisz daty jako `YYYY-MM-DD`. Zachowaj `created` przy edycji, zaktualizuj `updated` i zapisz w historii istotne ustalenie, jego datę, źródło i dostępne uzasadnienie.

Status opisuje etap pracy nad notatką. `new` oznacza nowy temat, `exploring` analizę w toku, `proposed` wariant do rozważenia, a `parked` temat odłożony. `accepted` i `rejected` wymagają jawnej decyzji właściciela zapisanej w historii. `closed` oznacza temat zakończony z zapisaną odpowiedzią lub odsyłaczem do rozstrzygnięcia. Wdrożenie zaakceptowanego pomysłu wymaga osobnej zgody. W treści stosuj etykiety **Confirmed**, **Proposed** i **Open question** oraz jawnie oznaczaj hipotezy.

Otwórz katalog repozytorium jako vault w Obsidianie, włącz wbudowaną wtyczkę **Bases** i otwórz [rejestr Project Brain](ideas/ideas.base) z eksploratora plików. Wybierz **Wszystkie**, **Inbox**, **Pomysły według obszaru**, **Analizowane** lub **Odłożone**. W widoku według obszaru rozwiń grupę **03 Rezerwacje i dostępność**.

W kolejnej sesji zapytaj „Jakie mamy otwarte pomysły dotyczące rezerwacji?”. W Markdown wyszukaj pole `area`, np. z katalogu głównego repozytorium:

```sh
rg -l '^area: "03 Rezerwacje i dostępność"$' docs/inbox docs/ideas docs/research
```

## Editing and visualization

Use relative Markdown links, descriptive headings and small files when a topic justifies a dedicated document. An Obsidian vault can point to the checked-out repository root; keep local Obsidian settings out of Git. Canvas/Excalidraw maps are helpful for exploration, but agreed rules and decisions must also be readable in Markdown.

During discovery, commit and push completed routine documentation directly to `main` at a planned publication step. Fetch first and preserve local work. Stop on conflicts or unsafe synchronization. Production code requires appropriate tests and verification before pushing.

This repository is public: use anonymized business examples only.
