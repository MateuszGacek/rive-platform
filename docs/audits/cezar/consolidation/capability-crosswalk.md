# Cezar i rivé — powiązania z mapą możliwości

[Indeks dowodów](evidence-index.md) · [Rozbieżności i luki](conflicts-and-gaps.md) · [Mapa możliwości rivé](../../../product/capability-map.md) · [Mapy Obsidiana](../../../maps/README.md)

Identyfikatory `DASH-*` i `PUB-*` prowadzą do ustaleń audytów. Powiązanie oznacza wspólny temat i obowiązuje w granicach podanego dowodu. Zakres i stan poszczególnych kart określa mapa możliwości. Pytania pozostają w dotychczasowym [rejestrze](../../../product/open-questions.md).

## Potwierdzone reguły rivé

| Status | Zakres potwierdzenia | Źródło |
| --- | --- | --- |
| `BUSINESS_CONFIRMED` | Jeden obiekt. Sprzedaż bezpośrednia obejmuje noclegi oraz rezerwacje płatnych wejść. Właściciel potwierdził potrzebę raportowania przychodów, kosztów i rentowności. Wybór pilota i jego miary czeka na D-01. | [Wizja](../../../product/vision.md#confirmed-intent), [oferta noclegowa](../../../discovery.md#wywiad-z-właścicielem--oferta-noclegowa-2026-11-19), [Day SPA](../../../product/reception-discovery.md#day-spa-bez-noclegu), [finanse](../../../product/capability-map.md#11-finanse-i-analityka), [D-01] |
| `BUSINESS_CONFIRMED` | Gość wybiera opcję noclegu z puli typu i pojemności. Recepcja przypisuje jednostkę i może zmienić jej przydział. Cena samego noclegu jest za jednostkę za noc. Dostęp w pakiecie może obejmować cały pobyt albo jedno wejście czasowe. Wycenia się go dla zadeklarowanej liczby osób, a recepcja przypisuje go uczestnikom na miejscu. | [Oferta noclegowa](../../../discovery.md#wywiad-z-właścicielem--oferta-noclegowa-2026-11-19), [pakiety](../../../product/reception-discovery.md#pakiety-noclegowe-z-dostępem-do-ośrodka) |
| `BUSINESS_CONFIRMED` | Formularz noclegowy tworzy tymczasową blokadę i uruchamia wysyłkę linku do płatności. Potwierdzenie następuje po wpłacie zaliczki 30% łącznej ceny. Terminy wynoszą 2 godziny dla szybkiej płatności i 24 godziny dla zwykłego przelewu. Dopłata jest możliwa przy zameldowaniu lub przy wyjeździe. | [Zaliczka i terminy](../../../discovery.md#wywiad-z-właścicielem--oferta-noclegowa-2026-11-19), [D-08] |
| `BUSINESS_CONFIRMED` | Wejście dzienne przez WWW jest potwierdzane od razu po udanym zapisie, bez konta i przedpłaty. Link z e-maila umożliwia zmianę lub odwołanie do planowanej godziny wejścia. Aktualny termin obowiązuje do skutecznego zapisania zmiany. | [Potwierdzenie WWW](../../../product/reception-discovery.md#potwierdzenie-rezerwacji-przez-www), [D-05] |
| `BUSINESS_CONFIRMED` | Jedna pula dla ośrodka i osobno faktyczna obecność. Potwierdzone wejście ma pierwszeństwo przed wyjątkiem recepcji. Czas i obecność liczy się dla każdej osoby. Rozliczenie jest na miejscu, minutowo. Reguły spóźnienia, częściowego przybycia i chwilowego wyjścia są opisane w warsztacie. | [Dostępność i rozliczenie](../../../product/reception-discovery.md#reguły-oferty-dostępności-i-rozliczenia), [spóźnienie](../../../product/reception-discovery.md#spóźnienie-na-zarezerwowane-wejście), [chwilowe wyjście](../../../product/reception-discovery.md#chwilowe-wyjście) |
| `BUSINESS_CONFIRMED` | Wspólny rachunek może objąć nocleg, zakupy i wpłaty. Recepcja może przypisać pozycje uczestnikom i zmienić podział przy rozliczeniu. Zaliczka pomniejsza saldo. Wizyta dzienna może być rozliczona indywidualnie lub na wspólnym rachunku. | [Recepcja i rachunki](../../../product/reception-discovery.md#punkt-wyjścia), [D-02], [D-08] |

## Powiązania według obszarów

| Obszar i istniejące karty | Dowód Cezara | Znaczenie dla rivé i powiązane pytania |
| --- | --- | --- |
| **WEB** · `WEB-01–05` | [PUB-02–07, PUB-10/11][pub] — opisy noclegów, kalendarz, treści i kontakt, dostępność, SEO i ścieżki mobilne. | `LEGACY_OBSERVED`: osobne opisy i kalendarz tworzą przejście między widokami. `PROPOSED`: rozważyć zachowanie wybranej opcji i czytelny cennik w badaniu ścieżki. Publikacja, treści i dostępność pozostają w [D-03]. Wydarzenia publiczne mapują się do `WEB-04`. |
| **CAT** · `CAT-01/02` | [DASH-05][dash] i [PUB-03/04][pub] — kategorie, ceny, promocje i rozdział usług w cenniku. | `LEGACY_OBSERVED`: na ekranach są warianty cenowe i kategorie. `OPEN_QUESTION`: kolejność taryf i zachowanie zaakceptowanej ceny, [D-03]. Przykłady Cezara dostarczają materiału do porównania z regułą jednostki i dostępu za uczestnika. |
| **BKG** · `BKG-01–06` | [DASH-02/03, DASH-09/10][dash] i [PUB-02, PUB-09/10][pub] — listy, statusy, daty i kalendarz, z ograniczeniami finalizacji. | `LEGACY_OBSERVED`: istnieją osobne widoki list i kalendarza. `OPEN_QUESTION`: reguły dostępności, przydziału, zmian i zwrotów nie wynikają z nazw ani kolumn. Dla rivé podstawą są typ i pula noclegu oraz potwierdzenie po zaliczce. [D-03], [D-08] |
| **EVT** · `EVT-02–06` | [DASH-03/04][dash] i [PUB-03/04, PUB-09][pub] — usługi, wydarzenia, vouchery, cennik wejść i liczba osób na widoku ośrodka. | `LEGACY_OBSERVED`: część ścieżek kieruje do telefonu lub kontaktu. `OPEN_QUESTION`: jakie miejsce w puli gwarantuje pakiet i jak rozliczać jego wyjątki. Terminarz zabiegów i saldo vouchera pozostają niepotwierdzone w audycie. [D-04] |
| **CRM** · `CRM-01/02` | [DASH-04][dash] i [PUB-02, PUB-05, PUB-09][pub] — lista gości, formularze i odnośniki do konta. | `LEGACY_OBSERVED`: kategorie pól w UI. `OPEN_QUESTION`: powiązania profili i dostawa wiadomości. Dla wejść rivé dane minimalne i e-mail są już potwierdzone. [D-05], [D-12] |
| **OPS** · `OPS-01–09` | [DASH-04, DASH-09/10][dash] — układ rachunku, gość, liczba osób i nieodczytane relacje między operacjami. | `LEGACY_OBSERVED`: widok rachunku zestawia klienta, usługi i sumę. `OPEN_QUESTION`: zasady przyjazdu i wyjazdu, klient rachunku grupy, korekty i zamknięcie zmiany. Ustalenia wspólnego rachunku pochodzą z warsztatu rivé. [D-02], [D-08], [D-09] |
| **POS** · `POS-01–03` | [DASH-04/05, DASH-09][dash] i [PUB-04][pub] — katalog i rachunki w panelu, oferta restauracji w WWW. | `LEGACY_OBSERVED`: poszczególne widoki pokazują dane handlowe. `OPEN_QUESTION`: jak zakup trafia na rachunek, kiedy jest płatny od razu i jak uzgadnia się korekty. [D-02], [D-08] |
| **HR** · `HR-01–06` | [DASH-06/07, DASH-09/11][dash] — grafik, ewidencja i raporty pracownicze. | `LEGACY_OBSERVED`: widoczne przedziały i suma czasu. `OPEN_QUESTION`: zatwierdzanie, korekty, kalkulacja wynagrodzeń oraz wpływ absencji na dostępność usługi. [D-06] |
| **FAC** · `FAC-01/02` | [DASH-04/06, DASH-09][dash] — widoki zakwaterowania i sprzątania. | `LEGACY_OBSERVED`: ekrany zawierają elementy związane z zakwaterowaniem i zadaniami. `OPEN_QUESTION`: skutki statusu gotowości lub usterki dla wydania pokoju i sprzedaży. [D-07], [D-03] |
| **PAY** · `PAY-01/02` | [DASH-04/07, DASH-09][dash] i [PUB-08/09][pub] — sumy rachunku, widoki kasowe i zasoby płatnicze w kalendarzu. | `LEGACY_OBSERVED`: widoczne elementy płatności i raportów. `OPEN_QUESTION`: potwierdzanie przelewu, spóźnione wpłaty, zwroty i dokumenty. Obsługę salda i zaliczki określają źródła rivé. [D-08] |
| **FIN** · `FIN-01–06` | [DASH-02/07, DASH-09][dash] — widoki kasowe, anulacje i pracownicy, częściowe pokrycie raportów. | `LEGACY_OBSERVED`: audyt pokazuje dostęp do wybranych widoków i kontrolek. `OPEN_QUESTION`: definicje miar, kosztów i marży, wygenerowanie raportu, eksport i uzgodnienie. [D-09] |
| **IAM** · `IAM-01–05` | [DASH-04/07, DASH-09/10][dash] i [PUB-02][pub] — pola roli, ustawienia konta i publiczne odnośniki do konta. | `LEGACY_OBSERVED`: widoczność opcji w konkretnym kontekście. `OPEN_QUESTION`: macierz ról, egzekwowanie dostępu i historia zmian. Brak renderu raportu nie dowodzi odmowy dostępu. [D-10] |
| **INT** · `INT-01/02`, `INT-05/06` | [DASH-09][dash] i [PUB-05, PUB-08/09][pub] — widoczne zasoby płatności, formularze i mapa. | `LEGACY_OBSERVED`: zasoby w publicznym widoku. `OPEN_QUESTION`: rzeczywiste połączenia, potwierdzenie dostaw e-mail i płatności, zakres zapisu. Audyty nie dostarczają wystarczającego dowodu o OTA (`INT-03`) ani o księgowości i fiskalizacji (`INT-02/04`). [D-05], [D-08], [D-11] |
| **DAT** · `DAT-01/02` | [DASH-04, DASH-09][dash] i [PUB-05/09][pub] — kategorie informacji, formularze i osadzony dostawca mapy. | `LEGACY_OBSERVED`: widoczny zakres wybranych danych. `OPEN_QUESTION`: powiązania rekordów, możliwość eksportu, retencja, kwalifikacja zgód i zakres migracji. [D-10], [D-12] |
| **ENG** · `ENG-01–03` | [DASH-01/02, DASH-08/09][dash] i [PUB-07–09][pub] — ograniczenia prób, próbki diagnostyczne i brak wyników procesów końcowych. | `OPEN_QUESTION`: ciągłość pracy, odzyskiwanie i sposób dostawy. Próbki mogą pomóc przygotować kryteria obserwacji. Wybór architektury pozostaje w [D-13]. |

## Elementy bez bezpośredniego odpowiednika

- `LEGACY_OBSERVED`: pola punktów, widok produktów za punkty i pomoc starego panelu pozostają materiałem kontekstowym. Powiązania z `CAT-01` lub `CRM-01` są tematyczne. Brak osobnej karty programu punktowego lub centrum pomocy. [DASH-04/05/07][dash]
- `LEGACY_OBSERVED`: konkretne promocje, kemping, naparzanie i newsletter pozostają przykładami oferty lub komunikacji. Można je odnieść do katalogu, wydarzeń lub komunikacji, bez przypisywania rivé każdego wariantu sprzedaży z Cezara. [DASH-03/05][dash] · [PUB-02–05][pub]
- `LEGACY_OBSERVED`: konkretne usterki odnośników, metadanych i układu należą do dowodów o starej stronie. `PROPOSED`: użyć rodzajów usterek przy określaniu kryteriów projektowych tam, gdzie wspierają istniejące `WEB-01–05`. [PUB-02, PUB-06/07/11][pub]

[dash]: evidence-index.md#dashboard
[pub]: evidence-index.md#public-web
[D-01]: ../../../product/open-questions.md#d-01
[D-02]: ../../../product/open-questions.md#d-02
[D-03]: ../../../product/open-questions.md#d-03
[D-04]: ../../../product/open-questions.md#d-04
[D-05]: ../../../product/open-questions.md#d-05
[D-06]: ../../../product/open-questions.md#d-06
[D-07]: ../../../product/open-questions.md#d-07
[D-08]: ../../../product/open-questions.md#d-08
[D-09]: ../../../product/open-questions.md#d-09
[D-10]: ../../../product/open-questions.md#d-10
[D-11]: ../../../product/open-questions.md#d-11
[D-12]: ../../../product/open-questions.md#d-12
[D-13]: ../../../product/open-questions.md#d-13
