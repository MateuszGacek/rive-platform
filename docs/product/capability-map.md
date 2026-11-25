# rivé — mapa możliwości produktu v2.1

**Status biznesowy**: `Potwierdzone` to cel zapisany przez właściciela, `Hipoteza` wymaga dowodu, a `Do decyzji` wymaga wyboru reguły lub zakresu. **Priorytet wdrożenia**: `Nieustalony` do czasu decyzji właściciela o `MVP`, `V1` lub `Później`. Sposób dostawy rozstrzyga [D-13](open-questions.md#d-13). Zastosowanie [obowiązków prawnych](../research/hotel-spa-benchmark.md#zgodność-w-polsce-do-potwierdzenia-przed-wyborem-rozwiązania) oceniamy dla danego procesu na podstawie źródeł.

[Ustalenia właściciela](../discovery.md) · [Pytania i decyzje](open-questions.md) · [Plan pracy agentów](agent-delivery-plan.md) · [Mapa w Obsidianie](../maps/rive-product-map.canvas)

## 01 Website i CMS

**Sprzedaż.** Redakcja, dostępność strony i przekazanie gościa do sprzedaży. [Pytanie D-03](open-questions.md#d-03).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| WEB-01 | Edycja treści i stron oferty (bez WordPressa) | Potwierdzone | Nieustalony | Osoba z uprawnieniem może samodzielnie edytować, sprawdzić podgląd i publikować. Wybór CMS później. [D-03](open-questions.md#d-03) |
| WEB-02 | Prezentacja noclegów i szczegółów oferty | Potwierdzone | Nieustalony | Zakres zdjęć, udogodnień, opisów do ustalenia |
| WEB-03 | Kontakt przez formularz | Potwierdzone | Nieustalony | Wiadomość trafia na wspólną skrzynkę recepcji. Recepcja odpowiada ze skrzynki. Ochrona przed spamem i zgody do ustalenia. [D-03](open-questions.md#d-03) |
| WEB-04 | Okresowe publikowanie wydarzeń | Potwierdzone | Nieustalony | Treść i publikacja na stronie oraz przejście do zakupu biletu. Sprzedaż i pojemność opisuje EVT-04. |
| WEB-05 | Przejście ze strony do rezerwacji | Potwierdzone | Nieustalony | Wspólna dostępność z rezerwacjami pracowników |

## 02 Katalog, produkty i cenniki

**Sprzedaż.** Rozdziel opis marketingowy, produkt sprzedażowy, reguły ceny i wersję zaakceptowanej oferty. [Pytanie D-03](open-questions.md#d-03).

| ID     | Możliwość                                 | Status biznesowy | Priorytet wdrożenia | Uwaga                                                                                                                                                                            |
| ------ | ----------------------------------------- | ---------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CAT-01 | Model katalogu i warianty taryf           | Potwierdzone     | Nieustalony         | Sam nocleg rozliczany za jednostkę za noc. Cena dostępu w pakiecie zależy od liczby osób. Szczegóły taryf, m.in. sezon, termin, czas i kanał, oraz kolejność reguł do ustalenia. |
| CAT-02 | Utrwalenie warunków zaakceptowanej oferty | Do decyzji       | Nieustalony         | W D-03 porównaj zmianę taryfy przed potwierdzeniem i po nim, w tym wpływ na wycenę i korekty.                                                                                    |

## 03 Rezerwacje i dostępność

**Sprzedaż.** Pokoje lub pule, reguły blokady i zwolnienia oraz konflikty między kanałami. [Pytanie D-03](open-questions.md#d-03).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| BKG-01 | Wyszukanie noclegu na podstawie terminu | Potwierdzone | Nieustalony | UX inspirowany platformami rezerwacyjnymi, nie ich pełny zakres |
| BKG-02 | Kalendarz dostępności noclegów | Potwierdzone | Nieustalony | Dostępność ma uwzględniać stronę rivé, recepcję i Booking.com. [D-11](open-questions.md#d-11) |
| BKG-03 | Rezerwacja online | Potwierdzone | Nieustalony | Na start jedno zamówienie online obejmuje jedną jednostkę. Formularz czasowo blokuje miejsce, potwierdzenie WWW następuje po zaliczce. Minimum danych osobowych do uzgodnienia |
| BKG-04 | Ręczna rezerwacja przy rozmowie telefonicznej | Potwierdzone | Nieustalony | W panelu uprawnionego pracownika |
| BKG-05 | Jednostki noclegowe i ograniczenia | Potwierdzone | Nieustalony | Edytowalna oferta [studiów, apartamentów i domków](../discovery.md#wywiad-z-właścicielem--oferta-noclegowa-2026-11-19). Gość wybiera rodzaj noclegu na stronie. Różne pojemności to osobne opcje i pule. Przydział konkretnej jednostki i jego zmiana należą do recepcji. |
| BKG-06 | Zmiany, anulowanie, no-show i zasady zaliczek | Do decyzji | Nieustalony | Nocleg potwierdzamy po zaliczce. Ustalono procent, terminy wpłaty i możliwość dopłaty przy zameldowaniu lub wyjeździe. Ustalono zmianę terminu z tygodniowym wyprzedzeniem, zasady anulacji i ręczne zwalnianie nocy przy no-show. Otwarte m.in. graniczna godzina zmiany i dokument zwrotu. [Reguły noclegów](../discovery.md#zmiana-terminu-noclegu--2026-11-20) |

## 04 SPA, wydarzenia i vouchery

**Sprzedaż.** Rozdziel wejście czasowe, sesję o stałej godzinie i zabieg z zasobami. [Pytanie D-04](open-questions.md#d-04).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| EVT-01 | Publikowanie wydarzeń na stronie | Potwierdzone | Nieustalony | Historyczny ID publikacji. Bieżący zakres opisuje WEB-04. |
| EVT-02 | Dostępność i rezerwacje usług SPA | Potwierdzone | Nieustalony | Recepcja uzgadnia termin masażu bezpośrednio z masażystą i zapisuje go w panelu. Reguły dostępności innych zabiegów do ustalenia. [Ustalenia](../discovery.md#oferta-i-dalszy-rozwój--2026-11-20) |
| EVT-03 | Pakiety noclegu i usług | Potwierdzone | Nieustalony | Sam nocleg jest bez dostępu. [Pakiet](reception-discovery.md#pakiety-noclegowe-z-dostępem-do-ośrodka) może obejmować cały pobyt albo jedno wejście z limitem czasu. Gwarancja dostępności składowych, koszyk i anulowanie do ustalenia. |
| EVT-04 | Vouchery, wydarzenia i rezerwacje grupowe | Potwierdzone | Nieustalony | Vouchery kwotowe i usługowe sprzedajemy na stronie oraz w recepcji z tej samej oferty. Voucher kwotowy można wykorzystać w częściach. Bilety kupuje się na stronie. Wydarzenie ma własny limit biletów, a obsługa może ograniczyć pulę Day SPA lub zarezerwować ośrodek na wyłączność. |
| EVT-05 | Wejścia czasowe i naliczanie opłaty | Potwierdzone | Nieustalony | Recepcja potwierdza wejście i wyjście każdej osoby. Na start naliczanie minutowe. W pierwszym pakiecie 4 h dopłata po przekroczeniu czasu jest minutowa. Dokument korekty i potwierdzenie wykonanego zwrotu do uzgodnienia. |
| EVT-06 | Rezerwacje wejść i wspólna pojemność | Potwierdzone | Nieustalony | Na start strona pokazuje wolne terminy, a rezerwację przyjmuje recepcja telefonicznie. Jedna pula dla całego ośrodka i osobny stan faktycznej obecności. Próg operacyjny to 40 osób. Recepcja może przyjąć dodatkowe osoby według faktycznego obłożenia, bez osobnego stałego sufitu w panelu. [Blokada przy spóźnieniu](reception-discovery.md#spóźnienie-na-zarezerwowane-wejście) ustalona. Zapas na przedłużenia do decyzji. Odrębne strefy to opcja na przyszłość. |

Tematy do warsztatu D-04:

- **Wejście czasowe i pojemność (EVT-05, EVT-06).** [Ustalenia z wywiadu i próby](reception-discovery.md#day-spa-bez-noclegu). Do doprecyzowania taryfy, korekty i obsługa wyjątków po wyczerpaniu puli.
- **Zabieg (EVT-02).** Dostępność terapeuty, gabinetu i sprzętu oraz obsługa konfliktu jednego z zasobów.
- **Wydarzenie (EVT-04).** Termin, pojemność lub wyłączność, uczestnicy, rezerwacja i ewentualna sprzedaż biletów.
- **Voucher (EVT-04).** Sprzedaż, aktywacja, rezerwacja i użycie, saldo po częściowym wykorzystaniu, ważność, anulowanie i zwrot. Uzgodnij skutki dla rozliczenia.

## 05 Klienci i komunikacja

**Sprzedaż.** Gość, kontakt rezerwacji, uczestnik i płatnik mogą wymagać osobnych relacji. [Pytanie D-05](open-questions.md#d-05).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| CRM-01 | Powiązania profili gościa między narzędziami | Hipoteza | Nieustalony | Sprawdzić identyfikatory dostawców i ręczne rozstrzyganie duplikatów. Wspólny identyfikator jest opcją. |
| CRM-02 | Komunikaty do gości | Do decyzji | Nieustalony | Ustal zdarzenie, odbiorcę i treść potwierdzeń, przypomnień i innych wiadomości. Kanał i dowód dostawy opisuje INT-05. |

## 06 Recepcja i rachunki gości

**Operacje.** Wspólny rachunek od rezerwacji lub przyjazdu. Pozycja, przypisanie do osoby i wpłata to trzy różne zdarzenia. [Pytanie D-02](open-questions.md#d-02).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| OPS-01 | Otwarcie rachunku klienta przy rezerwacji lub przy wejściu | Potwierdzone | Nieustalony | Rachunek grupy domyślnie przypisany do rezerwującego. Dwa pobyty klienta mogą mieć równoległe otwarte rachunki. |
| OPS-02 | Dopisywanie zakupów do otwartego rachunku | Potwierdzone | Nieustalony | Gastronomia, usługi i pozostałe pozycje |
| OPS-03 | Podgląd i korekta pozycji rachunku | Do decyzji | Nieustalony | Uprawnienia, anulowanie pozycji, ślad audytowy |
| OPS-04 | Zamknięcie rachunku i odnotowanie rozliczenia | Potwierdzone | Nieustalony | Integracja z urządzeniami nie jest przesądzona |
| OPS-05 | Wspólny rachunek przez rezerwację i pobyt | Potwierdzone | Nieustalony | Obejmuje nocleg, zakupy SPA i gastronomiczne, zaliczki oraz końcowe rozliczenie. Recepcja może wybrać jeden wspólny rachunek dla dwóch pobytów klienta. [Zasady](reception-discovery.md#punkt-wyjścia) |
| OPS-06 | Obsługa rachunku niezależnie od noclegu | Potwierdzone | Nieustalony | Wizyta dzienna może być rozliczona indywidualnie lub na wspólnym rachunku. Zakończenie wizyty kończy naliczanie czasu danej osoby. |
| OPS-07 | Przypisywanie i rozdzielanie pozycji lub wpłat między gości | Potwierdzone | Nieustalony | Recepcja może przypisywać pozycje konkretnym osobom podczas pobytu i zmieniać podział przy końcowym rozliczeniu; zaliczki, częściowo opłacone pozycje i fiskalizacja do zbadania |
| OPS-08 | Rozpoczęcie i zakończenie pobytu | Do decyzji | Nieustalony | Ustal zdarzenia przyjazdu i wyjazdu, wpływ na gotowość pokoju oraz zakres danych potrzebnych do raportowania. |
| OPS-09 | Uzgodnienie wpłat na żądanie | Do decyzji | Nieustalony | Raport wpłat jest dostępny w razie potrzeby. Do ustalenia pozostaje obsługa rozbieżności. [D-09](open-questions.md#d-09) |

[Warsztat recepcji](reception-discovery.md) · [Canvas recepcji](../maps/rive-reception.canvas)

## 07 Gastronomia i POS

**Operacje.** Z katalogu gastronomii do rachunku albo rozliczenia na miejscu według ustalonej reguły. [Pytanie D-02](open-questions.md#d-02).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| POS-01 | Użycie produktów i taryf w gastronomii | Potwierdzone | Nieustalony | Sprzedaż z katalogu gastronomii według zasad CAT-01. Właściciel katalogu i reguły uzgodnienia cen zależą od sposobu dostawy. Magazyn poza potwierdzonym zakresem. |
| POS-02 | Dopisanie zakupu gastronomicznego do wspólnego rachunku | Potwierdzone | Nieustalony | Pozycja trafia raz na właściwy rachunek. Źródło zapisu i obsługa powtórzenia zależą od sposobu dostawy. |
| POS-03 | Zapłata za zamówienie na miejscu | Potwierdzone | Nieustalony | Domyślnie zamówienie trafia na otwarty rachunek. Na życzenie gościa gastronomia przyjmuje zapłatę od razu, a system oznacza zamówienie jako opłacone. Dokumenty do uzgodnienia. [Zasady](reception-discovery.md#punkt-wyjścia) |

## 08 Personel i czas pracy

**Operacje.** Zmiana w grafiku, dostępność do usługi, zarejestrowana praca i kalkulacja wynagrodzeń mają różne cele. [Pytanie D-06](open-questions.md#d-06).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| HR-01 | Pracownik zapisuje dni i godziny pracy | Potwierdzone | Nieustalony | „Rozpocznij” i „Zakończ” automatycznie uzupełniają przedział. Pracownik może go poprawić albo wpisać ręcznie. [D-06](open-questions.md#d-06) |
| HR-02 | Podgląd własnej ewidencji czasu | Do decyzji | Nieustalony | Zakres historii i korekt |
| HR-03 | Korekty wpisów i historia zmian | Potwierdzone | Nieustalony | Pracownik sam poprawia własne wpisy. Po zamknięciu okresu system dodatkowo informuje kierownika o korekcie. [D-06](open-questions.md#d-06) |
| HR-04 | Grafiki i dostępność personelu | Potwierdzone | Nieustalony | Plan zmian oraz zależność usług od dostępności pracownika. Reguły podmian i kolizji do ustalenia. |
| HR-05 | Wewnętrzna kalkulacja wynagrodzeń | Potwierdzone | Nieustalony | Stawki, prowizje, okres i eksport do ustalenia. Formalne płace mają osobny proces. |
| HR-06 | Nieobecności i ich wpływ na obsadę | Potwierdzone | Nieustalony | Kto zgłasza zmianę i co robimy z usługami już zarezerwowanymi? |

## 09 Sprzątanie i utrzymanie obiektu

**Operacje.** Gotowość pokoju wpływa na wydanie, a blokada zasobu może wpływać na sprzedaż. [Pytanie D-07](open-questions.md#d-07).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| FAC-01 | Gotowość pokoi, sprzątanie i zadania | Potwierdzone | Nieustalony | Po wymeldowaniu jednostka trafia na wspólną listę do sprzątania. Jednostki z najbliższym przyjazdem są wyżej. Pracownik wybiera następną. [Ustalenia](../discovery.md#gotowość-noclegu--2026-11-20) |
| FAC-02 | Usterki i blokady zasobów | Potwierdzone | Nieustalony | Recepcja może wyłączyć jednostkę i wybrać automatyczne wygaśnięcie lub ręczne zdjęcie blokady. Skutki dla wydania i sprzedaży do doprecyzowania. [Ustalenia](../discovery.md#gotowość-noclegu--2026-11-20) |

## 10 Płatności i fiskalizacja

**Finanse.** Połącz potwierdzenie wpłaty, saldo, korektę i dokument przez uzgodnione odniesienia. [Pytanie D-08](open-questions.md#d-08).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| PAY-01 | Zaliczki, dopłaty, wpłaty częściowe i dzielone, zwroty | Potwierdzone | Nieustalony | Reguły przyjęcia i potwierdzenia wpłaty, alokacji, korekty i zwrotu. Wpłata zmienia saldo bez nowej pozycji sprzedaży. Raportowanie opisuje FIN-05. |
| PAY-02 | Dokumenty, korekty i uzgodnienie fiskalne | Do decyzji | Nieustalony | Kwalifikacja z księgowością i demonstracja na wybranym urządzeniu lub u dostawcy. |
| INT-01 | Obsługa płatności kartą / BLIK / terminalem | Potwierdzone | Nieustalony | Na start pracownik sprawdza wynik na terminalu i potwierdza wpłatę ręcznie w panelu. Integracja terminala odłożona. |
| INT-02 | Rozliczenia i kasa fiskalna | Potwierdzone | Nieustalony | Wpływ na system wymaga ustalenia |

## 11 Finanse i analityka

**Finanse.** Uzgodnienie danych źródłowych przed raportami zarządczymi. [Pytanie D-09](open-questions.md#d-09).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| FIN-01 | Sprzedaż według kategorii | Potwierdzone | Nieustalony | Noclegi, gastronomia, usługi itd. |
| FIN-02 | Obrót, przychód i udziały procentowe | Potwierdzone | Nieustalony | Definicje brutto/netto, memoriałowo/kasowo do uzgodnienia |
| FIN-03 | Raporty dostępne dla kierownictwa | Potwierdzone | Nieustalony | Osobne uprawnienia od operacyjnego rachunku gościa |
| FIN-04 | Koszty, marże i zyski | Potwierdzone | Nieustalony | Źródła kosztów, sposób ich przypisania i definicje do ustalenia. Eksport jako osobna decyzja. |
| FIN-05 | Raportowanie i uzgodnienie wpłat, zaliczek i sald | Potwierdzone | Nieustalony | Raport wpłat według metod dostępny na żądanie do porównania z gotówką i raportem terminala. [D-09](open-questions.md#d-09) |
| FIN-06 | Porównanie okresów, budżet i prognozy | Potwierdzone | Nieustalony | Kierunek raportowania. Najpierw słownik danych i uzgodnienie podstawowych raportów. |

## 12 Użytkownicy, role i dostęp

**Platforma.** Macierz ról, operacji i zakresu danych oraz ślad korekt. [Pytanie D-10](open-questions.md#d-10).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| IAM-01 | Logowanie uprawnionych pracowników | Potwierdzone | Nieustalony | Metoda uwierzytelniania nieustalona |
| IAM-02 | Role pracownika / supervisor / administrator | Potwierdzone | Nieustalony | Dokładna macierz uprawnień do zdefiniowania |
| IAM-03 | Ograniczenia wglądu do finansów | Potwierdzone | Nieustalony | Pracownik nie widzi wrażliwych danych finansowych |
| IAM-04 | Uprawnienia do operacji i korekt rachunków | Do decyzji | Nieustalony | Kto może anulować, edytować lub zamknąć rachunek |
| IAM-05 | Dziennik ważnych operacji | Do decyzji | Nieustalony | Przed produkcją pokaż ślad istotnych korekt, wpłat i zmian dostępu w wybranym rozwiązaniu. Zakres zdarzeń i wglądu ustal w D-10. |

## 13 Integracje i dystrybucja

**Platforma.** Mapuj właściciela faktu, dozwolone kierunki zapisu i obsługę rozbieżności. [Pytanie D-11](open-questions.md#d-11).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| INT-03 | Dystrybucja OTA i channel manager | Potwierdzone | Nieustalony | Import rezerwacji, zmian i anulowań z Booking.com. Wspólna pula z rivé. Obsługa aktualizuje na Booking.com ceny i dostępność ręcznie, a recepcja rozwiązuje konflikty. Możliwość dodania kolejnych integracji. [D-11](open-questions.md#d-11) |
| INT-04 | Księgowość, eksport i dokumenty | Do decyzji | Nieustalony | Nie budujemy własnego systemu fiskalizacji bez analizy |
| INT-05 | Kanały e-mail, SMS i kalendarz oraz dowód dostawy | Potwierdzone | Nieustalony | Kierunek integracyjny z ankiety. Ustal kanał, potwierdzenie dostawy lub synchronizacji i obsługę błędów dla komunikatów z CRM-02. |
| INT-06 | Umowy integracji i eksport danych | Do decyzji | Nieustalony | Sprawdzić wersję, licencję, sandbox, limity, zakres zapisu, potwierdzenia i eksport po zakończeniu umowy. |

## 14 Dane i migracja

**Platforma.** Ustal zakres migracji, uprawnienia, przenośność i uzgodnienie danych. [Pytanie D-12](open-questions.md#d-12).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| DAT-01 | Zakres i próba migracji | Do decyzji | Nieustalony | Jeśli migracja będzie potrzebna, obejmie dane do bieżącej obsługi. Właściciel planuje spróbować samodzielnie w przyszłości. [D-12](open-questions.md#d-12) |
| DAT-02 | Prywatność i retencja danych | Do decyzji | Nieustalony | Ustalić cele, role, zakres i retencję, w tym ewentualne dane o zdrowiu i dane płacowe. |

## 15 Inżynieria i ciągłość działania

**Platforma.** Przećwicz awarię, odzyskanie i odbiór przed wyborem zakresu własnego kodu. [Pytanie D-13](open-questions.md#d-13).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| ENG-01 | Ręczna obsługa podczas awarii | Potwierdzone | Nieustalony | Właściciel akceptuje procedurę ręczną. Uzgodnić zapis, wznowienie i rozliczanie rozbieżności. |
| ENG-02 | Monitoring, kopie i próbne odtworzenie | Do decyzji | Nieustalony | Przed produkcją pokaż monitoring i próbę odtworzenia w zakresie wybranego rozwiązania. Tolerancję przerwy i utraty danych ustal w D-13. |
| ENG-03 | Odsyłacz do decyzji o dostawie i architekturze | Do decyzji | Nieustalony | Porównanie czterech wariantów i wybór architektury prowadzi [D-13](open-questions.md#d-13). |

## Zależności przekrojowe

| Przepływ | Co musi być zgodne |
| --- | --- |
| Katalog → strona / rezerwacje / POS / SPA | Opis handlowy, reguła ceny, cena przyjęta przez gościa i kategoria pozycji. |
| WWW / recepcja / OTA → rezerwacja → wizyta | Sprzedaż korzysta z uzgodnionego źródła dostępności. Opóźnienie OTA i zmiany mają ścieżkę uzgodnienia. |
| WWW / telefon / recepcja → wejścia do ośrodka | Rezerwacje korzystają ze wspólnej puli. Odnotowane wejścia i wyjścia aktualizują faktyczną zajętość i wpływają na przyjmowanie kolejnych rezerwacji. |
| Usterka / sprzątanie → dostępność i wydanie | Oddziel blokadę sprzedaży od gotowości do przyjęcia gościa. |
| Grafik / gabinet / sprzęt / pojemność → SPA i pakiety | Wszystkie wymagane zasoby są dostępne w uzgodnionym czasie. Nieobecność ujawnia dotknięte rezerwacje. |
| Rezerwacja / wizyta / POS / SPA → rachunek | Właściwy klient i wizyta, jawna alokacja grupowa, brak powtórnych pozycji. |
| Rachunek → płatność / dokument → finanse | Pozycje, wpłaty i dokumenty można uzgodnić niezależnie. Zwrot lub korekta mają ślad. |
| Klient / role → wszystkie operacje | Minimalne dane i uprawnienia odpowiednie do roli, operacji i zakresu. |
| Integracje / dane → ciągłość działania | Każdy fakt ma właściciela, a zapis ręczny można uzgodnić po awarii. |

### Powiązania kart

| Karty | Zależność |
| --- | --- |
| WEB-05 → BKG-01 | Przejście z oferty do rezerwacji. |
| CAT-01 → BKG-05 | Taryfa i ograniczenia rezerwacji. |
| BKG-03 / BKG-04 → OPS-05 | Rezerwacja online lub telefoniczna przechodzi w wizytę i wspólny rachunek. |
| BKG-05 → OPS-08 | Gość wybiera rodzaj noclegu, a recepcja przydziela konkretną jednostkę. |
| OPS-02 → FIN-01 | Pozycja ma kategorię sprzedaży. |
| OPS-04 → FIN-02 | Rozliczenie ma dane do uzgodnienia z raportem obrotu. |
| IAM-03 → FIN-03 | Uprawnienia rozstrzygają dostęp do raportów. |
| HR-04 → EVT-02 | Dostępność personelu warunkuje termin zabiegu. |
| INT-01 → OPS-04 | Sposób potwierdzenia wpłaty wpływa na zamknięcie. |
| EVT-03 → BKG-02 | Pakiet korzysta z dostępności noclegu i pozostałych składowych. |
| EVT-03 → OPS-08 | Rezerwacja określa liczbę osób z dostępem w pakiecie. Recepcja przypisuje dostęp konkretnym uczestnikom pobytu. |
| OPS-05 → OPS-07 | Wspólny rachunek pozwala przypisać pozycje i rozdzielić wpłaty. |
| INT-03 → BKG-02 | Kanały OTA korzystają z uzgodnionej dostępności. |
| FAC-02 → BKG-02 | Blokada techniczna może ograniczać sprzedaż. |
| EVT-05 → OPS-06 | Czas każdej osoby wpływa na pozycje na rachunku wizyty dziennej. |
| OPS-06 → EVT-06 | Recepcja odnotowuje wejścia i wyjścia. Faktyczna obecność wpływa na dostępność wejść. |
| CRM-01 → OPS-01 | Właściwa identyfikacja klienta pozwala powiązać rachunek. |
| POS-02 → OPS-02 | Zakup trafia na właściwy rachunek. |
| OPS-07 → PAY-01 | Podział pozycji i saldo wyznaczają pytania o alokację wpłat. |
| PAY-01 → BKG-03 | Potwierdzona zaliczka zamienia tymczasową blokadę dostępności w potwierdzoną rezerwację noclegu. |
| PAY-01 → FIN-05 | Potwierdzone wpłaty i saldo są uzgadniane w raporcie. |
| INT-06 → ENG-01 | Integracja i eksport pozwalają uzgodnić zapis po awarii. |
| OPS-04 → PAY-01 | Saldo rachunku i dyspozycja rozliczenia są wejściem do procesu wpłaty. |

## Macierz kompletności discovery

**Proposed — ocena materiału, druga sesja 2026-11-25.** Każdą komórkę czytamy w odniesieniu do głównego przebiegu wskazanego w wierszu. **R** — rozwinięte: można opisać konkretny przypadek i oczekiwany wynik na podstawie decyzji właściciela. **C** — częściowe: jest przykład, propozycja lub reguła dla fragmentu. **W** — wstępne: zapisano cel albo pytanie. R dotyczy przykładu w danym wymiarze. Zatwierdzenie scenariusza przekrojowego oraz zamknięcie fazy należą do właściciela. Dla integracji oceniamy wiedzę o wymianie z innymi narzędziami, dla jakości — opis kryteriów odbioru. Warianty przygotowane przez agentów pozostają propozycjami.

| Obszar | Funkcje | Reguły | Dane | Zależności | Wyjątki | UX | Integracje | Jakość | Dowód i granica pokrycia |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 01 Website i CMS | R | C | C | R | C | C | C | C | WEB-01/05: znamy redaktora, podgląd i kanał zakupu. Brakuje przebiegu wycofania oferty z aktywnymi zakupami i odpowiedzialności za aktualność tłumaczeń. |
| 02 Katalog i ceny | C | C | C | R | C | W | C | C | CAT-01/02: nocleg za jednostkę, pakiet wg osób. Nadal nie wiadomo, która taryfa wygrywa przy zbiegu promocji ani co obowiązuje podczas zapłaty po zmianie cennika. |
| 03 Rezerwacje i dostępność | R | R | R | R | C | R | C | C | BKG-02/03/06: znane blokady, dopłaty, zmiana terminu i atomowa zamiana jednostek. Wpłata potwierdzona przez operatora po wygaśnięciu blokady wymaga odróżnienia od ustalonej procedury spóźnionego przelewu. |
| 04 SPA, vouchery, wydarzenia | R | C | C | R | C | C | C | C | EVT-02–06: Day SPA ma scenariusze od wejścia do zwrotu. Znamy częściową realizację vouchera i wpływ wydarzenia na pulę. Retreat bez dostępnej składowej i odwrócenie realizacji vouchera pozostają otwarte. |
| 05 Gość i komunikacja | C | C | C | R | C | C | C | C | CRM-01/02: ustalono minimum przy wejściu i kontakt telefoniczny. Wspólny telefon dwóch osób nie wystarcza do scalenia historii. Brakuje reguły rozstrzygnięcia i odpowiedzialności za błędny kontakt. |
| 06 Recepcja i rachunki | R | R | R | R | C | R | C | C | OPS-01/05/07: podział, ponowne przypisanie pozycji i zachowanie płatnika są opisane. Luka dotyczy m.in. błędu POS odkrytego po zamknięciu rachunku. |
| 07 Gastronomia i POS | R | R | C | R | C | C | C | C | POS-02/03: znamy obciążenie folio i zapłatę od razu. Wymaga rozstrzygnięcia wyścig pomiędzy zamknięciem rachunku a dopisaniem zamówienia oraz sposób potwierdzania zapisu przez zewnętrzny POS. |
| 08 Personel | R | C | C | R | C | R | C | C | HR-01/03: rejestracja i poprawianie czasu są rozwinięte. Dla grafików, absencji, wynagrodzeń i korekty zamkniętego okresu brakuje zasad rozliczenia. |
| 09 Obiekt | R | R | C | R | C | R | W | C | FAC-01/02: wspólna lista sprzątania, decyzja recepcji przy wydaniu oraz blokada usterki mają przebiegi. Przy zmianie blokady nie ustalono, jak obsługa wykrywa nieaktualną dostępność u pośrednika. |
| 10 Płatności i dokumenty | R | C | C | R | C | C | C | C | PAY-01/02: potwierdzenie karty na terminalu w obiekcie jest ręczne, przelew i zwrot mają wskazanych operatorów czynności. Otwarte dowody wykonania zwrotu, dokumenty i odpowiedzialność przy rozbieżności. |
| 11 Finanse | C | C | C | R | C | C | C | C | FIN-01/04/05: znany raport metod wpłat. Dla rentowności istnieje przykład porównawczy w D-09; okres, koszty i alokacja pakietów czekają na decyzję. Budżet i prognozy mają dopiero opis celu. |
| 12 Role i dostęp | C | C | C | R | C | C | C | C | IAM-02–05: znane ograniczenia widoku gastronomii i własnego czasu pracy. Brakuje właściciela uprawnień do eksportów i zamkniętych korekt oraz sposobu odebrania dostępu na wspólnym urządzeniu. |
| 13 Integracje | C | C | C | R | C | C | C | C | INT-03/05/06: znamy kierunek wymiany z Booking.com i rozstrzyganie kolizji. Brakuje potwierdzonego dostępu, sposobu identyfikacji zmian i możliwości eksportu. Pozostałe kanały mają słabsze pokrycie. |
| 14 Dane i migracja | C | C | C | C | C | W | C | C | DAT-01/02: wskazano minimalny zakres ewentualnej migracji. Brakuje próbki eksportu, reguł dopasowania sald, celów/okresów retencji i obsługi rozbieżności częściowo zrealizowanego vouchera. |
| 15 Ciągłość pracy | C | C | C | R | C | C | C | C | ENG-01/02: papierowe wejścia SPA i odtworzenie faktycznych godzin są ustalone. Dla pozostałych operacji mamy propozycję próby. Brakuje tolerancji przerwy/utraty danych i osoby decydującej o wznowieniu. |

Dowody szczegółowe: [wywiady o noclegach, personelu i obiekcie](../discovery.md), [przypadki recepcji](reception-discovery.md), [10 procesów przekrojowych](../research/platform-workflows.md), [ryzyka i próby odbioru](../research/quality-and-recovery.md), [decyzje D-01–13](open-questions.md). Praktyczna granica pokrycia przebiega także **wewnątrz** obszaru: np. finanse mają uzgodniony raport wpłat, a prognozowanie dopiero nazwę i cel.
