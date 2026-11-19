# Mapa funkcji i struktura widoku

**Confirmed.** W historycznym odczycie interfejsu rezerwacji z 15 listopada 2026 odnotowano nawigację, trzy zakładki, tabelę z pięcioma zatwierdzonymi nagłówkami, edytowalne pole tekstowe i przyciski. Dowód EV-02 zawiera 29 węzłów drzewa dostępności oraz dziewięć zweryfikowanych etykiet.

| Element | Co potwierdza dowód | Co pozostało otwarte |
| --- | --- | --- |
| Zakładki | Dwie zatwierdzone etykiety odnoszą się do oczekiwania i oczekiwania na potwierdzenie. | Aktywna zakładka, trzecia etykieta i kryteria statusów. |
| Tabela | Nagłówki odnoszą się do danych gościa, terminu pobytu, szczegółów, uwag i działań. | Zakres kolumn, typy danych, wiersze, sortowanie i stronicowanie. |
| Pole nawigacji | Widoczne jednowierszowe pole tekstowe opisane jako numer telefonu. | Filtrowanie, wyszukiwanie, walidacja i skutek użycia. |
| Linki i przyciski | Projekcja zawiera siedem linków i osiem przycisków. | Przypisanie do tras i operacji, uprawnienia oraz skutki. |

| ID | Obszar | Pokrycie | Pytania do sprawdzenia |
| --- | --- | --- | --- |
| M-01 | Rezerwacje | Historyczna lista i aktualny główny widok o układzie rezerwacyjnym. | Kanał online i telefoniczny, dostępność, kalendarz, statusy, anulacje i przypisanie pokojów. |
| M-02 | Obsługa ośrodka | UNKNOWN | Wejścia, pojemność, naliczanie czasu, strefy i pakiety. |
| M-03 | Recepcja | UNKNOWN | Przyjazdy i wyjazdy, rachunki, zaliczki, saldo, podział i historia. |
| M-04 | Sprzedaż | Kandydaci w inwentarzu. | Taryfy, gastronomia, SPA, vouchery, wydarzenia, promocje i usługi dodatkowe. |
| M-05 | Personel | UNKNOWN | Grafik, czas pracy, role i przypisywanie usług. |
| M-06 | Finanse | Kandydaci w inwentarzu. | Raporty, przychód, wpłaty, rozliczenia i zakres eksportu. |
| M-07 | Administracja i integracje | UNKNOWN | Konta i role, zasoby, ustawienia, powiadomienia i integracje. |
| M-08 | Sprzątanie i utrzymanie | Kandydaci w inwentarzu. | Gotowość pokojów, usterki, zadania i związek z przyjazdem. |

**Confirmed.** EV-07 potwierdza nawigację i trzy zakładki w drzewie dostępności. DOM zawiera pięć tabel o wspólnym układzie nagłówków i formularze z polami wyboru oraz tekstowymi. W drzewie dostępności odnotowano trzy tabele. EV-08 potwierdza, że pole „Numer telefonu” znajduje się w nawigacji poza formularzami. Zakładki mają znaczniki przełączania. Nagłówki tabel nie deklarują stanu sortowania.

**Open question.** Działanie pola, przełączanie zakładek, sortowanie i walidacja pozostają UNKNOWN. EV-09 pokazał wzorce ładowania i wywołań HTTP. Żaden nie dał podstaw do potwierdzenia obsługi konkretnego widoku. Dla pozostałych widoków potrzebne są dowody struktury oraz oddzielna weryfikacja zachowania. [Pokrycie i źródła](coverage-and-gaps.md)
