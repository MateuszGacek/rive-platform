# Rive — mapa możliwości produktu

**Status:** discovery / mapa robocza (12.11.2026). To **nie** jest zatwierdzony backlog, specyfikacja ani architektura. Źródło: rozmowy z właścicielem i [notatki discovery](../discovery.md).

- **Wymagane** = właściciel wskazał jako docelowe zachowanie produktu. Nie oznacza, że zostało zaprojektowane lub wdrożone.
- **Do weryfikacji** = możliwa podfunkcja lub wariant do sprawdzenia przed zatwierdzeniem.
- **Zależność** = relacja biznesowa do przemyślenia, nie automatycznie granica mikroserwisu.
- Identyfikatory (np. `BKG-01`) pomagają łączyć funkcje i diagramy, ale **nie zastępują GitHub Issues**.

[Wizualna mapa w Obsidian Canvas](../maps/rive-product-map.canvas) · [Jak korzystać z boardu](../maps/README.md)

## 01 Website i CMS

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| WEB-01 | Edycja treści i stron oferty (bez WordPressa) | Wymagane | Szybka strona publiczna, wybór CMS później |
| WEB-02 | Prezentacja noclegów i szczegółów oferty | Wymagane | Zakres zdjęć, udogodnień, opisów do ustalenia |
| WEB-03 | Kontakt przez formularz | Wymagane | Powiadomienia, spam, zgody do ustalenia |
| WEB-04 | Okresowe publikowanie wydarzeń | Wymagane | W pierwszej kolejności prezentacja; sprzedaż biletów niezatwierdzona |
| WEB-05 | Przejście ze strony do rezerwacji | Wymagane | Wspólna dostępność z rezerwacjami pracowników |

## 02 Rezerwacje i dostępność

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| BKG-01 | Wyszukanie noclegu na podstawie terminu | Wymagane | UX inspirowany platformami rezerwacyjnymi, nie ich pełny zakres |
| BKG-02 | Kalendarz dostępności noclegów | Wymagane | Spójność online i recepcji jest krytyczna |
| BKG-03 | Rezerwacja online | Wymagane | Potwierdzanie i dane gości do ustalenia |
| BKG-04 | Ręczna rezerwacja przy rozmowie telefonicznej | Wymagane | W panelu uprawnionego pracownika |
| BKG-05 | Konfiguracja jednostek noclegowych, cen i ograniczeń | Do weryfikacji | Nie znamy jeszcze modelu zasobów i cenników |
| BKG-06 | Zmiany, anulowanie, no-show i zasady zaliczek | Do weryfikacji | Sprawdzić istniejące zasady biznesowe |

## 03 Recepcja i rachunki gości

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| OPS-01 | Otwarcie rachunku klienta przy rezerwacji **lub** przy wejściu do obiektu | Wymagane | Rachunek przypisany do klienta; jeden czy kilka rachunków, czas życia i powiązania z wizytą pozostają otwarte |
| OPS-02 | Dopisywanie zakupów do otwartego rachunku | Wymagane | Gastronomia, usługi i pozostałe pozycje |
| OPS-03 | Podgląd i korekta pozycji rachunku | Do weryfikacji | Uprawnienia, anulowanie pozycji, ślad audytowy |
| OPS-04 | Zamknięcie rachunku i odnotowanie rozliczenia | Wymagane | Integracja z urządzeniami nie jest przesądzona |
| OPS-05 | Powiązanie rezerwacji z rachunkiem i wizytą | Do weryfikacji | Potwierdzić, czy rachunek z rezerwacji jest kontynuowany na miejscu, oraz obsługę grup i wielu pobytów |
| OPS-06 | Obsługa rachunku niezależnie od noclegu | Do weryfikacji | Klienci Day SPA, sauna, basen itd. |

## 04 Personel i czas pracy

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| HR-01 | Pracownik zapisuje dni i godziny pracy | Wymagane | Suma godzin czy przedział start/koniec — do ustalenia |
| HR-02 | Podgląd własnej ewidencji czasu | Do weryfikacji | Zakres historii i korekt |
| HR-03 | Zatwierdzanie i korekta wpisów | Do weryfikacji | Kto może edytować, audyt zmian |
| HR-04 | Planowanie grafików i dostępności personelu | Do weryfikacji | Wcześniejsza koncepcja, niezatwierdzony zakres pierwszej wersji |
| HR-05 | Wyliczanie wynagrodzeń na podstawie godzin | Do weryfikacji | Oddzielić kalkulację wewnętrzną od formalnych kadr/płac |

