# Pytania i decyzje discovery

Poniższe tematy zawierają otwarte pytania i odnotowane rozstrzygnięcia. Po decyzji zaktualizuj [mapę możliwości](capability-map.md) i [notatki z decyzji](../decisions/README.md) tam, gdzie zmieniają się zakres lub sposób dostawy. Ustalenia właściciela wpisz do [notatek discovery](../discovery.md). Dowody z rozmów i demo zapisuj w formie zanonimizowanej.

[Roadmapa projektu](../PROJECT-ROADMAP.md) określa kolejność rozstrzygania zagadnień. [Scenariusze recepcji](reception-discovery.md) służą do analizy domeny i późniejszych prób zatwierdzonej dostawy. Demonstracje i porównanie kosztów w D-13 stosuj przy decyzji o dostawcy lub integracji.

## D-01

**Pierwsza dostawa.** Jaki zakres i kryteria odbioru zatwierdzi właściciel w fazie 9?

- **Ustalono — właściciel, 2026-11-24.** Do pierwszej próby wybrano pełną zwykłą wizytę Day SPA od rezerwacji telefonicznej albo przyjęcia gościa bez rezerwacji do zapłaty. **Korekta kierunku, 2026-11-25.** Zachowujemy ten przebieg jako przykład domeny. Wybór zakresu pierwszej dostawy wraca do fazy 9. [Plan pracy](agent-delivery-plan.md#1-praca-w-ramach-roadmapy)
- **Ustalono — korekta właściciela, 2026-11-24.** W odbiorze pilota Day SPA sprawdzamy prostotę obsługi i samodzielne wykonywanie rutynowych czynności przez system. Właściciel wycofał wcześniejszy wybór miernika czasu obsługi. Pomiar bazowy i próg w sekundach nie są wymagane.

- **Powiązane karty** — OPS-05, OPS-06, BKG-02, WEB-05, HR-01.
- **Rozstrzyga** — Właściciel.
- **Kiedy** — W fazie 9 po uzgodnieniu fundamentów platformy. Scenariusze domenowe można stosować wcześniej do sprawdzania zależności.
- **Dowód** — Wybrany przebieg oraz próba pokazująca, które czynności wykonuje recepcja, które wykonuje system i kiedy potrzebna jest decyzja pracownika.

## D-02

**Recepcja i POS.** Jak anulujemy błędną pozycję i obsługujemy ponowienie zapisu z POS? Ustal zdarzenia przyjazdu i wyjazdu dla noclegów oraz rozdziel zamknięcie rachunku od uzgodnienia całej zmiany.

- **Ustalono** — [rozliczenie wizyty dziennej osobno lub na wspólnym rachunku](reception-discovery.md#reguły-oferty-dostępności-i-rozliczenia).
- **Ustalono — właściciel, 2026-11-24.** Rachunek grupy domyślnie przypisujemy do osoby rezerwującej. Recepcja może zmienić przypisanie. [Zasady wspólnego rachunku](reception-discovery.md#punkt-wyjścia)
- **Ustalono — właściciel, 2026-11-24.** Recepcja może zmienić przypisanie opłaconej pozycji. System zachowuje faktycznego płatnika i kwotę wpłaty oraz pokazuje nowe dopłaty lub nadpłaty. [Zasady wspólnego rachunku](reception-discovery.md#punkt-wyjścia)
- **Ustalono — właściciel, 2026-11-24.** Wspólny rachunek zamykamy po rozliczeniu uzgodnionych dopłat i zwrotów. Wymeldowanie może nastąpić przy otwartym rachunku. [Zasady wspólnego rachunku](reception-discovery.md#punkt-wyjścia)
- **Ustalono — właściciel, 2026-11-24.** Dwa pobyty jednego klienta domyślnie mają odrębne rachunki. Recepcja może je połączyć, dopóki oba są otwarte, także po wpłacie. System zachowuje faktycznych płatników i kwoty wpłat. [Zasady wspólnego rachunku](reception-discovery.md#punkt-wyjścia)
- **Ustalono — właściciel, 2026-11-24.** System dodaje cenę noclegu do rachunku w momencie potwierdzenia rezerwacji. [Zasady wspólnego rachunku](reception-discovery.md#punkt-wyjścia)
- **Ustalono — właściciel, 2026-11-24.** Gastronomia może poprawić przypisanie zamówienia do otwartego rachunku również po zapłacie. System zachowuje faktycznego płatnika i kwotę wpłaty. [Zasady wspólnego rachunku](reception-discovery.md#punkt-wyjścia)
- **Powiązane karty** — OPS-01–OPS-09, POS-02, POS-03.
- **Rozstrzyga** — Właściciel po przejściu procesu z recepcją.
- **Kiedy** — Na początku warsztatu recepcji, przed opisaniem oczekiwanych wyników demo.
- **Dowód** — Przykłady: solo, para/grupa, gość dzienny, zakup gastronomiczny opłacony od razu i dopisany do folio. Dla każdego oczekiwane pozycje, alokacje i saldo.

## D-03

**Oferta, strona, booking.** Skąd strona bierze dostępność i gdzie kończy się proces zakupu? Które różnice między jednostkami wpływają na ofertę, dostępność puli lub możliwość zmiany przydziału? Kiedy blokujemy zasób, wygaszamy rezerwację i obsługujemy zmianę, anulowanie lub no-show? Jakie taryfy mają pierwszeństwo i co zachowujemy z zaakceptowanej ceny? Sprawdź na tych samych danych zmianę ceny przed i po potwierdzeniu, anulowanie i no-show.

- **Ustalono** — [rezerwację typu noclegu z przydziałem jednostki przez recepcję i potwierdzenie noclegu po zaliczce](../discovery.md#wywiad-z-właścicielem--oferta-noclegowa-2026-11-19).
- **Ustalono — właściciel, 2026-11-24.** Osoba z uprawnieniem do publikowania może samodzielnie edytować treści ofert i wydarzeń, sprawdzać podgląd i publikować.
- **Ustalono — właściciel, 2026-11-24.** Formularz kontaktowy wysyła wiadomość na wspólną skrzynkę recepcji. Pracownik odpowiada gościowi z tej skrzynki.
- **Powiązane karty** — WEB-01–WEB-05, CAT-01, CAT-02, BKG-01–BKG-06.
- **Rozstrzyga** — Właściciel z recepcją i osobą odpowiedzialną za sprzedaż.
- **Kiedy** — Przed przygotowaniem scenariuszy rezerwacji i taryf.
- **Dowód** — Macierz typów ofert z przykładami cen, ograniczeń, momentem rezerwacji i zwolnienia. Próba ostatniego miejsca z telefonu i internetu. Zatwierdzona ścieżka redakcyjna i odbiorca kontaktu.

## D-04

**SPA, eventy i vouchery.** Jak rozliczyć korektę pomiaru po zamknięciu rachunku i powiązać ją z dokumentem? Dla pierwszego pakietu czterogodzinnego dopłata za dodatkowy czas jest minutowa; przy przedłużeniu obowiązują ustalone ostrzeżenie i decyzja recepcji. Jak chwilowe wyjście działa w pakiecie z jednym wejściem? Czy pakiet gwarantuje wszystkie terminy? Jak ośrodek obsługuje realizację voucherów i zmianę liczebności wydarzenia?

- **Ustalono** — [jedna strefa wejścia dla całego ośrodka, reguły obecności i naliczania czasu](reception-discovery.md#reguły-oferty-dostępności-i-rozliczenia), [spóźnienie](reception-discovery.md#spóźnienie-na-zarezerwowane-wejście) i [chwilowe wyjście z wizyty dziennej](reception-discovery.md#chwilowe-wyjście).
- **Ustalono — właściciel, 2026-11-24.** Vouchery kwotowe można wykorzystywać w częściach. Kupiony voucher zachowuje warunki zakupu. Strona i recepcja sprzedają vouchery z tej samej oferty. [Ustalenia o ofercie](../discovery.md#oferta-i-dalszy-rozwój--2026-11-20)
- **Ustalono — właściciel, 2026-11-24.** Pierwsza wersja wydarzeń umożliwia zakup biletu na stronie i otrzymanie potwierdzenia. [Ustalenia o ofercie](../discovery.md#oferta-i-dalszy-rozwój--2026-11-20)
- **Ustalono — właściciel, 2026-11-24.** Wydarzenie ma własny limit biletów. Obsługa może zmniejszyć pulę Day SPA lub zarezerwować ośrodek na wyłączność. [Ustalenia o ofercie](../discovery.md#oferta-i-dalszy-rozwój--2026-11-20)
- **Ustalono — właściciel, 2026-11-24.** Ograniczenie puli działa dla nowych rezerwacji od razu. Potwierdzone rezerwacje pozostają ważne, a kolizje trafiają do obsługi przez recepcję. [Ustalenia o ofercie](../discovery.md#oferta-i-dalszy-rozwój--2026-11-20)
- **Ustalono — właściciel, 2026-11-24.** Po odwołaniu wydarzenia obsługa rozpatruje opłacone zakupy indywidualnie, uzgadniając np. zwrot lub przeniesienie. [Ustalenia o ofercie](../discovery.md#oferta-i-dalszy-rozwój--2026-11-20)
- **Powiązane karty** — EVT-02–EVT-06, OPS-06.
- **Rozstrzyga** — Właściciel po obserwacji pracy recepcji i SPA.
- **Kiedy** — Przed testowaniem dopłat, zasobów i voucherów na demo.
- **Dowód** — Obserwacja wejścia i wyjścia, przykłady graniczne z oczekiwaną kwotą, macierz usług i zasobów, demo ESOK na recepcji oraz próba pakietu z niedostępną składową.

## D-05

**Gość i komunikacja.** Jak rozróżniamy gościa, rezerwującego, uczestnika i płatnika? Kiedy profil jest potrzebny? Kto rozstrzyga duplikaty? Które komunikaty są transakcyjne, a które marketingowe?

- **Ustalono** — [potwierdzenie telefoniczne wejścia i wymagane dane](reception-discovery.md#potwierdzenie-rezerwacji-przez-www). Reguły rezerwacji bez konta i e-maili dotyczą odłożonej samoobsługi WWW.
- **Powiązane karty** — CRM-01, CRM-02, INT-05.
- **Rozstrzyga** — Właściciel z recepcją.
- **Kiedy** — Przed wyborem danych gościa i kanałów dla pilota.
- **Dowód** — Przykłady z dwiema osobami o tym samym nazwisku, rezerwacją dla innej osoby i zmianą pokoju. Zatwierdzona lista komunikatów, źródeł danych i dowodów doręczenia.

## D-06

**Personel.** Jak oddzielić zmianę, dostępność do zabiegu, rzeczywisty czas i rozliczenie wynagrodzenia? Co przy nocnej zmianie, absencji i zastępstwie? Jak uwzględnić korektę zamkniętego okresu w rozliczeniu wynagrodzeń?

- **Ustalono — właściciel, 2026-11-24.** Przyciski „Rozpocznij” i „Zakończ” uzupełniają godziny pracy automatycznie. Pracownik może poprawić godzinę rozpoczęcia lub zakończenia albo wpisać cały przedział ręcznie. Obsługa ma być szybka i intuicyjna. Próba: pracownik rozpoczyna pracę o 08:00, a włącza rejestrację o 08:25. Może ustawić faktyczny początek na 08:00.
- **Ustalono — właściciel, 2026-11-24.** W otwartym okresie pracownik sam zapisuje i poprawia własne wpisy. Kierownik może w razie potrzeby sprawdzić historię zmian.
- **Ustalono — właściciel, 2026-11-24.** Po zamknięciu okresu pracownik może sam poprawić własny wpis. System informuje kierownika o zmianie i zachowuje historię. Wpływ na zakończone rozliczenie wynagrodzeń pozostaje do uzgodnienia.
- **Powiązane karty** — HR-01–HR-06.
- **Rozstrzyga** — Właściciel z osobą odpowiedzialną za kadry.
- **Kiedy** — Przed specyfikacją grafiku, czasu i kalkulacji wynagrodzeń.
- **Dowód** — Anonimowe przykłady grafików i korekt. Uzgodnienie celu ewidencji, zasad eksportu i zakresu wewnętrznej kalkulacji z osobą odpowiedzialną za kadry.

## D-07

**Obiekt.** Kto oznacza gotowość pokoju, tworzy zadanie i zamyka usterkę? Czy dany status blokuje wydanie, sprzedaż albo oba?

- **Ustalono — właściciel, 2026-11-24.** Przy zakładaniu blokady recepcja wybiera automatyczne wygaśnięcie albo ręczne potwierdzenie zdjęcia blokady. [Gotowość noclegu](../discovery.md#gotowość-noclegu--2026-11-20)
- **Powiązane karty** — FAC-01, FAC-02, BKG-02, OPS-08.
- **Rozstrzyga** — Właściciel z recepcją i osobą odpowiedzialną za obiekt.
- **Kiedy** — Przed uzgodnieniem reguł dostępności i wydania pokoju.
- **Dowód** — Przejście od wymeldowania do ponownego wydania pokoju oraz awaria przy istniejącej rezerwacji.

## D-08

**Wpłaty, dokumenty i prawo.** Jakie statusy i dokumenty towarzyszą zaliczce, częściowej wpłacie, zmianie, anulowaniu i zwrotowi? Jak uniknąć powtórnego rozliczenia, gdy potwierdzenie operatora nadejdzie po wygaśnięciu blokady? Kto przyjmuje płatność, wystawia dokument i obsługuje wyjątek?

- **Confirmed — doprecyzowanie indeksu, 2026-11-25.** Recepcja wybiera moment dopłaty i potwierdza zwykły przelew po sprawdzeniu wpływu. Po terminie może przywrócić rezerwację tylko gdy nadal ma dostępność. Recepcja ręcznie zleca należny zwrot; potwierdzenie wykonania i dokumenty pozostają otwarte.
- **Ustalono** — [wysokość zaliczki, terminy wpłaty i dostępne momenty dopłaty za nocleg](../discovery.md#wywiad-z-właścicielem--oferta-noclegowa-2026-11-19).
- **Ustalono — właściciel, 2026-11-24.** Przy podziale rachunku recepcja wybiera, czy zaliczka pomniejsza wspólne saldo do podziału, czy część wskazanej osoby. [Zasady wspólnego rachunku](reception-discovery.md#punkt-wyjścia)
- **Ustalono — właściciel, 2026-11-24.** W pierwszej wersji wynik płatności kartą pracownik sprawdza na terminalu i potwierdza ręcznie w panelu. Integracja terminala jest odłożona. [Zasady wspólnego rachunku](reception-discovery.md#punkt-wyjścia)
- **Powiązane karty** — OPS-03, OPS-04, OPS-07, OPS-09, POS-03, PAY-01, PAY-02, INT-01, INT-02.
- **Rozstrzyga** — Właściciel dla procesu, księgowość dla kwalifikacji i dokumentów.
- **Kiedy** — Po opisaniu wariantów wizyty i rachunku, przed oceną rozliczeń na demo.
- **Dowód** — Z księgowością uzgodnić skutki scenariuszy B2C/B2B, kasy, KSeF, VAT pakietów, opłaty miejscowej i GUS. Potem pokazać je na właściwym urządzeniu lub sandboxie dostawcy.

## D-09

**Finanse.** Jak definiujemy sprzedaż, obrót, przychód, wpływy, koszt, marżę i zysk? Brutto czy netto? Która data i źródło? Jak traktujemy vouchery, zwroty i koszty wspólne? Czy raport wykorzystania zasobów ma uzasadniony mianownik? Kto rozstrzyga rozbieżności wykryte przy porównaniu wpłat i zwrotów z danymi źródłowymi?

- **Ustalono — właściciel, 2026-11-24.** Panel udostępnia raport wpłat według metod. Personel porównuje go z gotówką i raportem terminala w razie potrzeby. Porównanie nie jest wymaganym krokiem zamknięcia zmiany ani dnia.
- **Powiązane karty** — FIN-01–FIN-06, OPS-09.
- **Rozstrzyga** — Właściciel z księgowością.
- **Kiedy** — Po ustaleniu zdarzeń z D-08, przed odbiorem raportu i zamknięcia zmiany.
- **Dowód** — Jeden okres z syntetycznymi dokumentami, wpłatami i kosztami. Suma i rozbicie kategorii uzgodnione z księgowością oraz menedżerem.

## D-10

**Dostęp.** Kto widzi rachunek, może dopisać lub skorygować pozycję, alokować ją, zwracać wpłaty, zamykać rachunek, eksportować raport i oglądać czas lub płace?

- **Ustalono — właściciel, 2026-11-24.** Gastronomia widzi dane potrzebne do rozpoznania rachunku, zamówienia gastronomiczne i ich status płatności. [Widok gastronomii](reception-discovery.md#punkt-wyjścia)
- **Powiązane karty** — IAM-01–IAM-05, OPS-03, OPS-07, HR-05, DAT-02.
- **Rozstrzyga** — Właściciel z osobami odpowiedzialnymi za operacje i dane.
- **Kiedy** — Przed specyfikacją uprawnień i próbą audytu.
- **Dowód** — Macierz rola × operacja × zakres danych. Próby dozwolone i odmowy także w API oraz eksporcie.

## D-11

**Dostawcy i integracje.** Jakie systemy, urządzenia, umowy i kanały już działają? Kto rozstrzyga o dostępności, cenie, rachunku, płatności i dokumencie? Czy wykupiony plan daje potrzebne API, zdarzenia, środowisko testowe, SLA i pełny eksport?

- **Ustalono — właściciel, 2026-11-24.** Od startu sprzedaży noclegów uwzględniamy trzy kanały: stronę rivé, recepcję i Booking.com. Booking.com jest pierwszą integracją kanału sprzedaży. Platforma ma pozwalać dodać kolejne integracje. Sposób połączenia pozostaje do decyzji.
- **Ustalono — właściciel, 2026-11-24.** Na start rivé importuje z Booking.com rezerwacje, zmiany i anulowania. Obsługa aktualizuje ceny oraz dostępność na Booking.com ręcznie.
- **Ustalono — właściciel, 2026-11-24.** rivé i Booking.com sprzedają ze wspólnej puli aktualizowanej ręcznie. Konflikt trafia do rozstrzygnięcia przez recepcję. Próba: oba kanały sprzedają ostatnie miejsce przed aktualizacją. Panel pokazuje rezerwacje do rozwiązania, a przydziały jednostek nadal nie mogą się nakładać.
- **Ustalono — właściciel, 2026-11-24.** Gdy nie ma wolnego noclegu zastępczego, panel pokazuje recepcji obie rezerwacje i godziny potwierdzenia. Recepcja rozstrzyga każdy przypadek indywidualnie, bez automatycznego pierwszeństwa kanału lub godziny.
- **Powiązane karty** — INT-01–INT-06, CRM-01, PAY-02, ENG-03.
- **Rozstrzyga** — Właściciel na podstawie demonstracji i potwierdzeń dostawcy.
- **Kiedy** — Przed porównaniem sposobów dostawy w D-13.
- **Dowód** — Inwentaryzacja, ten sam skrypt demo dla kandydatów, test powtórzenia i opóźnienia danych oraz porównywalne oferty.

## D-12

**Dane.** Jak przy ewentualnej migracji sprawdzamy przeniesione rezerwacje, salda, wpłaty i vouchery? Gdzie są dane wrażliwe, kto ma dostęp i ile trwa retencja?

- **Ustalono — właściciel, 2026-11-24.** Jeśli będzie potrzebna migracja, obejmie przyszłe rezerwacje, otwarte rachunki wraz z wpłatami oraz ważne niewykorzystane vouchery, jeśli takie dane istnieją. Właściciel chce spróbować przeprowadzić ją samodzielnie w przyszłości.
- **Powiązane karty** — DAT-01, DAT-02, INT-06, ENG-02.
- **Rozstrzyga** — Właściciel z osobą odpowiedzialną za dane i operacje.
- **Kiedy** — Przed ustaleniem zakresu eksportu, migracji i dostępu do danych.
- **Dowód** — Spis przepływów i zasady dostępu. Jeśli migracja będzie potrzebna, sprawdzony eksport oraz próbna migracja syntetyczna z raportem rozbieżności i planem wycofania.

## D-13

**Ciągłość i architektura.** Co personel zapisuje przy awarii i kto rozstrzyga konflikty po wznowieniu? Jaką przerwę i utratę danych akceptujemy? Gdzie zakup, konfiguracja, integracja lub własny kod mają uzasadnienie?

- **Powiązane karty** — ENG-01–ENG-03, INT-06, DAT-01.
- **Rozstrzyga** — Właściciel na podstawie wyników demo i analizy kosztów.
- **Kiedy** — Przed decyzją o architekturze produkcyjnej, zakupie lub integracji, stosownie do zakresu decyzji.
- **Dowód** — Dla uruchomienia: próba ręcznego działania, odtworzenia i uzgodniona odpowiedzialność za dane. Dla dostawcy: wynik próby i porównanie kosztów, jeśli rozważamy zakup lub integrację.

## Kolejność decyzji właściciela · Proposed, 2026-11-25

Ta kolejność dotyczy zależności projektowych. Stan wykonania i zadania pozostają w Issues. Rekomendacje służą do wyboru, a księgowość i prawnik weryfikują kwestie swojej specjalizacji. [Scenariusze porównawcze](../research/platform-workflows.md) · [Ryzyka i konsultacje](../research/quality-and-recovery.md)

**Proposed — po drugiej sesji.** Uszczegółowiono wcześniejsze sześć tematów, aby każda odpowiedź rozstrzygała jedną decyzję. Pozycje 1–7 porządkują granice biznesowe w fazie 2. Właściciel może świadomie odłożyć temat wraz z konsekwencją. Zakup usługi i wybór stacku mają osobne bramki.

| Kolejność i decyzja | Rekomendacja | Alternatywa i jej konsekwencja | Zależności / kto potwierdza |
| --- | --- | --- | --- |
| 1 · D-09 · Co przypada na miesiąc? | **A.** Dwa widoki: usługi wg wykonania i pieniądze wg rzeczywistej wpłaty lub zwrotu. Korekty domyślnie w miesiącu uznania z odnośnikiem do usługi. | **B.** Pokazywać także poprzedni okres po przeliczeniu. Poprawia porównania ekonomiczne, wymaga zachowania pierwotnie opublikowanej wersji. **C.** Okres zgodny wyłącznie z księgowością, możliwe opóźnienie informacji operacyjnej. | Właściciel wybiera punkt widzenia zarządczego na [przykładzie XI–I](../research/platform-workflows.md#od-zaliczki-do-wyniku-gałęzi). Księgowość osobno ustala podstawę i dokumenty D-08. |
| 2 · D-04/09 · Gdzie wykazać sprzedaż pakietu i koszty? | **A.** Rozdzielać cenę wg wiarygodnych cen osobnych. W panelu gałęzi pokazywać jej własne koszty, koszty wspólne na poziomie obiektu. | **B.** Przy braku podstawy wydzielić „Pakiety”. **C.** Przypisywać też koszty wspólne zatwierdzonym kluczem. Wynik działu zależy wtedy od jakości tego klucza. B dotyczy sprzedaży i może współistnieć z C. | Po 1. Właściciel z księgowością ustala podstawy i definicję wykonania dostępu całopobytowego. |
| 3 · D-03/11 · Jak chronimy cenę podczas płatności? | **A.** Wycenę z przyjętego formularza zachować do wygaśnięcia blokady. Po jej wygaśnięciu pokazać aktualne warunki i poprosić o akceptację. | **B.** Wycena zmienna do chwili rozpoczęcia płatności wymaga ponownego pokazania kwoty przed obciążeniem. W obu wariantach późny wynik operatora wymaga uzgodnienia z faktyczną wpłatą. | Właściciel zatwierdza obietnicę gościowi. Własny katalog lub PMS muszą potrafić wykazać zaakceptowane warunki. Wybór produktu później. |
| 4 · D-02/08/10 · Błąd POS po zamknięciu rachunku | **A.** Powiązana korekta z historią, obsługiwana przez uprawnioną recepcję; wskazana rola uzgadnia wyjątek dokumentowy. | **B.** Kierownik zatwierdza każdą korektę zamkniętego POS. Większa kontrola, wolniejsza obsługa. | Uprawnienia i dokumenty uzgadniają właściciel i księgowość. Oba warianty zachowują ustaloną samodzielną korektę i zlecenie zwrotu za pominięte wyjście SPA. |
| 5 · D-04 · Co gwarantuje retreat? | **A.** Sprzedawać stały program z terminami składowych, jeśli można zarezerwować cały komplet. | **B.** Pakiet z elementami umawianymi później. Łatwiejsza sprzedaż, potrzeba jasnej informacji i obsługi braku terminu. **C.** Odłożyć sprzedaż retreatu i pozostawić kontakt z obsługą. | Właściciel określa obietnicę. Odpowiedź wpływa na ofertę publiczną, dostępność zasobów, zwrot i pozycję 2. |
| 6 · D-05/10/12 · Do czego uprawnia identyfikacja gościa? | **A.** Rozdzielić wyszukanie, powiązanie profilu i dostęp do konkretnej rezerwacji. Przy niejednoznaczności ręczny wybór w zakresie roli. | **B.** Konto obejmujące wiele pobytów. Ułatwia powroty, wymaga potwierdzenia relacji do każdego pobytu, cofania dostępu i reguły dla wspólnego rachunku. | Przed określeniem granic CRM i portalu. Właściciel wskazuje czynności gościa, osoba ds. prywatności ocenia zakres danych i retencję. |
| 7 · D-11/13 · Co obiekt musi obsłużyć w trakcie awarii? | **A.** Najpierw przywracać recepcję, wejścia i wpłaty; WWW pokazuje odczytywalne treści i kontakt. Właściciel podaje dopuszczalną przerwę oraz lukę w zapisach oddzielnie. | **B.** Zachować także sprzedaż online przy awarii części operacyjnej. Większy koszt i potrzeba źródła wiarygodnej dostępności w obu trybach. | Decyzja wpływa na warunki zakupu, odtworzenie i topologię. Dostępność opcji OTA i eksport potwierdza dostawca. |
| 8 · fazy 3–4 · Czy oddzielać wdrożenia? | **A.** Najpierw porównać jedno wdrożenie z niezależną publikacją treści i ograniczeniami dostępu. | **B.** Oddzielić WWW od panelu przy potwierdzonej potrzebie niezależnej dostępności lub cyklu zmian. Dwa wdrożenia wprowadzają obsługę różnych wersji kontraktu. | Po 3, 6 i 7 oraz po akceptacji fazy. Dopiero potem porównywać technologie, hosting, rozwiązanie CMS i kompetencje utrzymującego. |

**Do właściwych specjalistów.** Kadry określają okres skutku poprawki godzin po rozliczeniu. Osoba ds. prywatności i właściciel zatwierdzają podstawy, minimalny zakres eksportu i okresy retencji. Księgowość kwalifikuje zaliczki, wykonanie, vouchery, dokumenty i korekty. Przy braku odpowiedzi odłożyć automatyczny eksport lub szczegółowy raport, wskazując właściciela otwartej decyzji. [D-06](#d-06) · [D-08](#d-08) · [D-12](#d-12)
