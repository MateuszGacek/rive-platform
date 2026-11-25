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

**Owner-confirmed follow-up (option C):** authorized staff may attribute individual purchases or services to particular guests **as they are added during the stay**, and can **adjust these allocations at final settlement**. The shared customer bill remains the default; this does not require one separate bill per person.

**Open questions:** whether the shared bill is assigned to the booking contact or another customer; treatment of deposits during splitting; whether already-paid/partially-paid items can be reassigned or require corrections; whether transfers create separate bills or fiscal documents. No technical or fiscal implementation has been chosen.

**Next interview question:** does a walk-in day-SPA customer without a reservation receive a guest bill that stays open for purchases, or can they also buy services and settle immediately without an open bill?

## Discovery synthesis — 2026-11-13

The owner supplied Discovery v2, a market segment review, and a stage-one hotel/SPA research export. The [capability map](product/capability-map.md) reflects the owner survey and follow-ups above. The research introduces options and checks, including timed admission, capacity, mapping guest identities across tools, and a purchased core with a limited custom layer. It does not settle any vendor, build-vs-buy outcome, or first release.

- Start by observing reception, including a shared group bill and a day guest. Confirm the day-guest path, then check the real timing and pricing rules for admissions.
- Compare scenarios across candidate tools, including cases in which the folio is assigned to a customer and used by multiple people. Document who owns each fact and how errors are resolved.
- Work from the [open questions](product/open-questions.md), [benchmark and demo script](research/hotel-spa-benchmark.md), and [agent delivery plan](product/agent-delivery-plan.md). Keep source financials and vendor quotes outside the public repository.

## Warsztat recepcji

Przebiegi wizyty Day SPA i pobytu grupowego z zaliczką są przygotowane do rozmowy z właścicielem. [Materiały warsztatowe](product/reception-discovery.md)

## Pomysł do oceny — hosting przyjazny agentom (2026-11-17)

**Źródło:** sugestia właściciela. **Proposed:** sprawdzić Vercel oraz inne opcje hostingu pod kątem współpracy z agentami. Deklarowana dobra współpraca Vercel z agentami wymaga weryfikacji; nie wybrano dostawcy ani architektury.

**Open question:** jakie możliwości i ograniczenia dla agentów, bezpieczeństwo, koszty, obsługa danych oraz potrzeby przyszłej platformy mają poszczególne opcje?

## Wywiad z właścicielem — wejścia do ośrodka (2026-11-19)

