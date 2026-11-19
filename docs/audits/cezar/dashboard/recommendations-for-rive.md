# Pytania do zweryfikowania w rivé

Poniższe propozycje odnoszą się do przyszłego warsztatu i decyzji produktowych. Obserwacja obecnego panelu nie zmienia zatwierdzonych reguł dotyczących wejść czasowych, rozliczeń wizyt dziennych i potwierdzania rezerwacji noclegu po zaliczce. [Pytania i decyzje](../../../product/open-questions.md)

| ID | Proposed | Istniejący zakres rivé |
| --- | --- | --- |
| RIV-01 | Uzgodnić słownik stanów rezerwacji dla telefonu i internetu. W scenariuszu syntetycznym oddzielić rezerwację miejsca w puli, przydział konkretnego pokoju, gotowość przed wydaniem i potwierdzenie po zaliczce. | BKG-01–06, OPS-08, FAC-02, CAT-01/02, D-03 |
| RIV-02 | Przejść syntetyczną wizytę dzienną. Oddzielić rezerwację pojemności, obecność, naliczanie czasu i rozliczenie. | EVT-03/05/06, OPS-06, D-04 |
| RIV-03 | Przejść pobyt grupowy z zakupem, dwiema wpłatami i podziałem pozycji. Ustalić właściciela rachunku, możliwość równoległych rachunków i skutki korekty. | OPS-01–09, POS-01–03, PAY-01/02, D-02, D-08 i D-09 |
| RIV-04 | Ustalić wpływ zmiany w grafiku na dostępność usług i na ewidencję faktycznego czasu pracy. | HR-01–06, D-06 |
| RIV-05 | Uzgodnić definicje raportów, źródła danych oraz uprawnienia w układzie rola × operacja × zakres rekordów. Przećwiczyć uzgodnienie na danych syntetycznych. | FIN-01–06, IAM-01–05, INT-01–06, DAT-01/02, D-09–12 |

Do prób recepcji można użyć istniejących przykładów, w tym wizyty dziennej i pobytu grupowego z zaliczką. Do szerszej weryfikacji obecnego panelu potrzebny jest staging lub kopia z danymi syntetycznymi oraz logiem zmian. Na produkcji alternatywą jest serwerowo egzekwowane konto bez zapisu i potwierdzony zakres odczytowy włącznie z działaniami w tle. [Warsztat recepcji](../../../product/reception-discovery.md)

**Proposed.** Na danych syntetycznych porównać widoki robocze rezerwacji i listę rezerwową. Następnie prześledzić, jak cena lub usługa z katalogu staje się pozycją rachunku i jak wpłata wpływa na saldo. Osobno zweryfikować pojemność ośrodka i gotowość zasobu. Odczyt UI pozwala zaplanować te próby bez założenia wspólnego modelu danych.
