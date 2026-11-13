# Plan pracy agentów — od discovery do wdrożenia

**Status: propozycja kolejności i kryteriów odbioru.** Zakres pilota, dostawcy i stack czekają na decyzję właściciela. Plan obejmuje konfigurację kupionych produktów, integracje i ewentualny własny kod. W każdym wariancie obowiązują te same uzgodnione wyniki biznesowe.

Źródła pracy: [ustalenia właściciela](../discovery.md), [mapa 15 obszarów](capability-map.md), [słownik](business-glossary.md), [pytania](open-questions.md), [benchmark i próby demo](../research/hotel-spa-benchmark.md), [instrukcje agentów](../../AGENTS.md).

## 1. Najpierw proces i wybór pilota

| Etap | Praca | Warunek przejścia |
| --- | --- | --- |
| 1. Obserwacja | Jedna zmiana recepcji od rezerwacji lub wejścia do rozliczenia i raportu. Zapisz role, narzędzia, przełączenia, awarie, ręczne obejścia, częstotliwość i koszt błędów. Uzupełnij spis systemów, urządzeń, umów i eksportów. | Właściciel potwierdza przebieg i najważniejsze tarcie. Oddziel stan obecny, przyszłe wymagania i hipotezy. |
| 2. Reguły pilota | Wybierz jeden przebieg z miernikiem. Rozpisz oczekiwane wyniki na przykładach solo, grupa i gość dzienny oraz warianty, które wymagają dalszej decyzji. Dla innych obszarów wystarczą zależności i pytania. | Karta pilota określa zakres, role, przykłady i wyjątki, które trzeba obsłużyć przed użyciem. Każdy nierozstrzygnięty przypadek ma właściciela i określony wpływ na pilot. |
| 3. Demo i koszt | Wykonaj scenariusze potrzebne do decyzji, sprawdź eksport, licencje i API. Porównaj zakup lokalny, zagraniczny, hybrydę i własny rdzeń z kosztem 3–5 lat oraz kosztem wyjścia. | Dowód z demo lub sandboxa dla funkcji krytycznych. Właściciel zatwierdza sposób dostawy, źródła danych i zakres pierwszej wersji. |
| 4. Projekt jednego wycinka | Rozrysuj stany, operacje i wyjątki, minimalny przepływ danych, role, obsługę awarii i strategię testów. Wybierz technologię adekwatną do zatwierdzonego zakresu. | Zatwierdzona specyfikacja wycinka z oczekiwanymi wynikami, uzgodnioną odpowiedzialnością za dane, sposobem testowania i wycofania. Istotne decyzje mają wpis w [rejestrze decyzji](../decisions/README.md). |
| 5. Realizacja i próba | Najpierw konfiguracja lub mały działający przebieg na danych syntetycznych. Następnie integracje, próba migracji, awarii i odtworzenia. | Odbiór wyników przez właściciela i odpowiednie osoby z operacji oraz księgowości. Przed produkcją uzgodnione wsparcie, procedura awarii, sposób wycofania i decyzja o starcie. |

**Kandydat do omówienia:** wspólny rachunek od rezerwacji lub wejścia do zamknięcia. Pokrywa recepcję, POS, płatności i podstawowy raport. Wejścia czasowe warto dodać do pilota po potwierdzeniu realnej reguły i znaczenia operacyjnego. Publiczna strona i kontakt mogą być osobnym wycinkiem po uzgodnieniu zakresu treści i punktu przekazania do rezerwacji. Dwa przebiegi i syntetyczny przykład rachunku grupy są w [notatce warsztatu recepcji](reception-discovery.md).

## 2. Pakiety pracy według obszaru

Zadanie otrzymuje agent z odpowiednim zakresem decyzji i testów. W discovery można pracować równolegle nad wywiadem i scenariuszami, analizą dostawców oraz danymi i zgodnością. Wspólne reguły rachunku, dostępności i tożsamości uzgadnia jeden prowadzący przed rozdzieleniem zmian implementacyjnych.

