# Hotel i SPA — ocena rynku i plan demonstracji

Discovery, 13.11.2026. Materiał wejściowy obejmował raport „rivé – research oprogramowania Hotel & SPA, etap 1”, uzupełniający benchmark segmentów i „Rivé Platform — analiza Discovery v2”. W eksporcie raportu tabele pokrycia i scenariuszy nie mają wierszy. Nie ma wyników demo ani ofert dopasowanych do obiektu. Benchmark służy do przygotowania porównywalnych prób. Ustalenia właściciela są w [notatkach discovery](../discovery.md).

## Co porównać

| Wariant | Kandydaci i rola | Co może zmienić wynik |
| --- | --- | --- |
| A. Zestaw polskich produktów | KWHotel lub Chart, POSbistro, osobny HR, ewentualnie ESOK | Pełny przebieg rachunku grupy i gościa dziennego, obsługa korekt i lokalnych urządzeń. |
| B. Zagraniczny PMS i SPA | Mews z narzędziem SPA, Clock PMS+, HotelTime z Libero. Apaleo jako kandydat na rdzeń z API. | Polska obsługa, dokumenty, koszty partnerów i dostępność API dla konkretnej kombinacji. |
| C. Własny rdzeń | Własne operacje tam, gdzie scenariusze i ekonomia to uzasadniają, z gotowymi usługami płatniczymi, fiskalnymi i dystrybucją tam, gdzie to możliwe. | Czas do pierwszej wartości, testy i utrzymanie reguł, awarie, koszty danych i odpowiedzialność operacyjna. |
| D. Kupiony rdzeń z warstwą rivé | Opcja, gdy kupione systemy przechodzą kluczowe próby, a wybrana luka jest mierzalna i da się ją obsłużyć wspieranym interfejsem. | Porównać obsługę czasową XSol na stanowisku recepcji, proces ręczny i własny kokpit. Mapowanie ID i KPI uzasadniać odrębnie. |

Źródła w pozostałych segmentach dają punkty odniesienia do dalszej kwalifikacji. Cloudbeds, Little Hotelier, RoomRaccoon i NFHotel to kandydaci PMS. Trybe, Book4Time, Zenoti, Booksy i Hoteligy pomagają ocenić SPA. XSol i Gantner dotyczą wejść i kontroli dostępu. Profitroom i Droplabs pomagają ocenić sprzedaż bezpośrednią, pakiety i vouchery. inEwi i Kadromierz są kandydatami do porównania grafiku i ewidencji. Dobór shortlisty zależy od potwierdzonych scenariuszy, sprzętu, dostępności i ofert. Zestawów produktów nie oceniaj na podstawie sumy deklarowanych funkcji osobnych narzędzi.

### Wybrane obserwacje ze źródeł producentów

