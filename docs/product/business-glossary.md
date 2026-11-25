# Słownik biznesowy

Pojęcia do rozmów, demonstracji i testów. Reguły otwarte rozstrzygamy w [rejestrze pytań](open-questions.md).

| Pojęcie | Znaczenie w discovery |
| --- | --- |
| Klient | Osoba, do której przypisujemy wspólny rachunek rezerwacji lub pobytu. Dla grupy domyślnie jest to rezerwujący. Recepcja może zmienić przypisanie. Dopasowanie i scalanie profili pozostaje otwarte. [Reguły rachunku](reception-discovery.md#punkt-wyjścia) |
| Rezerwujący | Osoba składająca rezerwację lub wskazana jako jej kontakt. Może dokonać rezerwacji dla innych uczestników. |
| Uczestnik | Osoba korzystająca z pobytu, wejścia, zabiegu lub wydarzenia. Recepcja może przypisać jej pozycję wspólnego rachunku. |
| Płatnik | Osoba lub podmiot dokonujący danej wpłaty. Jeden wspólny rachunek może mieć kilka wpłat od różnych płatników. |
| Oferta i taryfa | Co jest sprzedawane i na jakich warunkach. Uzgodnij cenę i ograniczenia obowiązujące w chwili akceptacji. |
| Zasób i pojemność | Jednostka, osoba, sprzęt lub wspólny limit, od których zależy dostępność. Rozróżniaj rezerwację pojemności od faktycznej obecności. |
| Rezerwacja | Zobowiązanie dotyczące oferty i zasobu lub miejsca w puli. Momenty potwierdzenia, blokady i zwolnienia zależą od oferty. |
| Wizyta lub pobyt | Faktyczne korzystanie z obiektu, np. pobyt noclegowy albo wizyta dzienna bez wcześniejszej rezerwacji. Rezerwacja opisuje zamówienie, a wizyta odnotowuje korzystanie z usługi. |
| Rachunek gościa, folio | Wspólny rachunek przypisany do klienta dla danej rezerwacji/pobytu, otwarty przy rezerwacji lub przyjeździe. Łączy pozycje i wpłaty, które mogą powstać przed rozpoczęciem pobytu. Otwarcie rachunku dla wizyty dziennej rozstrzyga D-02. |
| Pozycja i alokacja | Pozycja zwiększa należność. Alokacja określa udział poszczególnych osób w pozycji wspólnego rachunku. Jej zmiana zachowuje sumę pozycji. |
| Wpłata, zaliczka, zwrot | Wpłata zmniejsza saldo do zapłaty, a zaliczka jest jej wariantem. Zwrot ma własny ślad i wymaga uzgodnienia z ewentualną korektą pozycji lub dokumentu. |
| Dokument fiskalny i rozrachunek | Dokument ewidencjonuje zdarzenie zgodnie z właściwą regułą. Rozrachunek operatora potwierdza przepływ środków. Oba mają odrębne statusy i identyfikatory. |
| Sprzedaż, wpływ, przychód i marża | Mierniki wymagające uzgodnienia daty, podstawy i źródła. Uzgodnij moment ujęcia i sposób traktowania zaliczek, zwrotów i kosztów. |
| Zmiana, dostępność do zabiegów, czas pracy | Plan obsady, okno dostępności pracownika do sprzedaży usługi oraz ewidencja rzeczywistej pracy. Każda wartość ma własny proces korekty. |
| PMS, POS, ESOK, OTA | System operacji hotelowych, punkt sprzedaży, elektroniczny system obsługi klienta i zewnętrzny kanał rezerwacji. |

## Model pojęciowy i cykle życia

**Proposed — druga sesja, 2026-11-25.** Poniżej odpowiedzialność oznacza miejsce rozstrzygania sporu o dany fakt. Są to granice biznesowe do porównania z rozwiązaniem własnym lub dostawcą. Cykl opisuje zdarzenia widoczne dla obiektu. Fizyczny zapis, techniczne statusy i właściciel systemu pozostają do późniejszej decyzji.

| Pojęcia i odpowiedzialność | Cykl życia i powiązania | Przypadek kontrolny |
| --- | --- | --- |
| Treść, wariant oferty, taryfa i warunki | Redaktor przygotowuje, publikuje lub wycofuje opis. Sprzedaż wycenia wariant na konkretny termin i liczbę osób. Uzgodnione warunki odnoszą się do konkretnego zakupu. | Czy wycofanie opisu ze strony powinno też zamknąć sprzedaż w innych kanałach? To pytanie dla właściciela. Wcześniej kupiony voucher zachowuje warunki. Co z rozpoczętą płatnością za nocleg, rozstrzyga D-03. |
| Rezerwacja, blokada puli, przydział jednostki | Rezerwacja wiąże opcję i okres; tymczasowa blokada wygasa lub przechodzi w potwierdzenie. Recepcja przydziela jednostkę i może przenieść gościa. Źródło kanałowe wiąże import, zmianę i anulowanie z tą samą rezerwacją. | Rezerwacja z OTA może wymagać rozwiązania z powodu braku miejsca. Potwierdzenie nie może wymusić nakładających się przydziałów. |
| Zasób, usterka, gotowość i pobyt | Obiekt wyłącza jednostkę z użycia na okres; sprzątanie aktualizuje gotowość. Recepcja rejestruje zameldowanie i wymeldowanie. | Brudna jednostka daje ostrzeżenie. Wymeldowanie rozpoczyna potrzebę sprzątania nawet przy otwartym rachunku. |
| Pakiet, uprawnienie, bilet, voucher | Zakup określa zakres prawa. Termin, uczestnik i wykonanie są przypisywane osobno. Bilet odwołanego wydarzenia wymaga decyzji obsługi. Voucher kwotowy zachowuje resztę po częściowym użyciu. | Uprawnienie całopobytowe nie zajmuje z góry miejsca w puli. Odwołanie realizacji vouchera wymaga ustalenia skutku dla salda i dokumentu. |
| Wizyta, uczestnik, odcinek czasu i wykonanie zabiegu | Wejście uruchamia obecność. Przy przerwie recepcja wstrzymuje naliczanie i zachowuje miejsce do planowanego końca. Przy masażu recepcja zapisuje uzgodniony termin. Pracownik oznacza wykonanie, a system dopisuje cenę do otwartego rachunku. | Prognoza wyjścia nie kończy wizyty. Dwa oznaczenia wykonania tej samej usługi powinny dać jedną pozycję. |
| Osoba, rola w transakcji i upoważnienie | Rezerwujący, uczestnik i płatnik mogą być trzema osobami. Osoba kontaktowa może zmienić się przed pobytem. Proponowane utrzymanie kontaktu i zgody według celu oraz kanału. | Korekta danych kontaktowych nie zmienia historycznego płatnika. Wyszukanie po telefonie nie upoważnia do scalenia dwóch gości. |
| Zamówienie, rachunek, pozycja, alokacja | POS lub wykonana usługa dostarcza pozycję. Gastronomia może sama przenieść także opłacone zamówienie między otwartymi rachunkami. Recepcja rozdziela należność między osoby i rozlicza rachunek. Alokacja dzieli należność między osoby, zachowując sumę. | Korekta przypisania zapłaconego zamówienia pozostawia ślad rzeczywistej wpłaty. Błąd odkryty po zamknięciu ma własny przebieg w D-02. |
| Wpłata, zwrot, dokument i rozrachunek | Dyspozycja, potwierdzenie i rozrachunek u dostawcy mogą mieć różne daty. Zwrot ma osobny wynik. Dokument oraz jego korekta wskazują zdarzenie podlegające udokumentowaniu. | Ponowne powiadomienie o tej samej wpłacie nie pomniejsza salda drugi raz. Samo zlecenie zwrotu nie zamyka uzgodnienia z operatorem. |
| Zmiana pracownika, faktyczny czas i koszt | Grafik wyznacza plan, wpis zarejestrowany lub poprawiony opisuje pracę. Rozliczenie używa ustalonego okresu i przypisania kosztu. | Korekta pracownika po zamknięciu okresu uruchamia powiadomienie. Jej skutek finansowy wymaga decyzji kadrowej. |
| Gałąź działalności, składowa pakietu, okres i koszt | Finanse przypisują wykonanie oraz uzasadniony koszt do gałęzi według uzgodnionej podstawy. Raport przechodzi od danych źródłowych do sumy okresu z możliwością wyjaśnienia korekty. | Podział ceny pakietu musi dawać jego pełną wartość dokładnie raz. Sprzedaż vouchera i jego realizacja nie mogą podwoić wartości wykonanej usługi. |

[Reguły właściciela i przypadki recepcji](reception-discovery.md) · [Powiązania procesów](../research/platform-workflows.md) · [Rozstrzygnięcia i luki](open-questions.md)
