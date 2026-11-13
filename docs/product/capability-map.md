# rivé — mapa możliwości produktu v2

Stan discovery na 13.11.2026. **Wymagane** oznacza cel biznesowy zapisany przez właściciela. **Do weryfikacji** oznacza hipotezę, nieustaloną regułę lub zakres techniczny. Terminy, MVP i architektura wymagają osobnej decyzji.

[Ustalenia właściciela](../discovery.md) · [Pytania i decyzje](open-questions.md) · [Plan pracy agentów](agent-delivery-plan.md) · [Mapa w Obsidianie](../maps/rive-product-map.canvas)

## 01 Website i CMS

**Sprzedaż.** Redakcja, dostępność strony i przekazanie gościa do sprzedaży. [Pytanie D-03](open-questions.md#d-03).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| WEB-01 | Edycja treści i stron oferty (bez WordPressa) | Wymagane | Szybka strona publiczna, wybór CMS później |
| WEB-02 | Prezentacja noclegów i szczegółów oferty | Wymagane | Zakres zdjęć, udogodnień, opisów do ustalenia |
| WEB-03 | Kontakt przez formularz | Wymagane | Powiadomienia, spam, zgody do ustalenia |
| WEB-04 | Okresowe publikowanie wydarzeń | Wymagane | W pierwszej kolejności prezentacja; sprzedaż biletów niezatwierdzona |
| WEB-05 | Przejście ze strony do rezerwacji | Wymagane | Wspólna dostępność z rezerwacjami pracowników |

## 02 Katalog, produkty i cenniki

**Sprzedaż.** Rozdziel opis marketingowy, produkt sprzedażowy, reguły ceny i wersję zaakceptowanej oferty. [Pytanie D-03](open-questions.md#d-03).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| CAT-01 | Model katalogu i warianty taryf | Wymagane | Stałe i zależne od sezonu, terminu, osób, czasu, pakietu lub kanału. Konkretne reguły i kolejność do ustalenia. |
| CAT-02 | Utrwalenie warunków zaakceptowanej oferty | Do weryfikacji | Jak zmiana taryfy wpływa na wyceny, potwierdzone rezerwacje i korekty? |

## 03 Rezerwacje i dostępność

**Sprzedaż.** Pokoje lub pule, reguły blokady i zwolnienia oraz konflikty między kanałami. [Pytanie D-03](open-questions.md#d-03).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| BKG-01 | Wyszukanie noclegu na podstawie terminu | Wymagane | UX inspirowany platformami rezerwacyjnymi, nie ich pełny zakres |
| BKG-02 | Kalendarz dostępności noclegów | Wymagane | Spójność online i recepcji jest krytyczna |
| BKG-03 | Rezerwacja online | Wymagane | Potwierdzanie i dane gości do ustalenia |
| BKG-04 | Ręczna rezerwacja przy rozmowie telefonicznej | Wymagane | W panelu uprawnionego pracownika |
| BKG-05 | Jednostki noclegowe i ograniczenia | Wymagane | Pokoje/jednostki i tryby zależne od oferty. Sprzedaż konkretnej jednostki lub puli do ustalenia. |
| BKG-06 | Zmiany, anulowanie, no-show i zasady zaliczek | Do weryfikacji | Sprawdzić istniejące zasady biznesowe |

## 04 SPA, wydarzenia i vouchery

**Sprzedaż.** Rozdziel wejście czasowe, sesję o stałej godzinie i zabieg z zasobami. [Pytanie D-04](open-questions.md#d-04).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| EVT-01 | Publikowanie wydarzeń na stronie | Wymagane | Na razie ich prezentacja |
| EVT-02 | Dostępność i rezerwacje usług SPA | Wymagane | Oferta może zależeć jednocześnie od pojemności, pomieszczeń, sprzętu i personelu. |
| EVT-03 | Pakiety noclegu i usług | Wymagane | Kierunek oferty. Gwarancja dostępności składowych, koszyk i anulowanie do ustalenia. |
| EVT-04 | Vouchery, wydarzenia i rezerwacje grupowe | Wymagane | Kierunek oferty. Sprzedaż biletów, saldo vouchera, wyłączność i kolejność dostawy do ustalenia. |
| EVT-05 | Wejścia czasowe i dopłaty w strefach | Do weryfikacji | Hipoteza do obserwacji. Potwierdzić moment pomiaru, taryfy, ręczne korekty i dopisanie do rachunku. |
| EVT-06 | Obsługa pojemności stref i sesji | Do weryfikacji | Rozdziel limit rezerwacji i faktyczną obecność oraz uwzględnij zasoby współdzielone. |

## 05 Klienci i komunikacja

**Sprzedaż.** Gość, kontakt rezerwacji, uczestnik i płatnik mogą wymagać osobnych relacji. [Pytanie D-05](open-questions.md#d-05).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| CRM-01 | Powiązania profili gościa między narzędziami | Do weryfikacji | Sprawdzić identyfikatory dostawców i ręczne rozstrzyganie duplikatów. Wspólny identyfikator jest opcją. |
| CRM-02 | Potwierdzenia, przypomnienia i kontakt | Do weryfikacji | Oddziel komunikację transakcyjną od marketingowej, zweryfikuj kanały i potwierdzenia doręczenia. |

## 06 Recepcja i rachunki gości

**Operacje.** Wspólny rachunek od rezerwacji lub przyjazdu. Pozycja, przypisanie do osoby i wpłata to trzy różne zdarzenia. [Pytanie D-02](open-questions.md#d-02).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| OPS-01 | Otwarcie rachunku klienta przy rezerwacji lub przy wejściu | Wymagane | Przypisany do klienta, wspólny dla rezerwacji/pobytu. Właściciel rachunku grupowego i rachunki równoległe do ustalenia. |
| OPS-02 | Dopisywanie zakupów do otwartego rachunku | Wymagane | Gastronomia, usługi i pozostałe pozycje |
| OPS-03 | Podgląd i korekta pozycji rachunku | Do weryfikacji | Uprawnienia, anulowanie pozycji, ślad audytowy |
| OPS-04 | Zamknięcie rachunku i odnotowanie rozliczenia | Wymagane | Integracja z urządzeniami nie jest przesądzona |
| OPS-05 | Jeden wspólny rachunek przez rezerwację i pobyt | Wymagane | Obejmuje nocleg, zakupy SPA/gastronomiczne, zaliczki oraz końcowe rozliczenie; dla par i grup wspólny rachunek jest domyślny |
| OPS-06 | Obsługa rachunku niezależnie od noclegu | Do weryfikacji | Klienci Day SPA, sauna, basen itd. |
| OPS-07 | Przypisywanie i rozdzielanie pozycji lub wpłat między gości | Wymagane | Recepcja może przypisywać pozycje konkretnym osobom podczas pobytu i zmieniać podział przy końcowym rozliczeniu; zaliczki, częściowo opłacone pozycje i fiskalizacja do zbadania |

## 07 Gastronomia i POS

**Operacje.** Z katalogu gastronomii do rachunku albo rozliczenia na miejscu według ustalonej reguły. [Pytanie D-02](open-questions.md#d-02).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| POS-01 | Katalog gastronomii i ceny | Wymagane | Sprzedaż z katalogu i dopisywanie na rachunek. Magazyn poza potwierdzonym zakresem. |
| POS-02 | Przekazywanie pozycji z gastronomii do folio | Wymagane | Wymagany przebieg biznesowy. Ręczne dopisanie lub integracja POS zależą od decyzji. |

## 08 Personel i czas pracy

**Operacje.** Zmiana w grafiku, dostępność do usługi, zarejestrowana praca i kalkulacja wynagrodzeń mają różne cele. [Pytanie D-06](open-questions.md#d-06).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| HR-01 | Pracownik zapisuje dni i godziny pracy | Wymagane | Suma godzin czy przedział start/koniec — do ustalenia |
| HR-02 | Podgląd własnej ewidencji czasu | Do weryfikacji | Zakres historii i korekt |
| HR-03 | Zatwierdzanie i korekta wpisów | Do weryfikacji | Kto może edytować, audyt zmian |
| HR-04 | Grafiki i dostępność personelu | Wymagane | Plan zmian oraz zależność usług od dostępności pracownika. Reguły podmian i kolizji do ustalenia. |
| HR-05 | Wewnętrzna kalkulacja wynagrodzeń | Wymagane | Stawki, prowizje, okres i eksport do ustalenia. Formalne płace mają osobny proces. |
| HR-06 | Nieobecności i ich wpływ na obsadę | Wymagane | Kto zgłasza zmianę i co robimy z usługami już zarezerwowanymi? |

## 09 Sprzątanie i utrzymanie obiektu

**Operacje.** Gotowość pokoju wpływa na wydanie, a blokada zasobu może wpływać na sprzedaż. [Pytanie D-07](open-questions.md#d-07).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| FAC-01 | Gotowość pokoi, sprzątanie i zadania | Wymagane | Wydanie pokoju zależne od uzgodnionych statusów i odpowiedzialności. |
| FAC-02 | Usterki i blokady zasobów | Wymagane | Ustalić, kiedy usterka blokuje wydanie, a kiedy sprzedaż oraz kto zwalnia blokadę. |

## 10 Płatności i fiskalizacja

**Finanse.** Połącz potwierdzenie wpłaty, saldo, korektę i dokument przez uzgodnione odniesienia. [Pytanie D-08](open-questions.md#d-08).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| PAY-01 | Zaliczki, dopłaty, wpłaty częściowe i dzielone, zwroty | Wymagane | Wpłata zmienia saldo bez tworzenia pozycji sprzedaży. Reguły alokacji i korekt do ustalenia. |
| PAY-02 | Dokumenty, korekty i uzgodnienie fiskalne | Do weryfikacji | Kwalifikacja z księgowością i demonstracja na wybranym urządzeniu lub u dostawcy. |
| INT-01 | Obsługa płatności kartą / BLIK / terminalem | Wymagane jako proces biznesowy | Bez przesądzania o bezpośrednim API |
| INT-02 | Rozliczenia i kasa fiskalna | Wymagane jako proces biznesowy | Wpływ na system wymaga ustalenia |

## 11 Finanse i analityka

**Finanse.** Uzgodnienie danych źródłowych przed raportami zarządczymi. [Pytanie D-09](open-questions.md#d-09).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| FIN-01 | Sprzedaż według kategorii | Wymagane | Noclegi, gastronomia, usługi itd. |
| FIN-02 | Obrót, przychód i udziały procentowe | Wymagane | Definicje brutto/netto, memoriałowo/kasowo do uzgodnienia |
| FIN-03 | Raporty dostępne dla kierownictwa | Wymagane | Osobne uprawnienia od operacyjnego rachunku gościa |
| FIN-04 | Koszty, marże i zyski | Wymagane | Źródła kosztów, sposób ich przypisania i definicje do ustalenia. Eksport jako osobna decyzja. |
| FIN-05 | Metody i statusy wpłat, zaliczek i sald | Wymagane | Status w raportach pochodzi z uzgodnionych wpłat. Nie przesądza o integracji z terminalem. |
| FIN-06 | Porównanie okresów, budżet i prognozy | Wymagane | Kierunek raportowania. Najpierw słownik danych i uzgodnienie podstawowych raportów. |

## 12 Użytkownicy, role i dostęp

**Platforma.** Macierz ról, operacji i zakresu danych oraz ślad korekt. [Pytanie D-10](open-questions.md#d-10).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| IAM-01 | Logowanie uprawnionych pracowników | Wymagane | Metoda uwierzytelniania nieustalona |
| IAM-02 | Role pracownika / supervisor / administrator | Wymagane | Dokładna macierz uprawnień do zdefiniowania |
| IAM-03 | Ograniczenia wglądu do finansów | Wymagane | Pracownik nie widzi wrażliwych danych finansowych |
| IAM-04 | Uprawnienia do operacji i korekt rachunków | Do weryfikacji | Kto może anulować, edytować lub zamknąć rachunek |
| IAM-05 | Dziennik ważnych operacji | Do weryfikacji | Szczególnie płatności, uprawnienia, korekty |

## 13 Integracje i dystrybucja

**Platforma.** Mapuj właściciela faktu, dozwolone kierunki zapisu i obsługę rozbieżności. [Pytanie D-11](open-questions.md#d-11).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| INT-03 | Dystrybucja OTA i channel manager | Wymagane | Priorytet integracyjny z ankiety. Kanały, dostęp do API, synchronizacja i SLA do ustalenia. |
| INT-04 | Księgowość, eksport i dokumenty | Do weryfikacji | Nie budujemy własnego systemu fiskalizacji bez analizy |
| INT-05 | Integracje powiadomień, e-mail, SMS i kalendarza | Wymagane | Priorytet z ankiety. Przypadki, kanał, zgody i obsługa błędów do uzgodnienia. |
| INT-06 | Umowy integracji i eksport danych | Do weryfikacji | Sprawdzić wersję, licencję, sandbox, limity, zakres zapisu, potwierdzenia i eksport po zakończeniu umowy. |

## 14 Dane i migracja

**Platforma.** Ustal zakres migracji, uprawnienia, przenośność i uzgodnienie danych. [Pytanie D-12](open-questions.md#d-12).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| DAT-01 | Zakres i próba migracji | Do weryfikacji | Inwentaryzacja i próbne uzgodnienie rezerwacji, otwartych sald, wpłat, voucherów oraz identyfikatorów. |
| DAT-02 | Prywatność i retencja danych | Do weryfikacji | Ustalić cele, role, zakres i retencję, w tym ewentualne dane o zdrowiu i dane płacowe. |

## 15 Inżynieria i ciągłość działania

**Platforma.** Przećwicz awarię, odzyskanie i odbiór przed wyborem zakresu własnego kodu. [Pytanie D-13](open-questions.md#d-13).

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| ENG-01 | Ręczna obsługa podczas awarii | Wymagane | Właściciel akceptuje procedurę ręczną. Uzgodnić zapis, wznowienie i rozliczanie rozbieżności. |
| ENG-02 | Monitoring, kopie i próbne odtworzenie | Do weryfikacji | Zakres zależny od własności systemów i tolerancji przerwy oraz utraty danych. |
| ENG-03 | Strategia dostawy i architektura | Do weryfikacji | Porównaj cztery warianty na tych samych scenariuszach. Dobierz stack po decyzji o zakresie. |

## Zależności przekrojowe

| Przepływ | Co musi być zgodne |
| --- | --- |
| Katalog → strona / rezerwacje / POS / SPA | Opis handlowy, reguła ceny, cena przyjęta przez gościa i kategoria pozycji. |
| WWW / recepcja / OTA → rezerwacja → wizyta | Sprzedaż korzysta z uzgodnionego źródła dostępności. Opóźnienie OTA i zmiany mają ścieżkę uzgodnienia. |
| Usterka / sprzątanie → dostępność i wydanie | Oddziel blokadę sprzedaży od gotowości do przyjęcia gościa. |
| Grafik / gabinet / sprzęt / pojemność → SPA i pakiety | Wszystkie wymagane zasoby są dostępne w uzgodnionym czasie. Nieobecność ujawnia dotknięte rezerwacje. |
| Rezerwacja / wizyta / POS / SPA → rachunek | Właściwy klient i wizyta, jawna alokacja grupowa, brak powtórnych pozycji. |
| Rachunek → płatność / dokument → finanse | Pozycje, wpłaty i dokumenty można uzgodnić niezależnie. Zwrot lub korekta mają ślad. |
| Klient / role → wszystkie operacje | Minimalne dane i uprawnienia odpowiednie do roli, operacji i zakresu. |
| Integracje / dane → ciągłość działania | Każdy fakt ma właściciela, a zapis ręczny można uzgodnić po awarii. |