| Obszar | Co przygotować i od czego zależy realizacja | Przykład odbioru po zatwierdzeniu |
| --- | --- | --- |
| Website i CMS | Z D-03 opisz treści, role, podgląd i publikację, dostępność i ścieżkę kontaktu. Uzgodnij wejście do booking engine i zachowanie przy jego niedostępności. | Redaktor publikuje ofertę bez zmiany taryfy. Kontakt dociera do odbiorcy, a mobilna i klawiaturowa ścieżka do rezerwacji działa. |
| Katalog i ceny | Z D-03 zbierz przykłady taryf i ich pierwszeństwa, model wariantów, opłat i limitów. Uzgodnij źródło cen i sposób zachowania zaakceptowanej oferty. | Ta sama oferta wyceniana zgodnie z przykładami. Zmiana taryfy po potwierdzeniu wywołuje wyłącznie uzgodnione zmiany. |
| Rezerwacje | Ustal jednostkę lub pulę, moment blokady, wygaśnięcie, modyfikację, no-show i anulowanie. Zależy od taryf, blokad obiektu i właściciela dostępności. | Dwie próby ostatniego miejsca mają uzgodniony wynik. Anulowanie zwalnia właściwy zasób, a opóźnienie OTA tworzy widoczną sprawę do uzgodnienia. |
| SPA, eventy, pakiety, vouchery | Z D-04 wybierz jeden typ oferty. Zmierz wejścia i taryfy. Sprawdź sprzęt, pojemność, personel, gabinety i zależności składowych. | Zgodna kwota na granicy czasu, brak podwójnego zajęcia zasobu. Niepełny pakiet i ponowienie realizacji vouchera mają ustalone wyniki. |
| Klienci i komunikacja | Z D-05 ustal potrzebne relacje i minimum danych. Zweryfikuj źródło kontaktu, ręczną obsługę kolizji i zdarzenia powiadomień. | Dwie osoby o tym samym nazwisku pozostają rozróżnione. Komunikat trafia do właściwej osoby i ma widoczny wynik dostawy. |
| Recepcja i folio | Z D-02 i D-08 rozpisz rachunek od rezerwacji i od przyjazdu, zmianę alokacji w grupie, saldo i zamknięcie. Ustal zakres walk-in i korekt. | Rachunek zachowuje ciągłość od zaliczki do końca. Alokacja zmienia podział bez zmiany sumy. Konflikt dopisania i zamknięcia ma jawny wynik. |
| Gastronomia i POS | Wybierz jedną grupę produktów i jeden punkt sprzedaży. Ustal oznaczenie zakupu opłaconego lokalnie i obciążenia folio. | Zakup trafia na właściwy rachunek albo rozlicza się na miejscu według reguły. Powtórzony komunikat POS nie dubluje pozycji. |
| Personel | Z D-06 uzgodnij samoobsługę czasu, grafik, nieobecności, korekty i oddzielną kalkulację wewnętrzną. Ustal integrację kalendarza zabiegów. | Zmiana przez północ ma poprawny zapis. Nieobecność ujawnia dotknięte wizyty. Tylko uprawniona osoba widzi płace i koryguje wpisy. |
| Obiekt | Z D-07 ustal statusy gotowości i usterki, odpowiedzialność i relację z kalendarzem. | Sprzątanie wpływa na wydanie pokoju zgodnie z regułą, a blokada techniczna na właściwe zasoby i kanały sprzedaży. |
| Płatności i fiskalizacja | Z D-08 uzgodnij cykle wpłaty, rozrachunku i dokumentu. Potwierdź księgowanie zaliczek, zwroty, urządzenia oraz ślad korekt. | Wpłaty dzielone, utrata odpowiedzi operatora i korekta mają zgodne saldo i odrębne statusy. Raport uzgadnia się z operatorem i dokumentami. |
| Finanse | Z D-09 zdefiniuj okres, podstawę, kategorie i uzgodnienie. Dopiero potem rozważ koszty, marże, budżety i KPI. | Jedna sprzedaż jest liczona raz. Zaliczki, zwroty, koszty i alokacje mają uzgodnione traktowanie i dają się prześledzić do źródła. |
| Role i dostęp | Z D-10 przygotuj macierz ról, operacji i zakresu danych oraz ślad działań na rachunkach i płacach. | Ta sama reguła obowiązuje w UI, API i eksportach. Odmowy i ważne zmiany mają czytelny ślad bez poufnych danych w logach. |
| Integracje i dystrybucja | Z D-11 sprawdź dla każdego zapisu właściciela, wersję API, komercyjny dostęp, zdarzenia, limity i uzgodnienie. Zacznij od jednej integracji. | Powtórzenie, opóźnienie i awaria są odtwarzalne. Zaległość jest widoczna i daje się bezpiecznie uzgodnić. |
| Dane i migracja | Z D-12 przygotuj próbę eksportu, mapowania identyfikatorów, zakresu historii, retencji i migracji. | Liczby rezerwacji, salda, vouchery i korekty uzgadniają się. Raport rozbieżności i wycofanie zostały przećwiczone. |
| Inżynieria i operacje | Z D-13 uzgodnij środowiska, dostęp, obserwację, kopie, procedurę ręczną oraz tolerancję przerwy i utraty danych. | Próba awarii pokazuje co zrobić, kto podejmuje decyzję i jak odzyskać spójny stan. Odtworzenie zmierzono wobec uzgodnionego celu. |

