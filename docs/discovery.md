# Rivé — Product Discovery

> Last updated: 2026-10-23. These are early, non-confidential working notes, **not an approved product specification**.

## 1. Context and vision — to validate

- Rivé is being explored as a hospitality and wellness platform connected to the existing Cezar business in Bielsko-Biała.
- The long-term ambition is to support public-facing experiences and internal day-to-day operations in one coherent product.
- We will start by understanding real business processes, not by selecting frameworks or designing database tables.

## 2. Candidate product areas — ideas, not commitments

- **Website and CMS:** public pages, service offerings, marketing content, and SEO.
- **Booking and availability:** accommodation, wellness services, resources, schedules, packages, and events.
- **Guest CRM and operations:** guest profiles, visit history, reception workflows, and guest accounts.
- **Employees:** shift scheduling, time tracking, service assignments, and inputs for compensation calculations.
- **Payments and finance:** deposits, balances, refunds, reporting, and exports.
- **Integrations:** payment providers, distribution channels such as Booking.com/Airbnb, calendar/notifications, and accounting services.

This list describes possible areas to investigate; it is **not** the scope of an MVP.

## 3. Process and knowledge-management decisions

- Use `MateuszGacek/rive-platform` as the version-controlled project workspace.
- Keep exploratory conversations separate from durable, reviewed project notes.
- Capture facts, proposals, confirmed decisions, and open questions distinctly.
- Avoid choosing a technology stack or introducing OpenSpec until discovery provides enough clarity.
- Keep public documentation free of personal data, secrets, and confidential commercial information.

## 4. Technical decisions

None yet. A modular architecture and various frontend, backend, and CMS options have been discussed, but **nothing is approved**.

## 5. Open questions for discovery

1. How are reservations, availability, payments, and staff schedules managed today?
2. Which existing tools must stay in place or integrate with the future platform?
3. Which operational pain point should the first version solve?
4. Which resources can be booked independently, and which depend on employees, rooms, or equipment?
5. Which workflows need custom software versus an established product or service?
6. What information should remain confidential and therefore out of this public repository?

## 6. Next discussion

Walk through one real-world reservation or guest journey from first contact to final settlement. Record the process, exceptions, and current problems before designing the solution.
