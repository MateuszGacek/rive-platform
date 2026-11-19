# Pokrycie, dowody i luki

Historyczny inwentarz obejmuje 57 unikalnych kandydatów. Dwa widoki mają częściowo potwierdzoną strukturę: historyczna lista i bieżący widok główny. Pozostało 51 wykrytych kandydatów, dwie pozycje wyłączone z powodu ryzyka zapisu, jedna niesklasyfikowana i jedna poza zakresem. Weryfikacja dostępności tych pozycji pozostaje otwarta. Pięć wcześniejszych widoków testowych i test lokalny MCP nie wchodzą do wyniku produkcyjnego.

| Dowód | Data i typ | Zakres |
| --- | --- | --- |
| EV-01 | 14 listopada 2026, inwentarz i playbook | Wcześniejszy przegląd menu i listy rezerwacji. Kopie Claude i Codexa są identyczne, więc mają wspólne pochodzenie. |
| EV-02 | 15 listopada 2026, przejrzany odczyt struktury | Jeden historyczny widok z dziewięcioma zatwierdzonymi etykietami. Identyfikator odsyła do źródła w prywatnym archiwum audytu. |
| EV-03 | 15 listopada 2026, walidacja syntetyczna | Pięć widoków testowych Explorera. Nie potwierdzono pełnego ograniczenia narzędzi agenta. |
| EV-04 i EV-05 | 19 listopada 2026, walidacja syntetyczna | Osobna instancja przeglądarki i działające MCP. Powtórzono odczyt struktury, Network i Console na stronie lokalnej. |
| EV-07 | 19 listopada 2026, odczyt już otwartej karty | Widok główny, DOM i drzewo dostępności. W DOM nawigacji dopasowano linki do wszystkich 57 pozycji inwentarza. |

EV-02 i EV-07 dokumentują dwa różne widoki z podobną strukturą rezerwacyjną. Obecność linku nie potwierdza dostępności trasy ani skutków otwarcia. Podczas EV-07 nie wykonano przejścia ani odświeżenia. W ciągu około 4,6 sekundy nie zarejestrowano zdarzeń Network. Diagnostyka przeglądarki zwróciła jeden wpis kategorii błędu o nieustalonej przyczynie. Ruch przy wcześniejszym załadowaniu pozostaje nieobserwowany.

**Open question.** Skutki otwierania widoków i ich działań w tle, uprawnienia ról, struktura API, integracje, procesy i aktualność historycznej struktury. Potrzebne są udokumentowane warunki bezpiecznej obserwacji, oczyszczony materiał operatora lub test na danych syntetycznych. Brak dowodów na usterki produktu w zakresie tej rundy. [Mapa funkcji](functional-matrix.md)
