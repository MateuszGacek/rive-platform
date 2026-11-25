---
type: research
status: proposed
area: "15 Inżynieria i ciągłość działania"
source: "Analiza reguł rivé, OWASP ASVS, dokumentacja operatorów i źródła urzędowe"
created: 2026-11-25
updated: 2026-11-25
---

# Jakość i przywrócenie pracy obiektu

**Proposed · fazy 7 i 11.** Priorytet wynika z możliwej szkody dla gościa i możliwości odzyskania stanu. Poniższe przykłady to kryteria przyszłych prób. Źródła reguł to [procesy domenowe](platform-workflows.md) i [D-02–13](../product/open-questions.md).

| Priorytet i szkoda | Dowód przed produkcją | Sygnał i odpowiedzialność podczas pracy |
| --- | --- | --- |
| 1 · brak noclegu po sprzedaży | Test integracyjny równoległych zapisów WWW i recepcji dla ostatniego miejsca. Powtórzyć z OTA: zachować oba zobowiązania w przypadku konfliktu, fizyczne przydziały pozostają rozłączne. Test kontraktowy duplikatu, zmiany, anulowania i spóźnionego importu. | Wiek ostatniego skutecznego importu, liczba nierozwiązanych konfliktów. Recepcja widzi zagrożone rezerwacje, rozstrzyga indywidualnie. |
| 1 · utrata wpłaty lub podwójne obciążenie | Test przerwania po zapisie, powtórzonego webhooka lub potwierdzenia terminala. Zweryfikować autentyczność powiadomienia, kwotę, walutę i właściwy zakup. Zestawić historię wpłat i korekt z saldem, dokumentem i faktycznym płatnikiem. Sprawdzić jednoczesny zakup za resztę salda vouchera. | Liczba i wiek nieuzgodnionych wpłat/zwrotów. Obsługa widzi wynik niepewny. Zewnętrzną płatność sprawdzić przed ponowieniem. [Przykład właściwości webhooków](https://docs.stripe.com/webhooks) |
| 1 · dostęp do cudzego rachunku, płac lub danych gościa | Testy rola × czynność × zasób dla panelu, API i eksportu. Zablokowane konto nie zachowuje dostępu. Gość może zarządzać tylko swoją rezerwacją. Oddzielić dostęp techniczny, zwroty i odczyt finansów. Ograniczyć czas życia linków gościa i zasady odzyskiwania kont. | Historia autora, czasu i zakresu korekty, zwrotu, eksportu i zmiany uprawnienia. Dostęp do historii ograniczony. Logi bez danych kontaktowych, linków autoryzacyjnych i danych kart. [OWASP ASVS](https://asvs.owasp.org/) |
| 2 · nieprawidłowe koszty lub dostępność | Testy jednostkowe czasu, progów spóźnienia, końca dnia, zaokrągleń i częściowych realizacji. Test integracyjny powtórzenia „wykonano masaż”, konfliktu dopisania pozycji z zamknięciem rachunku. | Zachować źródło pozycji i historię korekty. Wyjątek trafia do odpowiedzialnej roli. Właściciel z księgowością uzgadnia raport na syntetycznym okresie. |
| 2 · sprzedaż lub recepcja niedostępna w szczycie | E2E rezerwacja i wpłata, telefon i „Wejście”, rozliczenie grupy. Sprawdzić słabe połączenie, dotyk/klawiaturę/czytnik, porównanie wizualne krytycznych stanów. Próbę obciążeniową oprzeć o spodziewany szczyt dnia wydarzenia i równoległe żądania ostatniego miejsca. | Opóźnienie zapisu i odczytu, błędy rezerwacji, opóźnienie zadań i ostatnia udana kopia. Ustalić osobę reagującą i progi wg tolerowanego skutku. |

**Model zagrożeń.** Gość i pracownik przekraczają inne granice zaufania. Numer jednostki identyfikuje rachunek w uprawnionym widoku gastronomii. Sam w sobie nie upoważnia do odczytu czy zmiany rezerwacji. Portal, eksport, treści CMS i komunikaty operatorów potrzebują odrębnych uprawnień i walidacji. Dla kont uprzywilejowanych rozważyć MFA, dla załączników i logów minimalizację danych, dla sesji wspólnych urządzeń szybkie przełączenie i wylogowanie. Przed wyborem hostingu ustalić dostęp administratorów, podwykonawców i miejsce przetwarzania.

**Wydanie i łańcuch dostaw.** Preview z syntetycznymi danymi, staging z osobnymi sekretami i kontami testowymi dostawców, produkcja z ograniczonym wdrażaniem i jawną akceptacją. CI ma minimalne uprawnienia. Propozycja: lockfile, weryfikacja zależności i sekretów, przypięte wersje akcji zewnętrznych, testy domenowe, kontraktowe i dostępności odpowiednie do zakresu zmiany. Dla migracji poszerzyć strukturę zgodnie ze starą wersją, sprawdzić zgodność odczytu i kopię, a usuwanie poprzedniego formatu planować oddzielnie. Wycofanie aplikacji nie cofnie pobranej płatności ani wysłanej wiadomości. [GitHub Actions — secure use](https://docs.github.com/en/actions/reference/security/secure-use)

**Procedura do przećwiczenia na izolowanym środowisku.**

1. Określić zakres awarii, osobę decyzyjną i ostatni wiarygodny stan. Wstrzymać niepewne zlecenia i automatyczne wiadomości. Przy braku wiarygodnej dostępności noclegu strona kieruje do recepcji.
2. Dla Day SPA obowiązuje potwierdzony zapis wejść i wyjść na papierze z faktyczną godziną. Recepcja przyjmuje gościa z rezerwacją, którą może sprawdzić, lub bez rezerwacji, jeśli wiarygodnie ocenia obłożenie. Dla noclegów, zamówień i wpłat proponujemy minimalny zapis ręczny z czasem i identyfikatorem do późniejszego uzgodnienia. Właściciel wybiera zabezpieczone miejsce i osobę uprawnioną.
3. Odtworzyć bazę, media, konfigurację i dostęp w izolacji z kopii oddzielonej od podstawowego środowiska. Zmierzyć czas od awarii do obsługi oraz lukę danych. Przy wymaganym odzyskiwaniu do chwili w czasie sprawdzić kopię bazową i historię zmian. [PostgreSQL — PITR](https://www.postgresql.org/docs/current/continuous-archiving.html)
4. Uzgodnić zdarzenia po kopii z rejestrem ręcznym, Booking.com, operatorem i terminalem. Sprawdzić otwarte rachunki, osoby na miejscu, przydziały, wpłaty i vouchery. Przed przełączeniem potwierdzić odcięcie zapisów i wysyłki z poprzedniego środowiska. Na odtworzonym utrzymać wysyłkę wyłączoną do uzgodnienia już wykonanych działań. Kontrolnie wznowić kolejkę po zaakceptowaniu rozbieżności: potwierdzić jedno aktywne źródło zapisu, jedną wpłatę i brak powtórnej wiadomości za zdarzenie już obsłużone. Następnie wznowić sprzedaż. Zapisać czasy, sumy i wyjątki.
5. Przy ewentualnej migracji wykonać próbę dla uzgodnionego zakresu D-12. Porównać identyfikatory, liczby rezerwacji, salda, wpłaty oraz pozostałe prawa voucherów. Przy rozbieżnościach zachować źródło, zatrzymać przełączenie lub uzgodnić nowe operacje przed powrotem. Właściciel chce przeprowadzić migrację samodzielnie.

**Open question — decyzje przed zobowiązaniem technicznym.** Właściciel określa akceptowalną przerwę i utratę danych osobno dla wejść, wpłat oraz treści WWW (RTO/RPO). Porównać tańszą kopię okresową i ręczne wznowienie z odzyskiwaniem do punktu w czasie. Oba warianty wymagają próby odtworzenia. Dla etapu discovery wystarczają dane syntetyczne i przegląd dokumentów.

| Specjalista | Pytanie do rozstrzygnięcia dla rivé | Co zależy od odpowiedzi |
| --- | --- | --- |
| Księgowość / doradca podatkowy | Jak ująć zaliczkę, późną anulację, zwrot, voucher kwotowy/usługowy, pakiet z różnymi usługami, fakturę B2B i B2C? Jak postąpić przy awarii kasy lub KSeF? | Zdarzenie i data dokumentu, korekta, eksport i zakres integracji. [Ministerstwo Finansów — KSeF](https://ksef.podatki.gov.pl/) |
| Prawnik konsumencki | Jak komunikować anulację noclegu i odstąpienie od umowy dla usługi na oznaczony termin oraz vouchera bez terminu? Czy obowiązki dostępności e-handlu dotyczą podmiotu i zakresu sprzedaży? | Warunki zakupu, komunikaty i odbiór dostępności. [UOKiK](https://prawakonsumenta.uokik.gov.pl/prawo-odstapienia-od-umowy/wylaczenia-prawa-do-odstapienia/) · [Polski Akt o Dostępności](https://www.gov.pl/web/dostepnosc-cyfrowa/polski-akt-o-dostepnosci--uslugi-handlu-elektronicznego) |
| Osoba odpowiedzialna za prywatność i kadry | Określić cele, podstawy, dostęp, okresy przechowywania, usuwanie/ograniczenie, umowy z dostawcami oraz reakcję na incydent dla danych gości i pracowników. Osobno ocenić śledzenie i komunikację marketingową. Jak korekta po zamknięciu okresu zmienia wypłatę? | Uprawnienia, eksport, retencja, procedura oceny i ewentualnego zgłoszenia naruszenia, rozliczenie pracy. [RODO](https://eur-lex.europa.eu/eli/reg/2016/679/oj) |

## Wymagania zmieniające granicę systemu · Proposed

| Sytuacja do sprawdzenia | Kryterium i decyzja projektowa |
| --- | --- |
| Sprzedaż biletów generuje szczyt odczytów WWW podczas rozliczania gości na miejscu | Oddzielnie mierzyć czas odpowiedzi publicznego odczytu, zatwierdzenia rezerwacji i zapisu wpłaty w recepcji. Przy degradacji ograniczenie ruchu lub cache opisu ma chronić zapis operacyjny. Dopiero uzgodnione natężenie i akceptowalny czas odpowiedzi pozwolą porównać koszt izolacji. |
| Wspólny tablet przechodzi od recepcji do gastronomii | Po zmianie roli ponownie sprawdzić uprawnienia, także po powrocie do poprzedniego ekranu i przy eksporcie. Poprzednio wyświetlony rachunek i dane płacowe nie mogą wrócić z lokalnego cache. Właściciel rozstrzyga model pracy na współdzielonych urządzeniach. |
| Zmiana strony lub kalendarza w piątek przed wydarzeniem | Osoba odpowiedzialna za utrzymanie powinna móc odróżnić błąd treści, błąd odczytu dostępności i błąd zapisu. Dla każdego wskazać ostatni poprawny wynik i bezpieczną czynność: cofnięcie publikacji, przejście na kontakt lub sprawdzenie zapisu. Próg alarmu ustalić względem utraconej możliwości sprzedaży i obsługi gości. |
