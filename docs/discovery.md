# Discovery — working notes

**Status:** Ongoing interview. This is a record of current intent and questions, **not** an approved specification. Do not invent answers.

## Agreed working model

- The owner supplies business knowledge and approves product decisions; agents help structure research and later build approved slices.
- Plan the full business broadly; detail only the current problem or next feature.
- Keep canonical knowledge in versioned Markdown, with visual maps as optional views.
- Separate **Confirmed**, **Proposed** and **Open question** statements.
- The repository is public: do not record personal, confidential operational or real financial data.

## Business areas to explore

These are **proposed investigation areas**, not approved modules:

| Area | Things to understand |
| --- | --- |
| Customer experience | Website, services, offers, guest journey, communications |
| Booking & availability | Reservable resources, overlaps, cancellations, pricing, external channels |
| Reception & CRM | Guest arrival, stay, extras, checkout, contact history |
| People & operations | Availability of employees, schedules, time worked, service delivery |
| Payments & reporting | Deposits, refunds, guest balances, revenue/cost visibility |
| Events & packages | Multi-resource bookings and group workflows |
| Integrations | Existing tools, payment/fiscal/accounting services and channel managers |

## First discovery questions

1. **Current operations:** which concrete business processes and tools already exist, and what causes the most manual work or mistakes?
2. **Target outcomes:** what should change for the owner, employees and guests when the platform is used?
3. **Offer and resources:** what can actually be booked, sold, bundled or reserved; what competes for the same capacity?
4. **Exception flows:** what happens with cancellations, no-shows, changes, overbooking, deposits and staff absence?
5. **Constraints:** what existing integrations, data-protection obligations, operational costs and real-world limitations must we respect?

## Session record template

When a substantive conversation produces new information, update the appropriate section or append a short entry:

- **Date / topic:**
- **Confirmed business facts:** (with source or owner confirmation)
- **Proposed options:** (with trade-offs; not decisions)
- **Open questions / assumptions to verify:**
- **Approved decisions:** (link to decision record when material)
- **Next interview topic:**

Avoid dumping full chat transcripts into the repository. Distill findings, preserve uncertainties, and update existing entries instead of repeating them.

## Next discussion

Clarify the guest account / on-site charges workflow (who opens it, what it is linked to, and how settlement works); then trace accommodation booking from website and staff channels to a single availability source.

## Discovery session — 2026-11-09: initial platform areas (owner input)

**Scope of these statements:** capabilities the owner wants the *future* platform to support. They do not establish that these capabilities already exist in today's tools.

### Confirmed business requirements / intended capabilities

**Public website and accommodation booking**
- The public website is a fast, modern, content-managed brand and offer presentation, **not WordPress**.
- Editors should be able to maintain content; event announcements may be displayed periodically.
- The site needs a contact form.
- Accommodation needs individual listings/offer pages and a booking flow with calendar, dates and availability. Booking.com/Airbnb are UX references, **not a requirement to replicate their entire feature sets**.
- The listing details, prices, booking rules, and external integration strategy are not designed yet.

**Staff-facing operational panel**
- Staff must be able to record their working days and hours; whether the entry is daily totals or exact start/end times is undecided.
- When a customer arrives at the property, staff should be able to open a customer bill/tab, add charges for products/services over the visit and close it at settlement.
- The business currently refers to card, BLIK, terminal and fiscal cash register for on-site settlement. The software's exact interaction with those devices/providers is **not yet defined**.
- Staff need access to lodging availability and must be able to create accommodation reservations manually when a customer calls by phone.
- Staff should only access capabilities needed for their responsibilities. Aggregate/sensitive financial access is reserved for administrative or supervisory roles.

**Management and reporting**
- Owners/managers should be able to analyze sales by business category: e.g., gastronomy, accommodation, and services.
- Percentage breakdowns, turnover and revenue metrics are desired; their exact accounting definitions, filters, tax treatment and attribution rules must be specified.

### Proposed decomposition — for analysis, NOT approved architectural modules

- Public web, content and accommodation listings
- Booking, shared availability and accommodation inventory
- On-site guest tabs, charges and settlement workflow
- Employees and work-time records
- Financial visibility and category reporting
- Identity, access control and staff roles
- Payment, fiscal and external-channel integrations

A role-aware internal panel may cover multiple business areas. The number of deployed apps (two or three), CMS, backend structure, and technology choices remain undecided.

### Open questions / dependencies to validate

1. Are customer tabs created for day-SPA guests, lodging guests, or both? Is a tab per person, group, room or visit? Can a customer have several tabs?
2. Are lodging reservations and on-site tabs separate concepts, and at what point are they linked?
3. Which inventory/resources and booking rules exist today (rooms, accommodation units, capacity, check-in/out, packages)? How are phone bookings and online availability reconciled?
4. Are payments registered manually as settlement methods, or must the platform integrate with terminal, BLIK provider, payment gateway and fiscal devices? What happens on partial payment, split bills and refunds?
5. Who enters time worked, who approves or corrects it, and does time tracking feed payroll or only reports?
6. Which roles may see itemized customer bills versus aggregate sales, costs, profits and employee compensation?
7. Are revenue/turnover metrics gross, net, cash received, or accrued? Which categories should each purchased item belong to?
8. What current tools, devices, and manual processes must be kept, replaced or integrated?

### High-level risks to investigate

- Preventing duplicate availability allocations when online and phone booking occur concurrently
- Safe handling of customer and employee personal data
- Accurate, auditable settlement and separation of transaction totals from analytical financial data
- Role-based access to sensitive reports versus daily operational tasks

