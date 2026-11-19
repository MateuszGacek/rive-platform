# Pokrycie, dowody i luki

Historyczny inwentarz obejmuje 57 unikalnych kandydatów. Dwa widoki mają częściowo potwierdzoną strukturę: historyczna lista i bieżący widok główny. Pozostało 51 wykrytych kandydatów, dwie pozycje wyłączone z powodu ryzyka zapisu, jedna niesklasyfikowana i jedna poza zakresem. Weryfikacja dostępności pozostaje otwarta. Klasyfikacja nowego wejścia jest niezależna od dowodu struktury: 54 pozycje mają BLOCKED_RISK z powodu nieustalonych skutków otwarcia lub pracy w tle, 2 dotyczą ryzyka zapisu, 1 pozostaje poza zakresem. Nie odnotowano odmowy dostępu. Pięć wcześniejszych widoków testowych i test lokalny MCP nie wchodzą do wyniku produkcyjnego.

| Dowód | Data i typ | Zakres |
| --- | --- | --- |
| EV-01 | 14 listopada 2026, inwentarz i playbook | Wcześniejszy przegląd menu i listy rezerwacji. Kopie Claude i Codexa są identyczne, więc mają wspólne pochodzenie. |
| EV-02 | 15 listopada 2026, przejrzany odczyt struktury | Jeden historyczny widok z dziewięcioma zatwierdzonymi etykietami. Identyfikator odsyła do źródła w prywatnym archiwum audytu. |
| EV-03 | 15 listopada 2026, walidacja syntetyczna | Pięć widoków testowych Explorera. Nie potwierdzono pełnego ograniczenia narzędzi agenta. |
| EV-04 i EV-05 | 19 listopada 2026, walidacja syntetyczna | Osobna instancja przeglądarki i działające MCP. Powtórzono odczyt struktury, Network i Console na stronie lokalnej. |
| EV-07 | 19 listopada 2026, odczyt już otwartej karty | Widok główny, DOM i drzewo dostępności. W DOM nawigacji dopasowano linki do wszystkich 57 pozycji inwentarza. |
| EV-08 | 19 listopada 2026, uzupełnienie DOM | Deklaracje zakładek, pola telefonu i nagłówków oraz zliczenie nierozpoznanych odnośników. Brak nowego przejścia. |
| EV-09 | 19 listopada 2026, analiza statyczna | Sześć już załadowanych skryptów. Mechanizmy ładowania i wywołania HTTP bez przypisania do obsługi kandydujących tras. |
| EV-10 | 19 listopada 2026, test syntetyczny | Natywne przechwytywanie zatrzymało niedopuszczone testowe żądania HTTP w badanej karcie. Do serwera dotarły uzgodnienie WebSocket i żądanie nowego okna. |

EV-02 i EV-07 dokumentują dwa różne widoki z podobną strukturą rezerwacyjną. Obecność linku nie potwierdza dostępności trasy ani skutków otwarcia. Podczas EV-07 nie wykonano przejścia ani odświeżenia. W ciągu około 4,6 sekundy nie zarejestrowano zdarzeń Network. Diagnostyka przeglądarki zwróciła jeden wpis kategorii błędu o nieustalonej przyczynie. Ruch przy wcześniejszym załadowaniu pozostaje nieobserwowany. Drugi przegląd inwentarza, raportów i wcześniejszych testów nie wykazał dowodu skutków otwierania kolejnych widoków. Uzupełnienie DOM nie potwierdziło nowych tras.

**Confirmed.** Klasy statyczne dla 57 pozycji: 0 READ_ONLY_CONFIRMED, 2 LOW_RISK_UNVERIFIED, 3 WRITE_RISK i 52 UNKNOWN. Dwie pozycje z dowodem struktury zachowują ten status wyłącznie dla obserwowanych widoków. Nie potwierdzono gotowej ochrony na produkcji i nie zmieniono kolejki dopuszczonych wejść.

**Open question.** Skutki otwierania widoków i ich działań w tle, uprawnienia ról, struktura API, integracje, procesy i aktualność historycznej struktury. Potrzebne są udokumentowane warunki bezpiecznej obserwacji, oczyszczony materiał operatora lub test na danych syntetycznych. Brak dowodów na usterki produktu w zakresie tej rundy. [Mapa funkcji](functional-matrix.md)
