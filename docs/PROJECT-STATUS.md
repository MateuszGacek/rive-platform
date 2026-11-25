# rivé — punkt wznowienia

**Aktualizacja 2026-11-25. Aktywna faza 2 · Business & Domain Discovery.** Właściciel zatwierdził zapisanie [nadrzędnej roadmapy](PROJECT-ROADMAP.md) i pozostanie przy projektowaniu całej platformy. Fazy 0–1 mają materiały do przeglądu. Zakres pierwszej dostawy oraz przejście do architektury i developmentu wymagają osobnych decyzji.

## Co mamy

- [Wizję jednego obiektu](product/vision.md), [mapę 15 obszarów](product/capability-map.md), [Canvas produktu](maps/rive-product-map.canvas), [szkic design systemu](design/design-system.md) i [Project Brain](README.md#project-brain).
- [Skonsolidowany audyt Cezara](audits/cezar/consolidation/evidence-index.md) jako materiał porównawczy. Uzupełniające źródła historyczne są opisane w [Issue #4](https://github.com/MateuszGacek/rive-platform/issues/4).
- [Day SPA i wspólny rachunek](product/reception-discovery.md) oraz [noclegi](discovery.md#wywiad-z-właścicielem--oferta-noclegowa-2026-11-19) mają szczegółowe ustalenia. W [mapie i pytaniach](product/open-questions.md) są również decyzje o gastronomii, sprzątaniu, personelu, masażach, voucherach, wydarzeniach, Booking.com oraz ewentualnej migracji.

## Decyzje wpływające na następny krok

- Na starcie Day SPA strona pokazuje dostępność, recepcja przyjmuje rezerwację telefonicznie, a akcja w panelu to „Wejście”. Samoobsługa WWW to odłożony wariant. [Reguły recepcji](product/reception-discovery.md#potwierdzenie-rezerwacji-przez-www)
- Sprzedaż przez WWW i rentowność gałęzi działalności to wcześniej wskazane priorytety. Ich zakres w pierwszej dostawie pozostaje do ustalenia. [Sprzedaż WWW](https://github.com/MateuszGacek/rive-platform/issues/10) · [Finanse](https://github.com/MateuszGacek/rive-platform/issues/11)
- Otwarte decyzje przekrojowe dotyczą właścicieli danych o cenie, dostępności, rachunku i wpłacie, definicji finansowych, dokumentów i zwrotów oraz zakresu uprawnień. Podział aplikacji i stack są przedmiotem późniejszej decyzji. [D-03](product/open-questions.md#d-03) · [D-08–D-13](product/open-questions.md#d-08)

## Wznowienie

**Confirmed — zakres sesji, właściciel, 2026-11-25.** W fazie 2 właściciel dopuścił równoległe badanie oraz szkice propozycji dla następnych faz. Ta zgoda obejmowała badanie, recenzję i lokalną konsolidację. Obowiązuje osobna akceptacja przed publikacją, przejściem fazy, wyborem rozwiązania, POC lub developmentem.

Prześledzono nocleg od WWW do rachunku i raportu oraz dziewięć powiązanych przebiegów. [Mapa przepływów i pokrycie 15 obszarów](research/platform-workflows.md) · [Kolejność decyzji właściciela](product/open-questions.md#kolejność-decyzji-właściciela--proposed-2026-11-25)

**Confirmed — druga sesja, 2026-11-25.** Właściciel przyjął wynik pierwszej sesji jako badanie i propozycje. Udzielił zgody na pogłębienie analizy w fazie 2. Kolejne rekomendacje również pozostają do decyzji.

**Punkt wznowienia.** Otworzyć [przykład finansowy XI–I](research/platform-workflows.md#od-zaliczki-do-wyniku-gałęzi) oraz [kolejkę decyzji](product/open-questions.md#kolejność-decyzji-właściciela--proposed-2026-11-25). Pierwszy wybór: czy obniżkę ceny grudniowej usługi uznaną w styczniu pokazać w wyniku stycznia z odniesieniem do grudnia, czy przeliczać również grudzień? Data rzeczywistej wypłaty pozostaje osobną informacją. Po odpowiedzi sprawdzić pakiety i przypisanie kosztów.

**Ocena bramki fazy 2.** **Faza 2 jest gotowa do przeglądu z właścicielem. Jej zamknięcie wymaga rozstrzygnięć.** Przejrzano 15/15 obszarów w [macierzy ośmiu wymiarów](product/capability-map.md#macierz-kompletności-discovery). Są rozwinięte reguły noclegów i Day SPA, rachunków, czasu pracy i sprzątania. Rozwinięto [cykle życia i granice odpowiedzialności](product/business-glossary.md#model-pojęciowy-i-cykle-życia). Do zamknięcia fazy nadal potrzebne są decyzje właściciela dotyczące definicji wyniku, ceny w toku zakupu, uprawnień przy korekcie i wspólnym rachunku, zakresu gwarancji pakietowych oraz działania przy awarii. Właściciel rozstrzyga lub świadomie odkłada te elementy z określeniem skutku i zatwierdza scenariusze przekrojowe. Szczegółowe SLA dostawcy, implementacyjne testy wydajności, końcowa biblioteka UI i wybór bazy mogą poczekać do właściwych faz.

**Niezależne review drugiej sesji.** Skorygowano zakres ręcznego potwierdzenia karty, uprawnienia gastronomii, założenia kosztowe marży pokrycia i odróżnienie rozrachunku operatora od wpłaty gościa. Test kalendarza obejmuje komunikaty dla czytnika ekranu. Porównanie wariantów ocenia granicę zapisu niezależnie od liczby wdrożeń. Właściciel zaakceptował publikację materiału przygotowawczego z obu sesji. Decyzje biznesowe i architektoniczne wymagają osobnego potwierdzenia.

**Proposed — materiały dalszych faz.** Fazy 3–5: [warianty aplikacji, model domenowy i właściciele danych](product/mvp-architecture.md). Faza 6: [interfejs i komponenty](design/design-system.md), [SEO i sprzedaż](research/direct-sales.md). Fazy 7 i 11: [ryzyka i odzyskiwanie](research/quality-and-recovery.md). Faza 8: [praca wielu agentów](product/agent-delivery-plan.md). Dla fazy 9 zapisano zależności i przykłady przyszłego odbioru. Faza 10 wymaga odrębnej zgody. Wcześniejsze materiały faz 0–1 pozostają podstawą.

**Weryfikacja, 2026-11-25.** Niezależni recenzenci sprawdzili procesy i dane, interfejs i sprzedaż oraz architekturę, jakość i utrzymanie. Uwzględniono ręczne ustalanie terminu masażu, dostęp danych dla gastronomii, rozróżnienie konfliktu OTA od wyjątku Day SPA i zabezpieczenie przed dwoma aktywnymi środowiskami po odtworzeniu. Nadal brak potwierdzenia komercyjnego dostępu OTA, oferty kosztowej, pomiarów ruchu, uzgodnionych definicji finansowych oraz prób integracji i odzyskiwania.

**Confirmed — sposób dalszej pracy.** Po dwóch sesjach badawczych właściciel i agent przechodzą do wspólnych decyzji według kolejki fazy 2. Agent przedstawia rekomendację, alternatywy i konsekwencje dla jednej decyzji naraz. Zatwierdzone odpowiedzi trafiają do właściwej karty discovery i punktu wznowienia. Otwarte pytanie nie zatrzymuje niezależnych obszarów.

[Issue #5](https://github.com/MateuszGacek/rive-platform/issues/5) śledzi D-01 i zakres pierwszej dostawy w fazie 9. [Issue #9](https://github.com/MateuszGacek/rive-platform/issues/9) śledzi warunki zakończenia fazy 2 i decyzję o otwarciu fazy 3.
