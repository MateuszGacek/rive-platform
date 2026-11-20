# Widoki i funkcje według obszaru

**Confirmed.** EV-11 rozszerza historyczny odczyt listy rezerwacji na wiele ekranów. Opis dotyczy struktury i widocznych opcji. Metody formularzy opisują markup, a etykiety akcji wskazują elementy do dalszej weryfikacji.

| Obszar | Funkcje i elementy widoczne w UI | Open question |
| --- | --- | --- |
| Rezerwacje | Osobne widoki oczekujących, zakończonych, anulowanych i listy według daty. Lista rezerwowa ma kolumny przyjazdu, wyjazdu i statusu. Rozpoznano też odrębne widoki imprez, voucherów i naparzania. | Zasady przejścia między stanami, dostępność, przydział zasobu, zachowanie szczegółów, anulowania i zmian. |
| Recepcja i klienci | Lista gości z polami kontaktowymi oraz kolumnami punktów i roli. Widok rachunków zestawia numer, klienta, usługi, uwagi i sumę. | Rola kont, rozliczenie, powiązanie z pobytami i przypisanie usług. |
| Ośrodek | Odczytano widok liczby osób z układem zakwaterowania. | Brak potwierdzenia liczników wejść, reguł pojemności i naliczania czasu. |
| Sprzedaż | Produkty z kolumnami nazwy i ceny oraz polem wyboru kategorii. Oddzielne widoki promocji, kategorii, imprez, filtrów, opcji, sezonów i produktów za punkty. | Reguły cen, punkty i użycie cen w rachunkach oraz płatnościach. |
| Personel | Widok grafiku z grupami recepcji i sprzątania. Ewidencja ma datę, godziny od/do, liczbę godzin i pracownika. | Reguły zatwierdzania, grafik a rezerwacja i sposób obliczeń. |
| Sprzątanie | Widoki punktów dziennych i tygodniowych, grup, komentarzy i tematów. | Przypisanie zadań oraz związek gotowości pokoju z recepcją. |
| Raporty | Wybrane widoki raportów kasowych, anulacji i pracowników. Widoczne formularze wyboru oraz kontrolki drukowania. | Obliczanie, generowanie, druk i eksport. Część ekranów nie wyrenderowała się w oknie próby. |
| Administracja i pomoc | Ustawienia konta z formularzem hasła, widoki pomocy, tematów i kontaktów. | Uprawnienia, zakres dziennika, integracje i faktyczna rola kandydatów. |

**BEHAVIOR_VERIFIED.** Na liście rezerwacji przełączono zakładkę „Czekające na potwierdzenie” i rozwinięto menu „Sprzedaż” oraz „Raporty”. Działanie formularzy, wyszukiwania, modyfikacji, płatności i przycisków drukowania pozostaje niezweryfikowane.

[Miary pokrycia i dowody](coverage-and-gaps.md)

<!-- EV-12 START -->
## EV-12 — zweryfikowane działanie w interfejsie

- Zakładki: Czekające na potwierdzenie, Promocja, Impreza, Punkty tygodniowe, Zamknięte. Dowód obejmuje stan aktywny i panel.
- Menu rozwijane: Sprzedaż, Raporty. Potwierdzono stan rozwinięcia w wybranych ekranach.
- Stronicowanie: lista zakończonych rezerwacji przeszła ze strony 1 na 2; aktywny numer strony został potwierdzony.
- W pozostałych przypadkach odnotowano strukturę, brak zmiany w obserwacji lub nie wykonano akcji. Działanie filtrów, sortowania, kontrolek daty, podglądów i modali pozostaje niepotwierdzone.
<!-- EV-12 END -->