## 05 Finanse i raporty

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| FIN-01 | Sprzedaż według kategorii | Wymagane | Noclegi, gastronomia, usługi itd. |
| FIN-02 | Obrót, przychód i udziały procentowe | Wymagane | Definicje brutto/netto, memoriałowo/kasowo do uzgodnienia |
| FIN-03 | Raporty dostępne dla kierownictwa | Wymagane | Osobne uprawnienia od operacyjnego rachunku gościa |
| FIN-04 | Koszty, marże, zyski i eksporty | Do weryfikacji | Wcześniejsza wizja, trzeba ustalić źródła danych |
| FIN-05 | Rejestr metod i statusów płatności | Do weryfikacji | Odnotowanie opłaty ≠ integracja z terminalem |

## 06 Użytkownicy, role i dostęp

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| IAM-01 | Logowanie uprawnionych pracowników | Wymagane | Metoda uwierzytelniania nieustalona |
| IAM-02 | Role pracownika / supervisor / administrator | Wymagane | Dokładna macierz uprawnień do zdefiniowania |
| IAM-03 | Ograniczenia wglądu do finansów | Wymagane | Pracownik nie widzi wrażliwych danych finansowych |
| IAM-04 | Uprawnienia do operacji i korekt rachunków | Do weryfikacji | Kto może anulować, edytować lub zamknąć rachunek |
| IAM-05 | Dziennik ważnych operacji | Do weryfikacji | Szczególnie płatności, uprawnienia, korekty |

## 07 Wydarzenia i oferta dodatkowa

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| EVT-01 | Publikowanie wydarzeń na stronie | Wymagane | Na razie ich prezentacja |
| EVT-02 | Rezerwacje Day SPA, masaży i rytuałów | Do weryfikacji | Pojawiały się we wcześniejszej wizji |
| EVT-03 | Pakiety łączące noclegi i usługi | Do weryfikacji | Wymaga modelowania zależnych zasobów |
| EVT-04 | Vouchery, wydarzenia i rezerwacje grupowe | Do weryfikacji | Model zakupów, dostępności i rozliczeń do analizy |

## 08 Integracje i systemy zewnętrzne

| ID | Możliwość | Status | Uwaga |
| --- | --- | --- | --- |
| INT-01 | Obsługa płatności kartą / BLIK / terminalem | Wymagane jako proces biznesowy | Bez przesądzania o bezpośrednim API |
| INT-02 | Rozliczenia i kasa fiskalna | Wymagane jako proces biznesowy | Wpływ na system wymaga ustalenia |
| INT-03 | Zewnętrzne kanały noclegowe (np. Booking.com, Airbnb) | Do weryfikacji | Sprawdzić PMS/channel manager, dostępność API, koszty |
| INT-04 | Księgowość, eksport i dokumenty | Do weryfikacji | Nie budujemy własnego systemu fiskalizacji bez analizy |
| INT-05 | Powiadomienia, e-mail i kalendarz | Do weryfikacji | Kanały, automatyzacje i zgody do ustalenia |

## 09 Zależności przekrojowe (hipotezy do zweryfikowania)

| Zależność | Pytanie |
| --- | --- |
| WEB-05 → BKG-01/BKG-02 | Jak strona pokazuje bieżącą dostępność z tego samego źródła co recepcja? |
| BKG-03/BKG-04 → OPS-05 | Jak rezerwacja prowadzi do wizyty, pobytu i rachunku gościa? |
| OPS-02/OPS-04 → FIN-01/FIN-02 | Kiedy pozycja rachunku staje się sprzedażą i jak kategoryzować wpływy? |
| IAM-02/IAM-03 → OPS/HR/FIN | Jak rozdzielić obsługę operacyjną od dostępu do danych wrażliwych? |
| INT-01/INT-02 → OPS-04 | Czy system tylko rejestruje zapłatę, czy integruje urządzenia/usługi? |
| EVT-02/EVT-03 → BKG-02/HR-04 | Czy rezerwacja usługi blokuje jednocześnie miejsce, sprzęt i pracownika? |

## Co robimy dalej

Wybieramy **jeden realny proces** do dokładniejszego rozłożenia. Aktualny kandydat: klient wchodzi do obiektu → personel otwiera rachunek → dopisuje produkty/usługi → rachunek zostaje opłacony i zamknięty. Zapisujemy warianty dla noclegu i wizyty dziennej, jeśli istnieją.

Nie zamieniamy tej mapy w kilkadziesiąt Issues. Dopiero po potwierdzeniu zakresu wyznaczymy epiki, MVP i konkretne zadania agentów.
