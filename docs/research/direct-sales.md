---
type: research
status: proposed
area: "01 Website i CMS"
source: "Strony obiektów, audyt publicznej strony Cezara, Google Search Central i web.dev"
created: 2026-11-25
updated: 2026-11-25
---

# Sprzedaż bezpośrednia, treści i pomiar

**Confirmed — zaobserwowane, 2026-11-25.** Hotel Klimczok prowadzi osobną stronę Day SPA. Aries Szczyrk przedstawia ofertę dla gości z zewnątrz i vouchery. Mercure Szczyrk przedstawia czas i skład ofert SPA. To przykłady komunikacji w regionie. Wielkość popytu i skuteczność tych stron pozostają nieznane. **Proposed.** Wyróżnik komunikacyjny rivé do sprawdzenia: gość widzi co zawiera pobyt, ile zapłaci i jak najprościej zarezerwować daną usługę. [Klimczok](https://www.klimczok.pl/day-spa-szczyrk) · [Aries](https://www.ariesszczyrk.pl/spa-wellness) · [Mercure](https://mercureszczyrk.pl/spa-szczyrk)

| Hipoteza intencji | Docelowa treść i czynność | Sposób sprawdzenia |
| --- | --- | --- |
| „nocleg ze SPA” + rzeczywista lokalizacja | /noclegi i karta typu, wyposażenie, dostęp do ośrodka wg pakietu, pełna cena po wyborze dat. Rezerwacja w kontekście wybranego typu. | Zapytania i kliknięcia w Search Console, przejścia od karty do potwierdzonych noclegów. |
| „day spa”, „sauna”, „4 godziny SPA” + okolica | /day-spa z godzinami dla dnia, zasadami i telefonem. Osobna karta pakietu tylko przy rzeczywiście odrębnej ofercie. | Wejście na stronę i kliknięcie telefonu mierzyć osobno od faktycznego zapisu przez recepcję. |
| „voucher na masaż”, „voucher SPA” | /vouchery z warunkami realizacji, kanałem umówienia i rozróżnieniem kwoty oraz usługi. | Potwierdzony zakup i późniejsza realizacja to osobne zdarzenia. |
| „retreat”, wydarzenie lub pakiet sezonowy | Publikować aktualną kartę z zakresem, terminem i informacją o miejscach. Przy braku terminu zaproponować kolejną dostępną ofertę albo kontakt. | Zapytania o konkretną ofertę, sprzedaż biletów i odwołania. Uzasadnić osobną kampanię dostępną pulą. |

**Proposed — SEO i CMS.** Jedna stabilna ścieżka dla oferty, unikalny tytuł, opis, H1, tekst cen, odpowiednie opisy zdjęć. Uwzględniać w sitemap opublikowane kanoniczne strony. Po zmianie adresu przekierować starą ścieżkę do właściwego odpowiednika. Nie indeksować podglądów, koszyków i parametrów wyszukiwania; dane rezerwacji chronić autoryzacją. Oznaczenia strukturalne Hotel/LocalBusiness i Event stosować dla zgodnych, widocznych danych. Weryfikować adres, telefon i godziny w profilu obiektu oraz na stronie. Dla zatwierdzonych tłumaczeń osobne URL i wzajemne hreflang. Brak danych uzasadniających dziś konkretny drugi język. [Search Central](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) · [Dane lokalne](https://developers.google.com/search/docs/appearance/structured-data/local-business) · [Wersje językowe](https://developers.google.com/search/docs/specialty/international/localized-versions)

**Proposed — wydajność.** Treść oferty powinna być dostępna w początkowym HTML, ze zdjęciami o dobranym rozmiarze i miejscu zarezerwowanym w układzie. Bieżąca dostępność i potwierdzenie ceny wymagają źródła transakcyjnego. Dla publicznych szablonów porównywać wyniki laboratoryjne przed wydaniem z późniejszymi danymi użytkowników. Punkty odniesienia dla 75. percentyla: LCP ≤ 2,5 s, INP ≤ 200 ms, CLS ≤ 0,1. Przy małym ruchu oznaczyć brak próby terenowej. [Core Web Vitals](https://web.dev/articles/vitals)

**Proposed — konwersja i powroty.** Dla gości rozpoczynających na karcie noclegu zestawić zbiorczo wybór typu → sprawdzenie dat → formularz przyjęty → rezerwacja potwierdzona po wpłacie. Wejścia od dat oraz powroty przez link zarządzania mają własny początek. Anulowanie lub zwrot śledzić oddzielnie. Porzucenie rozpatrywać według etapu i błędu, np. brak miejsca dla typu lub niedostępny operator. Odświeżenie potwierdzenia nie tworzy kolejnego zakupu. Gdy gość kończy sprawę telefonicznie, raport może pokazać nieznane źródło. Dla SPA kliknięcie telefonu nie oznacza nawet odebranej rozmowy. Pomiar nie wymaga dopisywania danych przy każdym wejściu. Do już uzgodnionego zakupu śniadania po zaliczce można porównać warunkową prezentację kolejnej oferty dla obdarowanego lub gościa powracającego. Potwierdzenia transakcyjne i zaproszenia marketingowe wymagają odrębnych reguł.

**Open question.** Właściciel wskazuje ofertę i odbiorców pierwszej kampanii oraz osobę utrzymującą aktualność treści. Dla profilowania lub kampanii specjalista potwierdza cel, podstawę, wymagane zgody kanałowe, sposób wycofania i retencję. Wariant oszczędny to zbiorcze zdarzenia bez nagrań sesji i CRM marketingowego. Zewnętrzne narzędzie dopiero po ocenie potrzeb, prywatności i kosztu. Audyt Cezara wykazał pobieranie mapy przed interakcją gościa. Dla rivé porównać tekstowy dojazd i link do mapy z osadzeniem uruchamianym po świadomej akcji, po ocenie zewnętrznych żądań i zgód. Dane kontaktowe, linki do zarządzania i swobodny tekst nie trafiają do analityki. [Notatka Project Brain o lejku](../ideas/posthog.md) · [Dane zabronione w Google Analytics](https://support.google.com/analytics/answer/6366371)
