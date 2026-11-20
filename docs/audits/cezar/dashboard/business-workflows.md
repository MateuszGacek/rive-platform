# Procesy biznesowe i zależności

Statusy opisują dowód o istniejącym panelu. OBSERVED_READ_ONLY oznacza obserwację struktury. INFERRED oznacza hipotezę wynikającą z częściowego dowodu. UNKNOWN oznacza brak danych do rozstrzygnięcia. BLOCKED_WRITE oznacza, że test przebiegu wymagałby zapisu.

| ID | Proces | Status | Ustalenie lub brakujący dowód |
| --- | --- | --- | --- |
| W-01 | Rezerwacja noclegu | BLOCKED_WRITE | Historyczna lista nie dokumentuje przyjęcia i potwierdzenia rezerwacji ani przydziału pokoju. |
| W-02 | Przyjazd gościa | UNKNOWN | Przejście od rezerwacji do pobytu i gotowości pokoju. |
| W-03 | Rozpoczęcie wizyty dziennej | UNKNOWN | Wejście, początek naliczania i wpływ na pojemność. |
| W-04 | Powiązanie zakupu z rachunkiem | UNKNOWN | Wybór rachunku, korekta i ślad powiązania. |
| W-05 | Rozliczenie wizyty | UNKNOWN | Saldo, płatność częściowa, dokument i zwrot. |
| W-06 | Praca recepcji | INFERRED | Lista może wspierać przegląd rezerwacji. Przypisanie do roli jest niepotwierdzone. |
| W-07 | Zmiana grafiku | UNKNOWN | Dostęp roli oraz wpływ zmiany na obsadę i usługi. |
| W-08 | Sprzedaż produktu lub usługi | UNKNOWN | Związek między taryfą, pozycją sprzedaży i rachunkiem. |
| W-09 | Generowanie raportów | UNKNOWN | Parametry, wynik, ślad wykonania i uprawnienia. |
| W-10 | Uzgodnienie finansów | UNKNOWN | Sposób porównania pozycji, wpłat, zwrotów i dokumentów. |
| W-11 | Odczyt struktury widoków rezerwacji | OBSERVED_READ_ONLY | Historyczna lista i główny widok, ponownie sprawdzone na osobnych listach (EV-11). |

**Open question.** Nagłówki tabeli wskazują rodziny informacji. Relacje danych między rezerwacją, gościem, terminem i zasobem nie zostały potwierdzone. Powiązania pobyt–rachunek, wizyta–obecność i pozycja–wpłata–dokument wymagają osobnych przykładów. [Słownik pojęć rivé](../../../product/business-glossary.md)

## Fragmenty procesu widoczne w EV-11

- Przegląd rezerwacji obejmuje kilka list i widoków datowych. Przełączenie zakładki potwierdzono. Zmiana stanu rezerwacji pozostaje ACTION_NOT_EXECUTED.
- Rachunek jest prezentowany razem z usługami i sumą. Rezerwacje prezentują gościa oraz termin, a katalog zestawia cenę i kategorię z produktem. Te układy UI nie rozstrzygają, jak rekordy wiążą się między ekranami.
- Ewidencja pracowników i sprzątanie mają własne ekrany. Zależność gotowości pokoju od zadań i przyjazdu pozostaje UNKNOWN.

<!-- EV-12 START -->
## EV-12 — przykłady przejść i ograniczenia

Potwierdzono 2 przejścia z listy rezerwacji do innych już udokumentowanych ekranów: katalog produktów, raport kasowy. Dowody opisują nawigację menu i zmianę stanu lokalnych zakładek. Reguły zmiany statusów, wyliczenie rachunku i relacje encji pozostają otwarte.
<!-- EV-12 END -->
