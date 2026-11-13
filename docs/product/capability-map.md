# rivé — mapa możliwości produktu v2.1

**Status biznesowy**: `Potwierdzone` to cel zapisany przez właściciela, `Hipoteza` wymaga dowodu, a `Do decyzji` wymaga wyboru reguły lub zakresu. **Priorytet wdrożenia**: `Nieustalony` do czasu decyzji właściciela o `MVP`, `V1` lub `Później`. Sposób dostawy rozstrzyga [D-13](open-questions.md#d-13). Zastosowanie [obowiązków prawnych](../research/hotel-spa-benchmark.md#zgodność-w-polsce-do-potwierdzenia-przed-wyborem-rozwiązania) oceniamy dla danego procesu na podstawie źródeł.

[Ustalenia właściciela](../discovery.md) · [Pytania i decyzje](open-questions.md) · [Plan pracy agentów](agent-delivery-plan.md) · [Mapa w Obsidianie](../maps/rive-product-map.canvas)

## 01 Website i CMS

**Sprzedaż.** Redakcja, dostępność strony i przekazanie gościa do sprzedaży. [Pytanie D-03](open-questions.md#d-03).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| WEB-01 | Edycja treści i stron oferty (bez WordPressa) | Potwierdzone | Nieustalony | Szybka strona publiczna, wybór CMS później |
| WEB-02 | Prezentacja noclegów i szczegółów oferty | Potwierdzone | Nieustalony | Zakres zdjęć, udogodnień, opisów do ustalenia |
| WEB-03 | Kontakt przez formularz | Potwierdzone | Nieustalony | Powiadomienia, spam, zgody do ustalenia |
| WEB-04 | Okresowe publikowanie wydarzeń | Potwierdzone | Nieustalony | Treść i publikacja na stronie. Terminy, pojemność i sprzedaż należą do obszaru 04. |
| WEB-05 | Przejście ze strony do rezerwacji | Potwierdzone | Nieustalony | Wspólna dostępność z rezerwacjami pracowników |

## 02 Katalog, produkty i cenniki

**Sprzedaż.** Rozdziel opis marketingowy, produkt sprzedażowy, reguły ceny i wersję zaakceptowanej oferty. [Pytanie D-03](open-questions.md#d-03).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| CAT-01 | Model katalogu i warianty taryf | Potwierdzone | Nieustalony | Stałe i zależne od sezonu, terminu, osób, czasu, pakietu lub kanału. Konkretne reguły i kolejność do ustalenia. |
| CAT-02 | Utrwalenie warunków zaakceptowanej oferty | Do decyzji | Nieustalony | W D-03 porównaj zmianę taryfy przed potwierdzeniem i po nim, w tym wpływ na wycenę i korekty. |

## 03 Rezerwacje i dostępność

**Sprzedaż.** Pokoje lub pule, reguły blokady i zwolnienia oraz konflikty między kanałami. [Pytanie D-03](open-questions.md#d-03).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| BKG-01 | Wyszukanie noclegu na podstawie terminu | Potwierdzone | Nieustalony | UX inspirowany platformami rezerwacyjnymi, nie ich pełny zakres |
| BKG-02 | Kalendarz dostępności noclegów | Potwierdzone | Nieustalony | Spójność online i recepcji jest krytyczna |
| BKG-03 | Rezerwacja online | Potwierdzone | Nieustalony | Potwierdzanie i dane gości do ustalenia |
| BKG-04 | Ręczna rezerwacja przy rozmowie telefonicznej | Potwierdzone | Nieustalony | W panelu uprawnionego pracownika |
| BKG-05 | Jednostki noclegowe i ograniczenia | Potwierdzone | Nieustalony | Pokoje/jednostki i tryby zależne od oferty. Sprzedaż konkretnej jednostki lub puli do ustalenia. |
| BKG-06 | Zmiany, anulowanie, no-show i zasady zaliczek | Do decyzji | Nieustalony | W D-03 rozpisz zmianę ceny i terminu, anulowanie oraz no-show. Zasady rozliczenia zaliczek wynikają z PAY-01 i D-08. |

## 04 SPA, wydarzenia i vouchery

**Sprzedaż.** Rozdziel wejście czasowe, sesję o stałej godzinie i zabieg z zasobami. [Pytanie D-04](open-questions.md#d-04).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| EVT-01 | Publikowanie wydarzeń na stronie | Potwierdzone | Nieustalony | Historyczny ID publikacji. Bieżący zakres opisuje WEB-04. |
| EVT-02 | Dostępność i rezerwacje usług SPA | Potwierdzone | Nieustalony | Oferta może zależeć jednocześnie od pojemności, pomieszczeń, sprzętu i personelu. |
| EVT-03 | Pakiety noclegu i usług | Potwierdzone | Nieustalony | Kierunek oferty. Gwarancja dostępności składowych, koszyk i anulowanie do ustalenia. |
| EVT-04 | Vouchery, wydarzenia i rezerwacje grupowe | Potwierdzone | Nieustalony | Kierunek oferty. Sprzedaż biletów, saldo vouchera, wyłączność i kolejność dostawy do ustalenia. |
| EVT-05 | Wejścia czasowe i dopłaty w strefach | Hipoteza | Nieustalony | Hipoteza do obserwacji. Potwierdzić moment pomiaru, taryfy, ręczne korekty i dopisanie do rachunku. |
| EVT-06 | Obsługa pojemności stref i sesji | Hipoteza | Nieustalony | Rozdziel limit rezerwacji i faktyczną obecność oraz uwzględnij zasoby współdzielone. |

Tematy do warsztatu D-04:

- **Wejście czasowe (EVT-05).** Moment startu i końca pomiaru, przedłużenie, dopłata, korekta i powiązanie z wizytą.
- **Sesja z limitem (EVT-06).** Termin, pojemność rezerwowana i faktyczna obecność oraz współdzielone limity.
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
| OPS-01 | Otwarcie rachunku klienta przy rezerwacji lub przy wejściu | Potwierdzone | Nieustalony | Przypisany do klienta, wspólny dla rezerwacji/pobytu. Właściciel rachunku grupowego i rachunki równoległe do ustalenia. |
| OPS-02 | Dopisywanie zakupów do otwartego rachunku | Potwierdzone | Nieustalony | Gastronomia, usługi i pozostałe pozycje |
| OPS-03 | Podgląd i korekta pozycji rachunku | Do decyzji | Nieustalony | Uprawnienia, anulowanie pozycji, ślad audytowy |
| OPS-04 | Zamknięcie rachunku i odnotowanie rozliczenia | Potwierdzone | Nieustalony | Integracja z urządzeniami nie jest przesądzona |
| OPS-05 | Jeden wspólny rachunek przez rezerwację i pobyt | Potwierdzone | Nieustalony | Obejmuje nocleg, zakupy SPA/gastronomiczne, zaliczki oraz końcowe rozliczenie; dla par i grup wspólny rachunek jest domyślny |
| OPS-06 | Obsługa rachunku niezależnie od noclegu | Do decyzji | Nieustalony | Klienci Day SPA, sauna, basen itd. |
| OPS-07 | Przypisywanie i rozdzielanie pozycji lub wpłat między gości | Potwierdzone | Nieustalony | Recepcja może przypisywać pozycje konkretnym osobom podczas pobytu i zmieniać podział przy końcowym rozliczeniu; zaliczki, częściowo opłacone pozycje i fiskalizacja do zbadania |
| OPS-08 | Rozpoczęcie i zakończenie pobytu | Do decyzji | Nieustalony | Ustal zdarzenia przyjazdu i wyjazdu, wpływ na gotowość pokoju oraz zakres danych potrzebnych do raportowania. |
| OPS-09 | Zamknięcie i uzgodnienie zmiany | Do decyzji | Nieustalony | Ustal, kto porównuje otwarte rachunki, gotówkę, wpłaty, zwroty i dokumenty oraz rozstrzyga różnice. |

[Warsztat recepcji](reception-discovery.md) · [Canvas recepcji](../maps/rive-reception.canvas)

## 07 Gastronomia i POS

**Operacje.** Z katalogu gastronomii do rachunku albo rozliczenia na miejscu według ustalonej reguły. [Pytanie D-02](open-questions.md#d-02).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| POS-01 | Użycie produktów i taryf w gastronomii | Potwierdzone | Nieustalony | Sprzedaż z katalogu gastronomii według zasad CAT-01. Właściciel katalogu i reguły uzgodnienia cen zależą od sposobu dostawy. Magazyn poza potwierdzonym zakresem. |
| POS-02 | Dopisanie zakupu gastronomicznego do wspólnego rachunku | Potwierdzone | Nieustalony | Pozycja trafia raz na właściwy rachunek. Źródło zapisu i obsługa powtórzenia zależą od sposobu dostawy. |
| POS-03 | Sprzedaż rozliczana na miejscu | Do decyzji | Nieustalony | Ustal kiedy rozliczamy od razu, jak dokumentujemy zakup i jak unikamy powtórnego obciążenia folio. |

## 08 Personel i czas pracy

**Operacje.** Zmiana w grafiku, dostępność do usługi, zarejestrowana praca i kalkulacja wynagrodzeń mają różne cele. [Pytanie D-06](open-questions.md#d-06).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| HR-01 | Pracownik zapisuje dni i godziny pracy | Potwierdzone | Nieustalony | Suma godzin czy przedział start/koniec — do ustalenia |
| HR-02 | Podgląd własnej ewidencji czasu | Do decyzji | Nieustalony | Zakres historii i korekt |
| HR-03 | Zatwierdzanie i korekta wpisów | Do decyzji | Nieustalony | Kto może edytować, audyt zmian |
| HR-04 | Grafiki i dostępność personelu | Potwierdzone | Nieustalony | Plan zmian oraz zależność usług od dostępności pracownika. Reguły podmian i kolizji do ustalenia. |
| HR-05 | Wewnętrzna kalkulacja wynagrodzeń | Potwierdzone | Nieustalony | Stawki, prowizje, okres i eksport do ustalenia. Formalne płace mają osobny proces. |
| HR-06 | Nieobecności i ich wpływ na obsadę | Potwierdzone | Nieustalony | Kto zgłasza zmianę i co robimy z usługami już zarezerwowanymi? |

## 09 Sprzątanie i utrzymanie obiektu

**Operacje.** Gotowość pokoju wpływa na wydanie, a blokada zasobu może wpływać na sprzedaż. [Pytanie D-07](open-questions.md#d-07).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| FAC-01 | Gotowość pokoi, sprzątanie i zadania | Potwierdzone | Nieustalony | Wydanie pokoju zależne od uzgodnionych statusów i odpowiedzialności. |
| FAC-02 | Usterki i blokady zasobów | Potwierdzone | Nieustalony | Ustalić, kiedy usterka blokuje wydanie, a kiedy sprzedaż oraz kto zwalnia blokadę. |

## 10 Płatności i fiskalizacja

**Finanse.** Połącz potwierdzenie wpłaty, saldo, korektę i dokument przez uzgodnione odniesienia. [Pytanie D-08](open-questions.md#d-08).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| PAY-01 | Zaliczki, dopłaty, wpłaty częściowe i dzielone, zwroty | Potwierdzone | Nieustalony | Reguły przyjęcia i potwierdzenia wpłaty, alokacji, korekty i zwrotu. Wpłata zmienia saldo bez nowej pozycji sprzedaży. Raportowanie opisuje FIN-05. |
| PAY-02 | Dokumenty, korekty i uzgodnienie fiskalne | Do decyzji | Nieustalony | Kwalifikacja z księgowością i demonstracja na wybranym urządzeniu lub u dostawcy. |
| INT-01 | Obsługa płatności kartą / BLIK / terminalem | Potwierdzone | Nieustalony | Bez przesądzania o bezpośrednim API |
| INT-02 | Rozliczenia i kasa fiskalna | Potwierdzone | Nieustalony | Wpływ na system wymaga ustalenia |

## 11 Finanse i analityka

**Finanse.** Uzgodnienie danych źródłowych przed raportami zarządczymi. [Pytanie D-09](open-questions.md#d-09).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| FIN-01 | Sprzedaż według kategorii | Potwierdzone | Nieustalony | Noclegi, gastronomia, usługi itd. |
| FIN-02 | Obrót, przychód i udziały procentowe | Potwierdzone | Nieustalony | Definicje brutto/netto, memoriałowo/kasowo do uzgodnienia |
| FIN-03 | Raporty dostępne dla kierownictwa | Potwierdzone | Nieustalony | Osobne uprawnienia od operacyjnego rachunku gościa |
| FIN-04 | Koszty, marże i zyski | Potwierdzone | Nieustalony | Źródła kosztów, sposób ich przypisania i definicje do ustalenia. Eksport jako osobna decyzja. |
| FIN-05 | Raportowanie i uzgodnienie wpłat, zaliczek i sald | Potwierdzone | Nieustalony | Widoczność metod i statusów oraz uzgodnienie danych źródłowych według reguł PAY-01. |
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
| INT-03 | Dystrybucja OTA i channel manager | Potwierdzone | Nieustalony | Priorytet integracyjny z ankiety. Kanały, dostęp do API, synchronizacja i SLA do ustalenia. |
| INT-04 | Księgowość, eksport i dokumenty | Do decyzji | Nieustalony | Nie budujemy własnego systemu fiskalizacji bez analizy |
| INT-05 | Kanały e-mail, SMS i kalendarz oraz dowód dostawy | Potwierdzone | Nieustalony | Kierunek integracyjny z ankiety. Ustal kanał, potwierdzenie dostawy lub synchronizacji i obsługę błędów dla komunikatów z CRM-02. |
| INT-06 | Umowy integracji i eksport danych | Do decyzji | Nieustalony | Sprawdzić wersję, licencję, sandbox, limity, zakres zapisu, potwierdzenia i eksport po zakończeniu umowy. |

## 14 Dane i migracja

**Platforma.** Ustal zakres migracji, uprawnienia, przenośność i uzgodnienie danych. [Pytanie D-12](open-questions.md#d-12).

| ID | Możliwość | Status biznesowy | Priorytet wdrożenia | Uwaga |
| --- | --- | --- | --- | --- |
| DAT-01 | Zakres i próba migracji | Do decyzji | Nieustalony | Inwentaryzacja i próbne uzgodnienie rezerwacji, otwartych sald, wpłat, voucherów oraz identyfikatorów. |
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
| OPS-02 → FIN-01 | Pozycja ma kategorię sprzedaży. |
| OPS-04 → FIN-02 | Rozliczenie ma dane do uzgodnienia z raportem obrotu. |
| IAM-03 → FIN-03 | Uprawnienia rozstrzygają dostęp do raportów. |
| HR-04 → EVT-02 | Dostępność personelu warunkuje termin zabiegu. |
| INT-01 → OPS-04 | Sposób potwierdzenia wpłaty wpływa na zamknięcie. |
| EVT-03 → BKG-02 | Pakiet korzysta z dostępności noclegu i pozostałych składowych. |
| OPS-05 → OPS-07 | Wspólny rachunek pozwala przypisać pozycje i rozdzielić wpłaty. |
| INT-03 → BKG-02 | Kanały OTA korzystają z uzgodnionej dostępności. |
| FAC-02 → BKG-02 | Blokada techniczna może ograniczać sprzedaż. |
| EVT-05 → OPS-06 | Wejście czasowe może wymagać rachunku wizyty dziennej. |
| CRM-01 → OPS-01 | Właściwa identyfikacja klienta pozwala powiązać rachunek. |
| POS-02 → OPS-02 | Zakup trafia na właściwy rachunek. |
| OPS-07 → PAY-01 | Podział pozycji i saldo wyznaczają pytania o alokację wpłat. |
| PAY-01 → FIN-05 | Potwierdzone wpłaty i saldo są uzgadniane w raporcie. |
| INT-06 → ENG-01 | Integracja i eksport pozwalają uzgodnić zapis po awarii. |
| OPS-04 → PAY-01 | Saldo rachunku i dyspozycja rozliczenia są wejściem do procesu wpłaty. |
