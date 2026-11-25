# Plan pracy agentów — od discovery do wdrożenia

**Status — 2026-11-25.** Ten dokument opisuje pracę w ramach [nadrzędnej roadmapy](../PROJECT-ROADMAP.md). Aktualną fazę i następny krok wskazuje [punkt wznowienia](../PROJECT-STATUS.md). Makietę, obserwację lub demo dobieramy do konkretnego pytania.

Źródła pracy: [ustalenia właściciela](../discovery.md), [mapa 15 obszarów](capability-map.md), [słownik](business-glossary.md), [pytania](open-questions.md), [benchmark i próby demo](../research/hotel-spa-benchmark.md), [instrukcje agentów](../../AGENTS.md).

## 1. Praca w ramach roadmapy

W discovery ustal reguły i zależności całej platformy. Architekturę produktu i technologię uzgadniamy w odpowiednich fazach roadmapy. Kolejność budowy i zakres pierwszej dostawy wybieramy w fazie 9. Do przygotowania zadania implementacyjnego użyj sekcji 3 po osobnej zgodzie właściciela na development.

**Przebieg do porównań.** 2026-11-24 właściciel wybrał pełną zwykłą wizytę Day SPA od rezerwacji telefonicznej lub wejścia do zapłaty jako pierwszy kandydat do próby. Rezerwowanie przedziałów jest nową funkcją. Po korekcie kierunku 2026-11-25 przebieg pozostaje [scenariuszem domenowym](reception-discovery.md#próby-przed-specyfikacją) z kryterium prostej obsługi. Przykład wspólnego rachunku z POS i podstawowym raportem pozostaje w [warsztacie rachunku grupowego](reception-discovery.md#pobyt-grupowy-z-zaliczką). O zakresie dostawy rozstrzygnie roadmapa wydań.

**Materiał do oceny.** [Warianty architektury](mvp-architecture.md) z wcześniejszej rozmowy oraz [scenariusze demo](../research/hotel-spa-benchmark.md) można wykorzystać, gdy odpowiadają na pytanie z aktywnej fazy. Przed obsługą rzeczywistych wpłat uzgodnij dokumenty, korekty i zwroty w [D-08](open-questions.md#d-08).

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

Uzgodnij poniższe granice na poziomie platformy w fazach 3–5, a potem odwołaj się do nich w specyfikacji wycinka. Dla każdego obszaru zapisz system wiodący, uprawnienia do zmiany i dowód wykonania operacji. Zmiana źródła wymaga ponownego uzgodnienia zależnych przebiegów.

| Fakt | Granica odpowiedzialności do wyboru |
| --- | --- |
| Cena i dostępność | Proposed: katalog może prowadzić taryfy, a rezerwacja zachować warunki potwierdzone gościowi. Porównaj z taryfą i potwierdzeniem prowadzonymi przez PMS. Ustal wpływ OTA, blokad technicznych, grafiku i SPA. |
| Klient i pobyt | Wybierz identyfikator źródłowy oraz regułę powiązania wielu identyfikatorów. Ustal właściciela relacji rezerwacji, uczestników i płatnika. |
| Pozycja i saldo rachunku | Wybierz jeden system, który przyjmuje lub odrzuca zapis pozycji, alokacji i zamknięcia. POS, SPA i recepcja muszą dostać potwierdzenie albo widoczny wyjątek. |
| Wpłata i dokument | Ustal osobno źródło statusu zapłaty, potwierdzenia rozrachunku oraz wystawienia lub przyjęcia dokumentu. Połącz ślady operacji do uzgodnienia. |
| Grafik i czas pracy | Wyznacz źródło obsady, źródło rzeczywistych wpisów i odbiorcę eksportu. Zaplanuj wpływ zmian grafiku na potwierdzone usługi. |
| Raport | Zapisz odczytywane źródła, moment aktualizacji i to, jak raport pokazuje braki lub rozbieżności w danych. |

Każdy wycinek ma identyfikatory z mapy, właściciela, linki do decyzji, punkt wejścia użytkownika, zakres i zależności. Specyfikacja zawiera tabelę kroków z danymi syntetycznymi i oczekiwanym wynikiem, role i ograniczenia danych, warunki ponowienia, zakres testów oraz sposób pomiaru i wycofania. Agent zgłasza rozbieżności między źródłami przed zakodowaniem reguły.

1. **Ustal źródła danych.** Dla dostępności, ceny, folio, wpłaty, dokumentu, czasu pracy i uprawnień zapisz system wiodący, dozwolony zapis i sposób porównania z pozostałymi. Dla mapowania identyfikatorów przewidź ręczne rozstrzygnięcie wątpliwych dopasowań.
2. **Wyznacz granicę własnego kodu.** Przy zakupie sprawdź konfigurację, eksport i procedury. W hybrydzie adapter odwzorowuje zatwierdzone operacje, a kokpit pokazuje także status niepewny i rozbieżności. W wariancie własnym reguły biznesowe powinny dać się przetestować niezależnie od interfejsu i dostawców. Wybór sposobu organizacji kodu i wdrożenia zależy od tych granic.
3. **Zapisz niezmienniki.** Rozdziel pozycję, alokację, wpłatę i dokument. Zaakceptowana alokacja zachowuje sumę pozycji. Zapis kwoty ma jednoznaczną walutę, jednostkę i regułę zaokrąglenia. Fizyczne przydziały jednostki są rozłączne. Recepcja może przyjąć wyjątek Day SPA po ostrzeżeniu, a konflikt z OTA zachowuje oba zobowiązania do rozwiązania. Ponowienie operacji rozpoznaje ten sam zamiar. Zmiana stanu ma uzgodnionego autora i ślad.
4. **Sprawdź ryzyka odpowiednimi testami.** Reguły kwot i czasu sprawdź na przykładach granicznych. Integracje sprawdź w sandboxie na opóźnieniu i powtórzeniu, rezerwacje na równoległym zapisie, a uprawnienia także przez bezpośrednie wywołanie. Zrób próbę całego przebiegu przez normalny interfejs oraz ręczne uzgodnienie po awarii.
5. **Oddaj dowód.** Pokaż wynik krok po kroku, wynik testów, odkryte ograniczenia, stan decyzji i sposób cofnięcia. Zapisz zakres środowiska, w którym dowód uzyskano.

## Faza 8 · propozycja pracy wielu agentów, 2026-11-25

**Proposed.** Po zatwierdzeniu developmentu prowadzący bierze jeden wynik biznesowy z Issue, czyta punkt wznowienia, reguły i odpowiednie ADR. W specyfikacji wskazuje identyfikatory kart, granicę zapisu, syntetyczny przykład sukcesu i wyjątku, wpływ na uprawnienia/dane, kontrakt, zakres plików i sposób odbioru. Przy niejasnej regule biznesowej zapisuje pytanie D-xx. Pozostałe niezależne zadania mogą być kontynuowane.

| Moment | Odpowiedzialność i dowód |
| --- | --- |
| Gotowość do pracy (Definition of Ready) | Właściciel zatwierdził fazę, zakres i kryteria. Znany właściciel wspólnych danych, spodziewany wynik konfliktu, wymagany kontrakt i odbiorcy. Przykład: zmiana przydziału zachowuje cenę. Dwa zespoły nie mogą równolegle definiować tej reguły. |
| Rozdział | Prowadzący przypisuje jeden zapisujący zespół do kontraktu. Dopiero po ustaleniu przykładów i zgodności wersji rozdziela domenę, UI i adapter. Dla kodu proponujemy osobne krótkie gałęzie i worktree z tego samego zatwierdzonego punktu. Przy nakładających się plikach zleca zmiany kolejno. Discovery wciąż ma istniejący workflow na main. |
| Realizacja i integracja | Autor podaje zakres, testy, zmiany danych i skutki awarii. Prowadzący najpierw integruje zgodny wstecz kontrakt, potem odbiorców. Weryfikuje wspólny przebieg po scaleniu zmian w środowisku testowym. |
| Niezależne review | Drugi agent czyta różnicę względem bazy i zatwierdzony scenariusz bez polegania na streszczeniu autora. QA sprawdza normalne wejście użytkownika i wyjątek. Dla wpłat, uprawnień, rezerwacji i migracji osobny przegląd ryzyka, dowód i akceptacja właściciela. Zmiana po recenzji wymaga sprawdzenia zmienionego zakresu. |
| Zakończenie (Definition of Done) | Dowód odbioru, wynik testów i review właściwej wersji, zgodne kontrakty, wpływ na migrację i odtworzenie, rozstrzygnięte uwagi. Właściciel zatwierdza wydanie produkcyjne osobno. |
| Przerwanie pracy | W Issue lub PR zapisać bazę i wersję, zakres, skończone i pozostałe kroki, wynik ostatniego sprawdzenia, niepewność oraz zależności. Nowy agent odczytuje status, Issue i różnicę, sprawdza stan drzewa i kontynuuje od pierwszego brakującego dowodu. |

**Open question.** Czy powtarzalne zadania recenzenta i badacza uzasadnią projektowe definicje własnych subagentów? Na początek wystarczają ograniczony zakres, zadanie i dostęp tylko do odczytu dla recenzenta. Wersjonowane profile roli warto porównać, jeśli przy kolejnych zadaniach powtarzają się błędy zakresu. Profil subagenta i profil ustawień całej sesji CLI mają odrębne zastosowania. [Dokumentacja subagentów Codex](https://developers.openai.com/codex/subagents)