- XSol opisuje rozliczanie czasu w strefach według odrębnych reguł i instalację na komputerach recepcji. Sprawdź opłaty graniczne, koszty wersji bez bramek, API, folio i dokumenty. [BaseSystem](https://www.basesystem.pl/hotele_i_spa)
- Clock opisuje sesje o stałym starcie z limitami i współdzieloną pojemnością. Trybe prezentuje day passy i sesje. Pokrycie swobodnych wejść z dopłatą, języków i polskich rozliczeń pozostaje do pokazania. [Clock](https://www.clock-software.com/who-its-for/wellness-activity-retreats) · [Trybe](https://try.be/bathhouses)
- Mews i KWHotel opisują KSeF w swoich materiałach. Zweryfikuj edycję, opłaty, konfigurację, potwierdzenia, korekty i obsługę awarii. W Mews dokumentacja Compliance Suite wskazuje brak dedykowanego publicznego API tego dodatku i brak objęcia go SLA Mews. [Mews](https://help.mews.com/s/article/Mews-Compliance-Suite) · [KWHotel](https://kwhotel.com/pl/produkty/ksiegowosc/ksiegowosc-specyfikacja-modulu/)
- POSbistro opisuje połączenie z systemem hotelowym. Na demo sprawdź powiązanie z klientem i pobytem, alokacje grupowe, walk-in, korektę i odzyskanie po awarii. [POSbistro](https://posbistro.com/typ-biznesu/oprogramowanie-dla-restauracji-hotelowej/)
- Integrację z OTA, wspólny identyfikator, przypomnienia, odzyskiwanie nierozliczonych pozycji, pakiety, vouchery i raport wykorzystania gabinetu oceniaj na rzeczywistym problemie i mierniku. Dane z innych branż lub obiektów są wskazówką do pomiaru.

## Wspólny skrypt demo

Na każdej próbie użyj tych samych syntetycznych danych, zapisanych kroków i oczekiwanych wyników uzgodnionych z właścicielem. Wynik ma zawierać wersję, moduły, licencję, sprzęt, kraj, ręczne kroki, ograniczenia i dowód (zanonimizowany zapis, eksport lub identyfikator testu). Status każdej próby uzupełnij jako **brak dowodu**, **deklaracja**, **dokumentacja**, **pokazano** lub **nie spełnia**, wraz z uzasadnieniem. Poniżej są scenariusze, których wyniki pozostają otwarte.

| ID | Próba | Oczekiwany dowód |
| --- | --- | --- |
| S-01 | Rezerwacja grupy z zaliczką, SPA i gastronomią, alokacja w trakcie i zmiana przy rozliczeniu | Jeden rachunek przez pobyt, zgodna suma pozycji, wpłaty i alokacje, ślad korekt. |
| S-02 | Gość dzienny bez noclegu, wejście czasowe przy granicy taryfy, dodatkowy zakup i wyjście | Wynik zgodny z uzgodnionym wariantem rozliczenia, identyfikacja gościa i dowód braku duplikatu. |
| S-03 | Rezerwacja ostatniego pokoju z dwóch kanałów, opóźnienie OTA, zmiana i anulowanie | Wynik kolizji i zwolnienia zasobu, sposób wykrycia i uzgodnienia opóźnionej zmiany. |
| S-04 | Zabieg zależny od terapeuty, gabinetu i sprzętu. Brak zasobu i absencja po sprzedaży | Brak podwójnej blokady, lista dotkniętych wizyt, sprawdzenie zastępstwa i powiadomień. |
| S-05 | Pakiet nocleg + SPA, jeden brakujący termin, voucher i ponowienie realizacji | Zgodne potwierdzenie lub wyjątek, saldo vouchera, brak osieroconej blokady. |
| S-06 | Częściowa wpłata, płatność kilkoma metodami, korekta po wpłacie, zwrot i dokument | Odrębne statusy wpłaty i dokumentu, uzgodnienie rachunku, operatora i księgowości. |
| S-07 | Ręczna obsługa podczas przerwy, powtórzona pozycja POS po wznowieniu | Widoczny stan niepewny, odzyskanie i uzgodnienie każdej pozycji raz. |
| S-08 | Zmiana nocna, nieobecność, korekta czasu i próba odczytu płac przez recepcję | Osobno grafik, praca i dostępność zabiegów. Ślad korekty i odrzucenie odczytu bez uprawnień. |
| S-09 | Gotowość pokoju, usterka, blokada i zwolnienie przy aktywnej rezerwacji | Widoczny wpływ na wydanie i sprzedaż według ustalonych zasad. |
| S-10 | Eksport otwartych rachunków, rezerwacji, wpłat i voucherów oraz raport za okres | Zachowane identyfikatory i ślad korekt. Salda i raport uzgadniają się z dokumentami. |

Do porównania dostawców użyj jednego wiersza na próbę i konfigurację. Krytyczność scenariusza uzgadnia właściciel przed demo.

| Próba | Dostawca, wersja i moduł | Wynik i dowód | Luka i obejście | Koszt i odpowiedzialność |
| --- | --- | --- | --- | --- |
| ID z tabeli powyżej | Konfiguracja testowa i plan handlowy | Status, data, dowód lub brak | Wpływ na pilot, koszt ręcznego kroku | Kto utrzymuje, koszt potwierdzony lub do wyceny |

## Zgodność w Polsce do potwierdzenia przed wyborem rozwiązania

| Temat | Dowód i następny krok |
| --- | --- |
| KSeF | MF opisuje etapy obowiązku. Dla projektu odroczenia sankcji do końca 2027 sprawdzić końcowy tekst, ogłoszenie i datę stosowania. Księgowość kwalifikuje przypadek obiektu oraz faktury B2B, korekty i tryb awaryjny. [MF: zasady KSeF](https://ksef.podatki.gov.pl/ksef-news/zasady-obowiazywania-ksef-i-przepisy-prawne/) · [MF: projekt odroczenia](https://www.gov.pl/web/finanse/rada-ministrow-za-odroczeniem-kar-za-bledy-w-ksef-i-przedluzeniem-odwrotnego-obciazenia-vat) |
| Kasy, VAT i dokumenty | Dla noclegu, gastronomii, wejść, zabiegów, pakietów i voucherów uzgodnić rodzaj dokumentu, moment wystawienia, korekty, tryb awaryjny i właściwe urządzenie lub dostawcę. [MF: kasy rejestrujące](https://podatki.gov.pl/podatki-firmowe/vat/kasy-rejestrujace) |
| Opłata miejscowa | Ustawa zmienia zasady od 1.01.2027 z wyjątkami wskazanymi w akcie. Dla obiektu sprawdzić obowiązującą uchwałę właściwej gminy, stawkę, zwolnienia, zakres rejestru i przekazanie środków. [Dz.U. 2026 poz. 1354](https://isap.sejm.gov.pl/isap.nsf/DocDetails.xsp?id=WDU20260001354) |
| GUS KT-1 | Metodyka opisuje miesięczne sprawozdanie dla obiektów z co najmniej 10 miejscami. Potwierdzić klasyfikację obiektu, okres, formularz i eksport. [Metodyka GUS](https://stat.gov.pl/download/gfx/portalinformacyjny/pl/defaultaktualnosci/5494/15/1/1/zeszyt_metodologiczny_statystyka_turystycznej_bazy_noclegowej.pdf) |
| Czas pracy i prywatność | Potwierdzić zakres formalnej ewidencji z kadrami. Ustalić cel i retencję danych, role dostawców, wymagane umowy oraz zasady dostępu. Ewentualne formularze zdrowotne wymagają osobnej oceny. [Rozporządzenie o dokumentacji pracowniczej](https://isap.sejm.gov.pl/isap.nsf/DocDetails.xsp?id=WDU20180002369) · [RODO](https://eur-lex.europa.eu/eli/reg/2016/679/oj) |

## Koszt i wybór

Porównaj na 3 i 5 lat, w scenariuszu bazowym i niekorzystnym. Suma obejmuje zakup i konfigurację, licencje, sprzęt, migrację, szkolenie, moduły i integracje, prowizje, wiadomości, koszt własnego kodu, utrzymanie, zgodność, obsługę awarii oraz koszt wyjścia z umowy. Własną pracę oszacuj w godzinach z zakresem i źródłem wyceny. Raportowe godziny i stawki są założeniami.

Ocenę korzyści oprzyj na odzyskanej marży, czasie pracy, częstości błędów i konwersji. Zapisz wartości bazowe przed zmianą, unikaj wielokrotnego liczenia tej samej korzyści. Liczby i oferty obiektu trzymaj poza publicznym repo. Jeśli wariant nie przechodzi niezbędnego scenariusza albo brak dowodu dostępu do integracji, zapisz lukę i koszt jej obejścia przed wyborem. Porównanie zamyka [D-11](../product/open-questions.md#d-11) i [D-13](../product/open-questions.md#d-13).