## 3. Jak przygotować zadanie implementacyjne

Zamknij poniższe granice w specyfikacji pilota. Dla każdego wiersza zapisz wybrany system wiodący, to kto może inicjować zmianę i dowód, po którym uznajemy operację za wykonaną. Zmiana źródła wymaga ponownego uzgodnienia zależnych przebiegów.

| Fakt | Granica odpowiedzialności do wyboru |
| --- | --- |
| Cena i dostępność | Katalog publikuje ofertę. System rezerwacji rozstrzyga o cenie potwierdzonej gościowi i zajęciu zasobu. Ustal wpływ OTA, blokad technicznych, grafiku i SPA. |
| Klient i pobyt | Wybierz identyfikator źródłowy oraz regułę powiązania wielu identyfikatorów. Ustal właściciela relacji rezerwacji, uczestników i płatnika. |
| Pozycja i saldo rachunku | Wybierz jeden system, który przyjmuje lub odrzuca zapis pozycji, alokacji i zamknięcia. POS, SPA i recepcja muszą dostać potwierdzenie albo widoczny wyjątek. |
| Wpłata i dokument | Ustal osobno źródło statusu zapłaty, potwierdzenia rozrachunku oraz wystawienia lub przyjęcia dokumentu. Połącz ślady operacji do uzgodnienia. |
| Grafik i czas pracy | Wyznacz źródło obsady, źródło rzeczywistych wpisów i odbiorcę eksportu. Zaplanuj wpływ zmian grafiku na potwierdzone usługi. |
| Raport | Zapisz odczytywane źródła, moment aktualizacji i to, jak raport pokazuje braki lub rozbieżności w danych. |

Każdy wycinek ma identyfikatory z mapy, właściciela, linki do decyzji, punkt wejścia użytkownika, zakres i zależności. Specyfikacja zawiera tabelę kroków z danymi syntetycznymi i oczekiwanym wynikiem, role i ograniczenia danych, warunki ponowienia, zakres testów oraz sposób pomiaru i wycofania. Agent zgłasza rozbieżności między źródłami przed zakodowaniem reguły.

1. **Ustal źródła danych.** Dla dostępności, ceny, folio, wpłaty, dokumentu, czasu pracy i uprawnień zapisz system wiodący, dozwolony zapis i sposób porównania z pozostałymi. Dla mapowania identyfikatorów przewidź ręczne rozstrzygnięcie wątpliwych dopasowań.
2. **Wyznacz granicę własnego kodu.** Przy zakupie sprawdź konfigurację, eksport i procedury. W hybrydzie adapter odwzorowuje zatwierdzone operacje, a kokpit pokazuje także status niepewny i rozbieżności. W wariancie własnym reguły biznesowe powinny dać się przetestować niezależnie od interfejsu i dostawców. Wybór sposobu organizacji kodu i wdrożenia zależy od tych granic.
3. **Zapisz niezmienniki.** Rozdziel pozycję, alokację, wpłatę i dokument. Zaakceptowana alokacja zachowuje sumę pozycji. Zapis kwoty ma jednoznaczną walutę, jednostkę i regułę zaokrąglenia. Potwierdzenie zasobu respektuje dostępność. Ponowienie operacji rozpoznaje ten sam zamiar. Zmiana stanu ma uzgodnionego autora i ślad.
4. **Sprawdź ryzyka odpowiednimi testami.** Reguły kwot i czasu sprawdź na przykładach granicznych. Integracje sprawdź w sandboxie na opóźnieniu i powtórzeniu, rezerwacje na równoległym zapisie, a uprawnienia także przez bezpośrednie wywołanie. Zrób próbę całego przebiegu przez normalny interfejs oraz ręczne uzgodnienie po awarii.
5. **Oddaj dowód.** Pokaż wynik krok po kroku, wynik testów, odkryte ograniczenia, stan decyzji i sposób cofnięcia. Zapisz zakres środowiska, w którym dowód uzyskano.
