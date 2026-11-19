# Pokrycie, dowody i luki

Historyczny inwentarz obejmuje 57 unikalnych kandydatów. Po uwzględnieniu jednego odczytu struktury, 52 pozycje pozostają wykrytymi kandydatami, dwie wyłączono z powodu ryzyka zapisu, jedna jest niesklasyfikowana i jedna poza zakresem. Weryfikacja dostępności tych pozycji pozostaje otwarta. Pięć wcześniejszych widoków testowych i test lokalny MCP nie wchodzą do wyniku produkcyjnego.

| Dowód | Data i typ | Zakres |
| --- | --- | --- |
| EV-01 | 14 listopada 2026, inwentarz i playbook | Wcześniejszy przegląd menu i listy rezerwacji. Kopie Claude i Codexa są identyczne, więc mają wspólne pochodzenie. |
| EV-02 | 15 listopada 2026, przejrzany odczyt struktury | Jeden historyczny widok z dziewięcioma zatwierdzonymi etykietami. Identyfikator odsyła do źródła w prywatnym archiwum audytu. |
| EV-03 | 15 listopada 2026, walidacja syntetyczna | Pięć widoków testowych Explorera. Nie potwierdzono pełnego ograniczenia narzędzi agenta. |
| EV-04 i EV-05 | 19 listopada 2026, walidacja syntetyczna | Osobna instancja przeglądarki i działające MCP. Powtórzono odczyt struktury, Network i Console na stronie lokalnej. |

Wcześniejszy plan pilota miał status „nie uruchomiono”. Późniejszy EV-02 dokumentuje odrębny odczyt. Przesunięcie jednego wpisu z wykrytych do zaobserwowanych wyjaśnia zmianę liczby kandydatów z 53 do 52. Zaliczenie testu osobnej przeglądarki nie rozstrzyga ograniczeń całego zestawu narzędzi agenta.

**Open question.** Skutki otwierania widoków i ich działań w tle, uprawnienia ról, struktura API, integracje, procesy i aktualność historycznej struktury. Potrzebne są udokumentowane warunki bezpiecznej obserwacji, oczyszczony materiał operatora lub test na danych syntetycznych. Brak dowodów na usterki produktu w zakresie tej rundy. [Mapa funkcji](functional-matrix.md)
