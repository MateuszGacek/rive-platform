# Ścieżki użytkownika

**OBSERVED — 2026-11-19.** Przejścia sprawdzono w Chrome DevTools MCP do granicy wysłania formularza, rezerwacji lub płatności. „Zakończenie” poniżej oznacza ostatni zaobserwowany krok, nie finalizację transakcji.

| Cel | Sprawdzona ścieżka | Zakończenie i ograniczenie |
| --- | --- | --- |
| Oferta z głównej | [Start](https://sauna-cezar.pl/) → menu „Poznaj nas” → [sauna](https://sauna-cezar.pl/sauna), [basen](https://sauna-cezar.pl/basen), [masaż](https://sauna-cezar.pl/masaze) | Opisy usług są dostępne; nagłówek kieruje do rezerwacji telefonicznej. Nie znaleziono ścieżki zakupu wejścia online. |
| Oferta → kontakt | Dowolna strona oferty → menu „Info&Kontakt” → [Kontakt](https://sauna-cezar.pl/kontakt) | Formularz ma imię i nazwisko, e-mail i treść. Zatrzymano przed wysłaniem. |
| Nocleg → rezerwacja | [Start](https://sauna-cezar.pl/) lub menu „Nocleg” → [opis jednostki](https://sauna-cezar.pl/studio) → powrót do menu/CTA „Kalendarz wolnych pokoi” → [panel HTTPS](https://panel.sauna-cezar.pl/rezerwacja-zewnetrzna) | Panel pokazuje daty, liczbę osób i kalendarz. Nie wywołano wyszukiwania ani rezerwacji. Link źródłowy używa HTTP, a linki panelu do opisów jednostek wskazują stare adresy. |
| Informacja o ośrodku → wejście | [Sauna](https://sauna-cezar.pl/sauna) → [cennik](https://sauna-cezar.pl/cennik) → kontakt telefoniczny w nagłówku | Widać taryfy godzinowe w grafice. Brak zaobserwowanego koszyka lub formularza kupna wejścia. |
| Promocja → rezerwacja | [Promocje](https://sauna-cezar.pl/pakiety) → [„Pierwszy raz za darmo”](https://sauna-cezar.pl/node/121) → [formularz promocji](https://sauna-cezar.pl/pierwszy-raz-za-darmo) | Formularz wymaga danych kontaktowych, wyboru newslettera i oferuje hasło do konta. Zatrzymano przed „Submit”. |
| Wydarzenie → udział | [Wydarzenia](https://sauna-cezar.pl/wydarzenia) → [Andrzejki](https://sauna-cezar.pl/node/129) lub [Sylwester](https://sauna-cezar.pl/node/130) | Opisy kierują do rezerwacji telefonicznej. Wpis 2027 ma pusty widok szczegółowy. |
| Mobile → główne CTA | Start przy 390 px → przycisk menu → „Nocleg” → „Zarezerwuj nocleg”; osobno przewinięcie do karty „ZAREZERWUJ NOCLEG” | Obie drogi ujawniają link do panelu. Menu rozwija się po dotknięciu, lecz przycisk ma nieczytelną nazwę dostępną dla czytnika ekranu. |

**INFERRED.** Punkt przerwania najważniejszych ścieżek to przejście z treści marketingowej do oddzielnego panelu lub do telefonu. Dla pokoju użytkownik musi odszukać wspólny CTA, ponieważ strona szczegółowa nie prowadzi bezpośrednio do rezerwacji tego typu.

**PROPOSED.** Dla rivé projektować osobno ścieżkę noclegu, wejścia czasowego oraz pakietu nocleg + dostęp. Moment blokady dostępności, zaliczki i potwierdzenia pozostaje zgodny z [potwierdzonymi ustaleniami](../../../discovery.md#wywiad-z-właścicielem--oferta-noclegowa-2026-11-19) i otwartymi pytaniami [D-03/D-04](../../../product/open-questions.md#d-03).