### Next interview topic

Walk through **a real on-site guest visit**, from arrival and tab creation, through posting purchases, to closing the tab and collecting payment. Then map its relationship to accommodation bookings.

## Discovery session — 2026-11-13: business coverage and customer account timing

**Source:** owner's answers to the 20-question discovery survey, plus follow-up clarifications. These are requirements for the future product, **not** confirmation of current implementations or first-release priority.

### Confirmed direction

- **Purpose and scope:** one Rivé property. Primary business outcomes: customer settlements and financial control, workforce management, and growth through online sales. The owner selected all suggested first-delivery areas, so **delivery priority remains unresolved**.
- **Existing setup:** fiscal register, payment terminal, and separate applications; exact vendors/integrations remain to be inventoried.
- **Offer:** accommodation, day SPA/sauna/pool/massages, gastronomy, events, packages, vouchers, group/private rentals.
- **Accommodation:** rooms/units and other offer-specific booking modes. Booking rules vary by offer.
- **Availability:** SPA services can depend on capacity, rooms, equipment and employee availability simultaneously.
- **Pricing:** fixed, seasonal/weekend/holiday, party-size/duration, package/discount and channel-dependent variants are in scope for analysis. Separate bookings, add-ons, and combined carts may all be needed depending on offer.
- **Guest account/folio:** an open bill/account is **assigned to a customer** and may be opened **during booking or on arrival**. For the same booking/stay, **one shared customer account** is intended to cover accommodation charges, deposit payments, gastronomy, SPA services, other purchases and final settlement. Deposits are payments against the balance, not duplicate charge items. The rules for groups, multiple concurrent accounts and settlement splits remain open.
- **Settlement:** payment in full at visit end; deposits/balances; split payments by person or method; partial payments and refunds. These are supported business scenarios, not a selected payment processor or fiscal integration design.
- **Gastronomy:** product-and-price catalog plus adding items to customer accounts; inventory management was not selected.
- **Staff:** staff enter their own hours, work schedules/absences and internal compensation calculation. **Manager approval of time records remains open** (not selected, not rejected).
- **Facility operations:** room readiness/cleaning status, cleaning tasks and faults/blocks of resources.
- **Finance:** sales/revenue by category, payments/deposits/outstanding balances, costs/margins/profit, period comparison, budgeting and forecasting; financial definitions are not specified.
- **Prioritized integrations:** Booking.com/Airbnb/channel manager; BLIK, terminal and online payments; email/SMS/calendar. **Accounting/KSeF/fiscal integration is unprioritized, not excluded**.
- **Identity/permissions:** simple roles plus permissions by function and specific data/operations.
- **Business continuity:** a manual fallback procedure is acceptable in case of outage (no commitment to offline-first).
- **Delivery approach:** longer business discovery and architecture planning before development. 

### Key questions to resolve next (customer account and booking)

1. **Confirmed:** for the same customer/booking/stay, one common account carries accommodation charges, deposit payments and on-site purchases. **Open:** when do individual charges become payable and how is the deposit displayed/applied?
2. Is an account per customer **per visit/stay**, or can one customer keep multiple concurrent open accounts or a persistent account across visits?
3. Can a booking for a couple/family/group produce one customer's account, multiple accounts, or transfers/split settlement?
4. When is an accommodation charge actually added — at booking, arrival, departure, or another business milestone? How are deposits shown and applied?
5. Can day guests without accommodation reservations have accounts? Who may open, adjust, split and close them?
6. Which business events trigger refunds, credit notes/adjustments and fiscal documents?

**Next discovery prompt:** a couple or family reserves one room. Who owns the common account, who can add charges, and may members pay separately? Compare this with a solo guest.

## Discovery session — 2026-11-13: common bill confirmed

**Owner-confirmed business decision:** choose **A — one common customer bill** for a booking/stay. The same bill is used for accommodation, deposit(s), gastronomy, SPA purchases and the final settlement. It may originate at booking or on arrival. This confirms **the business behavior**, not a database entity design or fiscal treatment.

**Important financial distinction (design constraint for later validation):** a booked accommodation charge or SPA purchase increases the amount due; a deposit or later payment reduces the outstanding balance. The system must avoid counting a deposit twice as revenue/sale. Exact accounting/fiscal treatment remains subject to research.

**Still open:** detailed timing and rules of allocating charges or payments across people; whether a customer may have several simultaneous bills; cancellations and refunds; when a charge is posted and a bill can be closed; day-guest account creation rules.

**Next question answered:** option C — a shared bill by default with the ability to split charges or payments between people. Exact bill owner/booking contact, timing of split, reassignment of items, deposit allocation and fiscal treatment remain to be determined.

## Discovery session — 2026-11-13: flexible group settlement confirmed

**Owner-confirmed business requirement:** for couples, families and groups the default is **one shared customer bill** for a reservation/stay. Authorized reception staff must be able to **split individual charges among guests or accept separate payments from multiple people**. This extends (rather than replaces) the shared-bill rule. Do not assume a separate account is automatically created for each guest.

**Open questions:** whether the bill is assigned to the booking contact or another customer; whether staff can allocate charges to specific people while the bill is still open or only at settlement; treatment of deposits during splitting; corrections after partial payment; whether any transfer creates a separate bill or fiscal document. No technical or fiscal implementation has been chosen.

**Next interview question:** should charges be assigned to particular people throughout the stay, or only when the shared bill is settled?