**Confirmed** — uzgodniono warianty dostępu w pakietach noclegowych oraz rezerwację, pomiar czasu i rozliczenie wizyt dziennych. Reguły spóźnienia i częściowego przybycia grupy oraz przypadki do sprawdzenia przed wdrożeniem są w [notatce recepcji](product/reception-discovery.md#day-spa-bez-noclegu).

## Wywiad z właścicielem — oferta noclegowa (2026-11-19)

**Confirmed** — obecna oferta obejmuje studia, apartamenty i domki. Typy noclegów i skład oferty mają się dać edytować. Poszczególne jednostki mogą różnić się układem i cechami. [Pakiety noclegowe z dostępem do ośrodka](product/reception-discovery.md#pakiety-noclegowe-z-dostępem-do-ośrodka) są odrębnym wyborem w ramach oferty.

**Confirmed — właściciel, 2026-11-19, potwierdzone ponownie 2026-11-21.** Gość rezerwuje wybraną opcję noclegu, np. studio dwuosobowe. Jednostki tego samego typu o różnej pojemności są osobnymi opcjami w ofercie i mają osobne pule dostępności. Jeśli w danym terminie są wolne trzy studia dwuosobowe, jedna rezerwacja zajmuje jedno studio z tej puli. Recepcja przypisuje konkretną jednostkę i może później zmienić przydział.

**Confirmed** — liczba gości może być mniejsza niż pojemność wybranej opcji. Dwie osoby mogą zarezerwować studio czteroosobowe. Rezerwacja zajmuje całą jednostkę.

**Confirmed — korekta właściciela, 2026-11-21.** Na start jedno zamówienie na stronie obejmuje jedną jednostkę. Gość, który potrzebuje kolejnej jednostki, składa osobne zamówienie. Właściciel wycofał wcześniejszą zgodę na kilka jednostek w jednym zamówieniu, żeby uprościć obsługę. Źródło: rozmowa z właścicielem.

**Research — 2026-11-19.** Domki Mszana stosują cenę za czteroosobowy domek niezależną od liczby gości. Apartamenty River w Wiśle stosują bazę dla dwóch osób i dopłatę za każdą kolejną. Hotel & SPA Jawor publikuje różne podstawy wyceny pakietów, m.in. pakiet pobytowy SPA za osobę i ofertę dla par za pokój. To przykłady z publicznych ofert. [Domki Mszana](https://rudawkarymanowska.pl/noclegi/domki-mszana-4-osobowe/) · [Apartamenty River](https://apartamentyriver.pl/cennik/) · [Pakiety Hotelu Jawor](https://hotel-jawor.pl/pakiety/)

**Confirmed — cena samego noclegu.** Stawka jest za całą jednostkę za noc. Dla tej samej opcji i terminu liczba gości mieszcząca się w limicie nie zmienia ceny noclegu.

**Confirmed — dostęp w pakiecie.** Cena dostępu do ośrodka zależy od liczby osób objętych pakietem. Dostęp można kupić dla części gości z jednej rezerwacji, np. dla dwóch z czterech osób nocujących w studiu. Na stronie gość podaje liczbę osób z dostępem, a recepcja przypisuje go konkretnym uczestnikom na miejscu.

**Proposed — przebieg WWW i e-mail.** Gość wybiera daty i liczbę osób, wybiera dostępną opcję noclegu i wariant dostępu do ośrodka, sprawdza łączną cenę i warunki oraz podaje dane rezerwującego. Po potwierdzeniu rezerwacji e-mail zawiera daty, opcję noclegu, liczbę gości, zasady dostępu do ośrodka, łączną cenę i informacje o płatności zgodne z wybranymi warunkami.

**Research — potwierdzanie noclegu, 2026-11-19.** Beskidzkie Apartamenty w Szczyrku potwierdzają rezerwację po wpłacie 50% zaliczki w ciągu 24 godzin. Beskidy To Tu wymagają co najmniej 30% przedpłaty w ofercie standardowej oraz 100% w ofercie bezzwrotnej. Accor publikuje także elastyczną taryfę bez przedpłaty. To przykłady warunków konkretnych ofert. [Beskidzkie Apartamenty](https://beskidzkieapartamenty.pl/wp-content/uploads/2021/06/regulamin-sun-sport.pdf) · [Beskidy To Tu](https://beskidytotu.pl/regulamin/) · [Accor](https://all.accor.com/a/pl/deals-corner.html)

**Confirmed — nocleg z zaliczką.** Po przyjęciu formularza tymczasowo zajmujemy jedno miejsce w puli wybranej opcji noclegu, pokazujemy termin płatności i wysyłamy e-mail z linkiem do płatności. Po potwierdzeniu wpłaty rezerwacja staje się potwierdzona, a gość otrzymuje osobny e-mail. Gdy termin płatności upłynie bez wpłaty, miejsce wraca do puli. Zaliczka pomniejsza saldo pobytu.

**Research — wysokość zaliczki i czas blokady, 2026-11-19.** Booking.com pozostawia kwotę i termin przedpłaty w warunkach oferty obiektu. Airbnb pokazuje kwotę i harmonogram dla kwalifikujących się rezerwacji. Połowa ceny jest w dokumentacji przykładem płatności dzielonej, a 24 godziny na poprawienie płatności po akceptacji prośby przez gospodarza to odrębny przypadek. [Booking.com](https://secure.booking.com/faq.en-gb.html?aid=330843) · [Airbnb — płatności dzielone](https://www.airbnb.com/help/article/2143) · [Airbnb — oczekiwanie na wpłatę](https://www.airbnb.com/help/article/2411)

**Research — porównanie terminów, 2026-11-19.** Przy szybkiej płatności online Mews domyślnie trzyma wstępną rezerwację przez 15 minut, a Noclegi.pl daje 30 minut na finalizację wymaganej przedpłaty przed zwolnieniem dostępności. W ofertach bezpośrednich Beskidzkie Apartamenty podają 50% zaliczki w 24 godziny, a Rudawka Rymanowska 30% w trzy dni od potwierdzenia. Terminy tych ofert dotyczą wpłaty, więc nie przesądzają długości blokady w formularzu online. [Mews](https://help.mews.com/s/article/payments-through-the-mews-booking-engine) · [Noclegi.pl](https://noclegi.pl/warunki-korzystania-26082026) · [Beskidzkie Apartamenty](https://beskidzkieapartamenty.pl/wp-content/uploads/2021/06/regulamin-sun-sport.pdf) · [Domki Mszana](https://rudawkarymanowska.pl/noclegi/domki-mszana-4-osobowe/)

**Confirmed — zaliczka i czas blokady.** Na start zaliczka wynosi 30% łącznej ceny rezerwacji, w tym wybranego pakietu. Od przyjęcia formularza gość ma dwie godziny na szybką płatność online albo 24 godziny na zwykły przelew. Dwie godziny dają czas na powrót do płatności po przerwie lub w podróży. Procent zaliczki i terminy mają się dać łatwo zmienić.

**Confirmed — dopłata po zaliczce.** Pozostałą kwotę można zapłacić przy zameldowaniu albo przy wyjeździe. Moment dopłaty wybiera recepcja (potwierdzenie właściciela, 2026-11-21).

**Confirmed — właściciel, 2026-11-21.** Strona może przyjmować rezerwacje noclegów również w dniu przyjazdu, bez dodatkowej godziny odcięcia sprzedaży. Dla rezerwacji na dziś jedyną opcją wpłaty zaliczki przez stronę jest szybka płatność. Dostępność wybranej opcji pozostaje warunkiem rezerwacji. Źródło: rozmowa z właścicielem.

**Confirmed — cel biznesowy, właściciel 2026-11-24.** Przy rezerwacji na ostatnią chwilę gość ma mieć prostą drogę do zarezerwowania wolnego noclegu. Jeśli nie może dokończyć rezerwacji na stronie, powinien móc łatwo skontaktować się z recepcją. Właściciel wskazał do rozważenia telefoniczne potwierdzenie bez zaliczki dla gościa dzwoniącego tuż przed przyjazdem.

**Proposed — rezerwacja na ostatnią chwilę, 2026-11-24.** Na stronie gość może szybko zakończyć rezerwację, płacąc online. Przy problemie z płatnością albo braku czasu na zwykły przelew strona pokazuje akcję „Zadzwoń do recepcji”. Jeśli gość rozpoczął już rezerwację online, recepcja odszukuje ją i sprawdza status wpłaty oraz blokady. **Open question.** Od kiedy strona przestaje oferować zwykły przelew przy przyjeździe następnego dnia?

**Confirmed — właściciel, 2026-11-24.** Recepcja może według własnej oceny potwierdzić telefonicznie dostępny nocleg bez zaliczki, z płatnością na miejscu. Dotyczy to rezerwacji na ostatnią chwilę i na dalszy termin. Po potwierdzeniu rezerwacja zajmuje miejsce w puli. Źródło: warsztat noclegów, wybór wariantu C.

**Confirmed — właściciel, 2026-11-21.** Jeśli gość opłaci zaliczkę zwykłym przelewem po terminie, a zwolnione miejsce zostało już sprzedane, wpłata trafia do obsługi przez recepcję. Wygasła rezerwacja nie zostaje potwierdzona. Jeśli miejsce jest nadal dostępne, recepcja może przywrócić rezerwację i zaliczyć wpłatę na jej poczet. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-21.** Na początek recepcja ręcznie potwierdza wpłatę zwykłym przelewem w panelu po sprawdzeniu, że środki wpłynęły. Źródło: rozmowa z właścicielem.

**Research — zwroty szybkich płatności, 2026-11-21.** [PayU](https://developers.payu.com/europe/pl/docs/payment-flows/refunds/) i [Przelewy24](https://developers.przelewy24.pl/) udostępniają zlecanie zwrotów i powiadomienia o wyniku. Przy ocenie operatora sprawdzić ochronę przed ponownym zleceniem tego samego zwrotu, potwierdzenie wykonania i obsługę błędów. Wybór operatora i zakres automatyzacji pozostają otwarte.

**Confirmed — właściciel, 2026-11-21.** Na początek przy anulowaniu noclegu z prawem do zwrotu system wylicza kwotę i pokazuje sprawę do rozliczenia, a recepcja ręcznie zleca zwrot. Źródło: rozmowa z właścicielem.

**Open question** — jak potwierdzamy wykonanie zwrotu i uzgadniamy dokumenty? Jak termin wpłaty ma działać przy rezerwacji blisko przyjazdu? Które różnice poza pojemnością tworzą osobną opcję noclegu?

## Kierunek warsztatu produktu — 2026-11-20

**Confirmed — właściciel.** Najpierw chcemy szeroko poznać wszystkie 15 obszarów platformy i ich zależności, a dopiero stopniowo szczegółowo projektować wybrane procesy. Rozmowa może przechodzić między tematami bez zamykania wszystkich decyzji i bez wyboru pierwszego pilota. Celem jest spójny produkt, nie przyspieszenie implementacji.

**Confirmed — sposób pracy.** Omawiamy funkcje na przykładach, rozróżniając rezerwację i faktyczny pobyt lub wizytę, rachunek i wpłatę oraz planowaną dostępność i obecność. Rekomendacje i obserwacje audytu nie stają się decyzjami bez potwierdzenia właściciela. Jedno główne pytanie prowadzi kolejną rundę rozmowy.

**Open question.** Kolejność obszarów warsztatu jest robocza i może się zmieniać; wybór pilota i podejścia do dostawy pozostaje osobną późniejszą decyzją. Źródło: rozmowa z właścicielem, 2026-11-20.

## Oferta i dalszy rozwój — 2026-11-20

**Confirmed — właściciel.** Poza noclegiem i wejściem do ośrodka dostępne są masaże oraz gastronomia na terenie obiektu. W przyszłości planowane są wydarzenia oraz osobna marka RO.

**Open question.** RO może być osobnym projektem z możliwym powiązaniem z rivé; charakter marki, zakres i sposób powiązania nie zostały ustalone. Nie przesądza to wspólnych danych, sprzedaży ani architektury. Źródło: rozmowa z właścicielem, 2026-11-20.

**Confirmed — właściciel, 2026-11-20.** Masaże będą umawiane wyłącznie telefonicznie przez recepcję. Sposób prowadzenia grafiku i wewnętrznej rejestracji nie został ustalony.

**Confirmed — właściciel, 2026-11-20.** Recepcja może widzieć i zapisywać terminy masaży w panelu rivé, aby ułatwić organizację. Goście umawiają je telefonicznie. Szczegóły grafiku i dostępności pozostają do zaprojektowania.

**Confirmed — właściciel, 2026-11-24.** Recepcja ustala dostępność bezpośrednio z masażystą i zapisuje uzgodniony termin w panelu. Źródło: warsztat masaży, wybór wariantu C.

**Confirmed — właściciel, 2026-11-24.** Pracownik oznacza masaż jako wykonany, a system automatycznie dopisuje cenę do otwartego rachunku gościa. Źródło: warsztat masaży, wybór wariantu A.

**Confirmed — właściciel, 2026-11-24.** Pierwsza oferta voucherów obejmie vouchery kwotowe i vouchery na określone usługi. Konkretne kwoty, długości wizyt i warianty usług pozostają do dopracowania. Źródło: warsztat voucherów, wybór wariantu C.

**Confirmed — właściciel, 2026-11-24.** Kupiony voucher zachowuje warunki obowiązujące przy zakupie. Zmiany oferty, np. zmiana długości masażu, stosujemy przy kolejnych zakupach. Źródło: warsztat voucherów, wybór wariantu A.

**Confirmed — właściciel, 2026-11-24.** Voucher kwotowy można wykorzystywać w częściach. Po opłaceniu rachunku pozostałe saldo można wykorzystać przy następnej wizycie. Przykład syntetyczny: z vouchera na 200 zł po opłaceniu rachunku za 120 zł pozostaje 80 zł. Źródło: warsztat voucherów, wybór wariantu A.

**Confirmed — właściciel, 2026-11-24.** W pierwszej wersji oferty voucherów sprzedaż odbywa się na stronie oraz w recepcji. Oba kanały korzystają z tej samej oferty. Źródło: warsztat voucherów, wybór wariantu A.

**Confirmed — właściciel, 2026-11-24.** W pierwszej wersji wydarzeń gość może kupić bilet na stronie i otrzymać potwierdzenie zakupu. Źródło: warsztat wydarzeń, wybór wariantu C.

**Confirmed — właściciel, 2026-11-24.** Wydarzenie ma własny limit biletów. Przy jego tworzeniu obsługa może na czas wydarzenia zmniejszyć pulę Day SPA lub zarezerwować ośrodek na wyłączność. Źródło: warsztat wydarzeń, wybór wariantu A.

**Confirmed — właściciel, 2026-11-24.** Obsługa może od razu ograniczyć przyjmowanie nowych rezerwacji Day SPA w terminie wydarzenia. Już potwierdzone rezerwacje pozostają ważne. Kolidujące rezerwacje trafiają na listę spraw do rozwiązania przez recepcję. Źródło: warsztat wydarzeń, wybór wariantu B.

**Confirmed — właściciel, 2026-11-24.** Po odwołaniu wydarzenia z opłaconymi biletami obsługa rozpatruje każdy zakup osobno i uzgadnia z gościem rozwiązanie, np. zwrot albo przeniesienie na inny termin. Źródło: warsztat wydarzeń, wybór wariantu C.

**Confirmed — właściciel, 2026-11-20.** Z gastronomii mogą korzystać zarówno goście korzystający z ośrodka, jak i goście noclegowi, w tym zamawiając śniadanie lub inne jedzenie. Obecnie nie ma dowozu ani sprzedaży na zewnątrz.

**Confirmed — właściciel, 2026-11-21.** Śniadanie jest opcjonalnym dodatkiem przy rezerwacji noclegu przez WWW. Gość może też dokupić je na miejscu i dopisać do rachunku pobytu. Przy rezerwacji online może wybrać śniadania dla wszystkich osób na cały pobyt albo wskazać wybrane dni i liczbę osób dla każdego z nich. Źródło: rozmowa z właścicielem.

**Proposed — właściciel, 2026-11-21.** W wariancie z wybranymi dniami pokazać kalendarz pobytu, w którym gość zaznacza dni śniadań i liczbę osób.

**Confirmed — właściciel, 2026-11-21.** Kuchnia widzi w panelu dzienną listę śniadań zamówionych online i dokupionych na miejscu. Przy zamówieniu można zapisać opcjonalną notatkę o godzinie śniadania, widoczną dla kuchni. Źródło: rozmowa z właścicielem.

**Proposed — właściciel, 2026-11-20.** Sprzedaż na zewnątrz lub dowóz mogą być kierunkiem na przyszłość; zakres i decyzja o wprowadzeniu pozostają otwarte.

**Confirmed — kierunek warsztatu, 2026-11-20.** Właściciel wybiera kompleksowe omówienie noclegów, w tym pełnej drogi gościa i zależności, z zamiarem domknięcia tego obszaru. Nierozstrzygnięte reguły pozostają otwarte do wyraźnej decyzji.

**Confirmed — korekta właściciela, 2026-11-20.** Dodatkowe filtrowanie ofert noclegowych jest wskazane. Wcześniejsza interpretacja wypowiedzi jako rezygnacji z filtrowania była błędna. Konkretne filtry i ich relacja do gwarantowanych cech oraz do puli lub konkretnych jednostek pozostają do ustalenia.

**Confirmed — doprecyzowanie właściciela, 2026-11-24.** Przy kilku lub kilkunastu pozycjach oferta noclegowa ma mieć prostą wyszukiwarkę z ograniczoną liczbą filtrów. **Proposed.** Zacząć od terminu i liczby osób. Rodzaj noclegu pokazać na liście, a dodatkowy filtr dodać, jeśli pomaga wybrać spośród faktycznie dostępnych ofert. Cechy takie jak taras omówić przy opisie i gwarancjach oferty.

**Confirmed — doprecyzowanie właściciela, 2026-11-20.** Recepcja potrzebuje możliwości zmiany przydziału noclegu, np. przeniesienia osoby niekorzystającej z ośrodka do studia dalej od niego. Właściciel wskazał też, że na stronie nie zawsze jest jasne, którą konkretnie jednostkę wynajęto.

**Historia decyzji — relacja do wcześniejszej reguły puli.** W rozmowie właściciel potwierdził przykład ofert odpowiadających konkretnym jednostkom, po czym doprecyzował potrzebę elastycznego przenoszenia i niejednoznaczną widoczność jednostki na stronie. Ustalić, co dokładnie gość wybiera i ma zagwarantowane oraz czy i kiedy recepcja może to zmienić. Źródło: rozmowa z właścicielem, 2026-11-20.

**Confirmed — korekta właściciela, 2026-11-21.** Gość wybiera na stronie rodzaj noclegu, a recepcja później przydziela konkretną jednostkę. Rozważany wcześniej wybór konkretnej jednostki na stronie został cofnięty. Przykład warsztatowy: 14 jednostek w czterech rodzajach. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Recepcja decyduje o doborze i podmianie jednostki dla gościa; system nie musi ograniczać tej decyzji regułą równoważności. Właściciel powierza właściwy dobór recepcji. Sposób prezentacji oferty i techniczne skutki zmiany dla dostępności pozostają do omówienia. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Przy zmianie przydziału recepcja może po ostrzeżeniu zapisać wybór jednostki zajętej w nakładającym się terminie. Rozwiązanie konfliktu może wymagać kolejnych przesunięć; takie zmiany muszą być dozwolone. Sposób oznaczenia i rozwiązania konfliktu oraz jego wpływ na sprzedaż pozostają do ustalenia. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Dostępność ma zapobiegać podwójnej sprzedaży lub nakładającym się rezerwacjom bez możliwego zakwaterowania, ale nie powinna niepotrzebnie blokować sprzedaży, gdy gościowi można zapewnić nocleg. **Open question:** jak rozstrzygać rzeczywistą dostępność podczas nierozwiązanego konfliktu przydziałów i które przesunięcia wolno uwzględniać. Źródło: rozmowa z właścicielem.

**Confirmed — korekta właściciela, 2026-11-20.** Dwa nakładające się przydziały nie mogą być zapisane do tej samej jednostki noclegowej. Przy przeniesieniu do zajętego studia trzeba również przenieść dotychczas przypisanego gościa. To zastępuje wcześniejsze ustalenie z tej rozmowy, że konflikt można zapisać po ostrzeżeniu. Gdy system nie potrafi ustalić dostępności, termin ma być niedostępny online. **Open question:** szczegółowy przebieg zamiany i obsługa braku miejsca zastępczego. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Recepcja może zamienić dwa przydziały w jednej operacji. Zmiana jest zapisywana po sprawdzeniu poprawności obu przydziałów, tak aby nie powstało nakładanie w jednej jednostce. Źródło: rozmowa z właścicielem.

**Confirmed — doprecyzowanie właściciela, 2026-11-24.** Recepcja samodzielnie decyduje o przeniesieniu gościa między jednostkami, także między różnymi opcjami noclegu. System sprawdza dostępność jednostek w terminie przed zapisem wyboru recepcji. Obowiązuje ustalona możliwość zapisania poprawnej zamiany dwóch przydziałów w jednej operacji. Źródło: warsztat noclegów, wariant D.

**Confirmed — właściciel, 2026-11-24.** Zmiana przydziału jednostki, również na inną opcję noclegu, zachowuje dotychczasową cenę rezerwacji. Jeśli recepcja uzgodni z gościem inną cenę, wprowadza ją osobną czynnością. Źródło: warsztat noclegów, wybór wariantu A.

**Confirmed — właściciel, 2026-11-24.** W potwierdzeniu gość widzi zarezerwowaną opcję noclegu, np. studio dwuosobowe. Konkretną jednostkę podaje recepcja przy zameldowaniu. Źródło: warsztat noclegów, wybór wariantu A.

## Zmiana terminu noclegu — 2026-11-20

**Confirmed — właściciel.** Gość ma móc zmienić termin noclegu przez link, z ograniczeniem przed przyjazdem. Jeśli system nie pozwoli na zmianę, gość kontaktuje się z recepcją. Dokładny próg pozostaje otwarty.

**Research — 2026-11-20.** [Airbnb](https://www.airbnb.com/help/article/913) opisuje dla rezerwacji domów wniosek o zmianę wymagający zgody gospodarza; cena może się zmienić, a przy braku zgody pierwotna rezerwacja pozostaje. [Booking.com](https://secure.booking.com/faq.en-gb.html?aid=330843) uzależnia zmiany od warunków obiektu i oferty. W Wiśle [Willa pod Starą Skocznią](https://willapodstaraskocznia.pl/) podaje jednorazową bezpłatną zmianę co najmniej 14 dni przed przyjazdem, zależną od dostępności; [Wielka Niedźwiedzica](https://wielkaniedzwiedzica.pl/regulamin-platnosci-i-anulacje/) wymaga kontaktu z obsługą i dostępności, a przy droższym terminie dopłaty. [Panorama Górska](https://panorama-gorska.pl/regulamin/) rozpatruje zmianę indywidualnie. To przykłady zasad obiektów, nie dowód powszechnej praktyki ani terminów automatycznej zmiany online.

**Open question.** Ustalić termin samodzielnej zmiany, warunki taryfowe, różnicę ceny i rozliczenie zaliczki oraz moment zwolnienia pierwotnego terminu. Źródło: rozmowa z właścicielem i wskazane strony, 2026-11-20.

**Confirmed — właściciel, 2026-11-20.** Samodzielna zmiana terminu noclegu przez link ma być dostępna z co najmniej tygodniowym wyprzedzeniem; przy krótszym czasie gość kontaktuje się z recepcją. Propozycja 48 godzin została odrzucona jako zbyt krótka. **Open question:** dokładna godzina graniczna i zasady wyjątków obsługiwanych przez recepcję. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Po zmianie terminu nocleg jest wyceniany według aktualnego cennika dla nowego terminu, ponieważ ceny dni mogą się różnić. **Proposed:** przed zatwierdzeniem pokazać starą i nową cenę oraz różnicę. Rozliczenie różnicy i zaliczki pozostaje otwarte. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Przy zmianie noclegu na droższy termin różnicę gość dopłaca na miejscu wraz z pozostałą należnością; nie jest wymagana kolejna płatność w trakcie zmiany. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Tańszy termin zmniejsza należność na rachunku, rozliczaną później na miejscu. **Open question:** obsługa przypadku, gdy wpłacona już zaliczka przekracza nową należność. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Jeżeli po zmianie terminu wpłacona zaliczka przekracza należność za nocleg, nadpłatę można wykorzystać na inne zakupy na rachunku, a niewykorzystaną część zwrócić przy wyjeździe. Sposób zwrotu i dokumenty pozostają do uzgodnienia. To odpowiada na wcześniejsze pytanie o nadpłatę. Źródło: rozmowa z właścicielem.

## Anulowanie noclegu — 2026-11-20

**Confirmed — właściciel.** Gość ma również móc anulować nocleg samodzielnie przez link. Warunki anulacji i zwrotu nie zostały jeszcze wybrane.

**Research — 2026-11-20.** [Airbnb](https://www.airbnb.com/help/article/3066) pokazuje gościowi kwotę zwrotu przed anulowaniem; zależy ona od warunków rezerwacji i czasu. [Hotel Beskid w Milówce](https://hotelbeskid.com/regulamin/) opisuje anulowanie w systemie według warunków oferty. [Beskidzki Raj](https://www.beskidzkiraj.com/hotel/warunki-rezerwacji) wymaga kontaktu z recepcją, dopuszcza bezkosztową anulację na 7 dni przed przyjazdem i opisuje brak zwrotu przedpłaty przy późniejszej anulacji. To przykłady konkretnych ofert, a nie wspólna reguła rynku.

**Open question.** Ustalić granicę zwrotu i skutki późniejszej anulacji osobno od samej możliwości anulowania przez link oraz od zasad zmiany terminu. Źródło: rozmowa z właścicielem i wskazane strony, 2026-11-20.

**Confirmed — właściciel, 2026-11-20.** Przy anulowaniu noclegu co najmniej siedem dni przed przyjazdem gościowi przysługuje pełny zwrot zaliczki. Warunki późniejszego anulowania pozostają otwarte. Właściciel chce najpierw dopracować zasady, a podsumowanie przygotować później. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Gość może anulować nocleg przez link również mniej niż siedem dni przed przyjazdem. Możliwość anulowania jest odrębna od nieustalonych skutków finansowych późnej anulacji. Źródło: rozmowa z właścicielem.

**Research — późna anulacja, 2026-11-20.** [Beskidzki Raj](https://www.beskidzkiraj.com/hotel/warunki-rezerwacji) podaje brak zwrotu przedpłaty przy anulacji mniej niż 7 dni przed przyjazdem; dla pakietów pobiera 30–50% przedpłaty. [Kompleks Beskid](https://wa-uploads.profitroom.com/kompleksbeskid/17719408896245_Regulamin_KB_25.pdf) dla rezerwacji standardowej podaje po tym terminie opłatę 30% wartości rezerwacji. [Airbnb](https://www.airbnb.com/help/article/3066) opisuje pełny, częściowy lub zerowy zwrot w zależności od oferty i terminu. To przykłady, nie reguła dla rivé; opłata liczona od ceny pobytu nie musi być równa wysokości już wpłaconej zaliczki. Warunki i ewentualne wyjątki pozostają do decyzji właściciela.

**Confirmed — właściciel, 2026-11-20.** Przy anulowaniu noclegu mniej niż siedem dni przed przyjazdem wpłacona zaliczka przepada. Nie ustalono dodatkowej opłaty ponad wpłatę ani wyjątków; sposób prezentacji i rozliczenia oraz kwalifikacja warunków wymagają doprecyzowania. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Jeśli gość nie anuluje noclegu i nie przyjedzie, zaliczka przepada. Moment uznania nieprzybycia oraz dalsza dostępność jednostki pozostają do ustalenia. Źródło: rozmowa z właścicielem.

**Proposed — właściciel, 2026-11-20.** Przy braku przyjazdu przetrzymać nocleg przez pierwszą dobę, powiadomić recepcję o nieobecności i umożliwić próbę kontaktu z gościem. **Open question:** dokładny czas powiadomienia i zwolnienia, decyzja recepcji oraz wpływ na pozostałe noce. Źródło: rozmowa z właścicielem; przebieg wymaga doprecyzowania.

**Confirmed — właściciel, 2026-11-20.** O zwolnieniu pozostałej rezerwacji po nieprzyjeździe decyduje recepcja; nie ma automatycznej decyzji ani automatycznego anulowania. Powiadomienie ma wspierać reakcję personelu. Dokładny moment powiadomienia i ręcznego zwolnienia pozostaje do ustalenia. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Jeśli gość noclegowy nie przybył, recepcja dostaje przypomnienie o godzinie 20:00 w dniu planowanego przyjazdu oraz kolejną informację następnego dnia. **Open question:** godzina i forma kolejnej informacji. Powiadomienia nie anulują rezerwacji. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-24.** Po pierwszym przypomnieniu recepcja próbuje skontaktować się z gościem. Jeśli gość potwierdzi, że nie przyjedzie, recepcja może od razu zwolnić pozostałe noce. Przy braku odpowiedzi może to zrobić następnego dnia po drugim przypomnieniu. Zwolnienie pozostałych nocy jest decyzją recepcji. Źródło: warsztat noclegów, wybór wariantu A.

**Confirmed — właściciel, 2026-11-24.** Przy nieprzyjeździe gościa z rezerwacją potwierdzoną telefonicznie bez zaliczki nie naliczamy dodatkowej opłaty. Recepcja stosuje ustaloną procedurę kontaktu i zwalniania pozostałych nocy. Źródło: warsztat noclegów, wybór wariantu A.

**Confirmed — właściciel, 2026-11-20.** Recepcja oznacza faktyczne zameldowanie gościa w systemie, odrębnie od rezerwacji. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Osobne meldowanie każdej osoby z jednej rezerwacji nie jest potrzebne. Nie przesądza to zasad indywidualnej obecności w ośrodku, które dotyczą odrębnego procesu. Źródło: rozmowa z właścicielem.

## Gotowość noclegu — 2026-11-20

**Confirmed — właściciel.** Recepcja potrzebuje w panelu statusu gotowości jednostki, np. gotowa do wydania lub wymagająca sprzątania. Szczegółowa lista i reguły są do decyzji.

**Research — 2026-11-20.** [OPERA Cloud](https://docs.oracle.com/en/industries/hospitality/opera-cloud/25.5/ocsuh/c_housekeeping_room_management.htm) podaje m.in. statusy czysty, brudny, opcjonalnie sprawdzony i wymagający odświeżenia oraz odrębne wyłączenia jednostek. To przykład jednego systemu, nie potwierdzona reguła rivé. [Audyt Cezara](audits/cezar/dashboard/functional-matrix.md) pokazuje widoki sprzątania, lecz nie potwierdza listy statusów gotowości ani jej powiązania z recepcją.

**Proposed.** Rozdzielić gotowość/sprzątanie, zajętość oraz blokadę z powodu usterki; ustalić potrzebne etapy i wpływ blokady na wydanie oraz przyszłą sprzedaż. Źródło: rozmowa z właścicielem i dokumentacja OPERA Cloud, 2026-11-20.

**Confirmed — właściciel, 2026-11-20.** Statusy sprzątania jednostki: wymaga sprzątania, sprzątanie w toku i czysty/gotowy po sprzątaniu. Status „w toku” jest opcjonalny; można przejść od wymagającego sprzątania bezpośrednio do czystego. Może przydać się przy późniejszej rozbudowie. Oddzielna blokada z powodu usterki i jej skutki pozostają propozycją do omówienia. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Recepcja może wyłączyć jednostkę z użycia na określony czas, np. z powodu usterki, niezależnie od stanu sprzątania. Wpływ na istniejące rezerwacje i zasady zwolnienia blokady pozostają do omówienia. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Przy wyłączeniu jednostki na termin istniejącej rezerwacji system pokazuje recepcji kolidującą rezerwację i umożliwia przeniesienie gościa, bez automatycznego anulowania. Szczegóły, gdy brak miejsca zastępczego, pozostają otwarte. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Jednostkę można wyłączyć także wtedy, gdy brak wolnego noclegu zastępczego. Istniejąca rezerwacja pozostaje do ręcznego rozwiązania przez recepcję, bez automatycznego anulowania. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-24.** Przy zakładaniu blokady jednostki recepcja wybiera tryb zakończenia. Blokada może wygasnąć automatycznie o wskazanej porze albo pozostać aktywna do ręcznego potwierdzenia jej zdjęcia. Źródło: warsztat sprzątania i usterek, wybór wariantu C.

**Confirmed — właściciel, 2026-11-20.** Po wymeldowaniu system automatycznie oznacza jednostkę jako wymagającą sprzątania. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-24.** Jednostki wymagające sprzątania trafiają na wspólną listę. System pokazuje wyżej jednostki z najbliższym przyjazdem, a pracownik sam wybiera następną jednostkę do sprzątania. Źródło: warsztat sprzątania, wybór wariantu A.

**Confirmed — właściciel, 2026-11-20.** Zarówno pracownik sprzątający, jak i recepcja mogą oznaczyć jednostkę noclegową jako czystą. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Próba zameldowania w jednostce wymagającej sprzątania wywołuje ostrzeżenie, lecz nie jest blokowana; decyzję podejmuje recepcja. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Standardowo rachunek rozlicza się przed wymeldowaniem. W wyjątku, np. gdy gość opuścił obiekt bez zapłaty, recepcja może po ostrzeżeniu wymeldować go mimo zaległości; rachunek pozostaje otwarty do dalszej obsługi. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Po wymeldowaniu nierozliczone rachunki są widoczne na osobnej liście należności dla recepcji, aby można było do nich wrócić. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Recepcja może w panelu przedłużyć pobyt, jeśli jednostka jest dostępna na dodatkowe noce. Zasady wyceny i zmiany jednostki doprecyzowano poniżej. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-20.** Dodatkowe noce przy przedłużeniu pobytu są wyceniane według aktualnego cennika dla tych dni. Właściciel wskazał sprzedaż dodatkową jako pożądany kierunek; konkretne propozycje i sposób ich prezentacji pozostają do ustalenia. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-21.** Jeśli obecna jednostka nie jest dostępna na dodatkowe noce, recepcja może zaproponować przeprowadzkę do innej wolnej jednostki w ramach tego samego pobytu i rachunku. Dodatkowe noce są wyceniane według aktualnego cennika. Źródło: rozmowa z właścicielem.

**Confirmed — właściciel, 2026-11-21.** Wcześniejsze zameldowanie i późniejsze wymeldowanie to płatne dodatki uzgadniane z recepcją według dostępności jednostki i czasu potrzebnego na sprzątanie. Źródło: rozmowa z właścicielem.

**Research — wcześniejszy wyjazd, 2026-11-21.** [Ośrodek Adam w Szczyrku](https://adam.szczyrk.pl/info/regulamin) i [Kompleks Beskid](https://wa-uploads.profitroom.com/kompleksbeskid/17719408896245_Regulamin_KB_25.pdf) przewidują brak zwrotu za niewykorzystany okres po rozpoczęciu pobytu, gdy rezygnuje gość. [Willa Szwajcaria w Wiśle](https://www.willaszwajcaria.pl/pokoje) również nie przewiduje zwrotu, ale w uzasadnionym przypadku pozwala wykorzystać kwotę w innym terminie. [Airbnb](https://www.airbnb.com/help/article/3066) stosuje warunki danej rezerwacji przy wyjeździe z przyczyn osobistych. Źródła: regulaminy obiektów i centrum pomocy Airbnb.

**Confirmed — właściciel, 2026-11-21.** Przy wcześniejszym wyjeździe z decyzji gościa domyślnie obowiązuje pełna cena zarezerwowanych nocy. Recepcja może w indywidualnym przypadku obniżyć należność. Po potwierdzonym wcześniejszym wyjeździe pozostałe noce od razu wracają do sprzedaży, niezależnie od rozliczenia rachunku. Dokładne uprawnienia do korekty i sposób jej rozliczenia pozostają otwarte. Źródło: rozmowa z właścicielem.

**Research — wyposażenie na życzenie, 2026-11-21.** [Mercure Szczyrk Resort](https://mercureszczyrk.pl/hotel-dla-dzieci-w-gorach) oferuje bezpłatne łóżeczka turystyczne i krzesełka do karmienia. [Gołębiewski w Wiśle](https://www.golebiewski.pl/wisla/jesien-first-minute) wymienia też wanienki. [Beskidzki Raj](https://www.beskidzkiraj.com/pakiety/kwotowy-500-zl) w warunkach ogólnej oferty pokoi przewiduje płatne łóżeczko w miarę dostępności. Przykłady nie ustalają zakresu oferty rivé.

**Confirmed — właściciel, 2026-11-21.** Na start rivé nie oferuje dodatków do wyposażenia takich jak łóżeczko turystyczne. Można rozszerzyć ofertę w przyszłości. Właściciel wskazał wybór układu łóżek (jedno king size albo dwa pojedyncze) jako osobny wariant noclegu. Wybór zostaje odłożony do czasu wymiany łóżek w obiekcie i jest poza początkowym zakresem implementacji. Sposób obsługi ustalimy po powrocie do tego tematu. Źródło: rozmowa z właścicielem.

**Research — funkcje wokół rezerwacji noclegu, 2026-11-21.** [Cloudbeds](https://myfrontdesk.cloudbeds.com/hc/en-us/articles/50076487181211-Booking-Engine-Settings-page-overview) pokazuje najniższą stawkę bazową dla poszczególnych dat w kalendarzu i pozwala prezentować dodatki przed lub po potwierdzeniu rezerwacji. [Booking.com](https://developers.booking.com/demand/docs/orders-api/order-preview-create) przewiduje informacje o przyjeździe i prośby specjalne tam, gdzie mają zastosowanie.

**Confirmed — właściciel, 2026-11-21.** Kalendarz pokazuje ceny „od” przed wyborem dat. Po wyborze gość widzi pełną cenę pobytu przed potwierdzeniem. W formularzu może podać orientacyjną godzinę przyjazdu widoczną dla recepcji. Brak godziny nie blokuje wysłania formularza. Jeśli gość jej nie poda, pole zostaje puste i nie wysyłamy próśb o uzupełnienie (doprecyzowanie właściciela, 2026-11-21). Po rezerwacji gość może dokupić śniadanie przez link do zarządzania rezerwacją. Jeśli nie wybrał go w formularzu, na ekranie potwierdzenia wpłaty zaliczki widzi ofertę śniadania z ceną i przyciskiem do dokupienia. Przycisk pozwala potwierdzić wybrane śniadania bez przechodzenia ponownie przez proces płatności. Śniadanie trafia na ten sam rachunek pobytu i jest rozliczane na miejscu, bez osobnej płatności online. Źródło: rozmowa z właścicielem.
