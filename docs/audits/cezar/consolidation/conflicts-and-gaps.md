# Cezar i rivé — rozbieżności i luki

[Indeks dowodów](evidence-index.md) · [Powiązania z mapą rivé](capability-crosswalk.md) · [Pytania discovery](../../../product/open-questions.md)

## Rozbieżności istotne dla interpretacji

| Temat | Co wynika ze źródeł | Jak wykorzystać w discovery |
| --- | --- | --- |
| Wejście dzienne | `LEGACY_OBSERVED`: publiczna strona Cezara kieruje na telefon. `BUSINESS_CONFIRMED`: na start rivé pokazuje dostępność na stronie, a rezerwację przyjmuje telefonicznie recepcja. | Reguły rezerwacji online bez konta i przedpłaty dotyczą odłożonej samoobsługi WWW. [Warsztat recepcji](../../../product/reception-discovery.md#potwierdzenie-rezerwacji-przez-www), [PUB-03/09][pub], [D-04], [D-05] |
| Kalendarz i potwierdzenie noclegu | `LEGACY_OBSERVED`: audyt pokazuje osobny kalendarz, typy i odnośniki do logowania. `BUSINESS_CONFIRMED`: rivé blokuje jedno miejsce w puli wybranej opcji i potwierdza nocleg po zaliczce. | `OPEN_QUESTION`: kartę noclegu rivé można oprzeć o ustalenia właściciela. Sposób dostępu do rezerwacji noclegowych i zachowanie przy zmianie nadal wymagają doprecyzowania. Widoczne zasoby Autopay wskazują na obecność dostawcy w widoku Cezara. Reguły płatności Cezara i wybór dostawcy rivé pozostają otwarte. [PUB-02/08/09][pub], [D-03], [D-08] |
| Dwie liczby interakcji dashboardu | `LEGACY_OBSERVED`: podsumowanie obejmuje 3 interakcje w EV-11 oraz 18 zmian stanu kontrolek i 2 przejścia w EV-12. | Przebiegi raportujemy osobno. Zachowujemy 47 udokumentowanych ekranów. Siedem niepełnych renderów raportów ma osobny status. [DASH-01/02][dash] |
| Zakres prób responsywnych | `OPEN_QUESTION`: wprowadzenie raportu UX mówi o głównej, cenniku i panelu w trzech szerokościach oraz o „pozostałych 47 stronach”. Inwentarz liczy 47 adresów treści łącznie, a panel osobno. | Do podsumowania przyjmujemy licznik z raportu pokrycia. Brzmienie raportu UX nie zwiększa inwentarza ani zakresu prób na poszczególnych urządzeniach. [PUB-01/06][pub] |
| Skróty w dokumentacji rivé | `BUSINESS_CONFIRMED`: szczegółowe dokumenty opisują potwierdzenie noclegu po zaliczce i telefoniczne potwierdzenie wejścia. Reguły potwierdzenia e-mailem dotyczą odłożonej samoobsługi wejść. | `PROPOSED`: doprecyzować opisy kart `BKG-03` i `CRM-02` z odsyłaczami i zakresem obowiązywania. [Mapa możliwości](../../../product/capability-map.md#03-rezerwacje-i-dostępność), [potwierdzenia wejść](../../../product/reception-discovery.md#potwierdzenie-rezerwacji-przez-www), [D-03], [D-05] |

## Decyzje potrzebne przed szczegółową specyfikacją

| Pytanie | Co trzeba rozstrzygnąć | Kto i jaki dowód |
| --- | --- | --- |
| `OPEN_QUESTION` · [D-01] | Co obejmie pierwsza dostawa i jakie będą kryteria odbioru? | Decyzja właściciela w fazie 9. Dla zwykłej wizyty Day SPA ustalono prostotę obsługi jako kryterium scenariusza. |
| `OPEN_QUESTION` · [D-03], [D-07], [D-11] | Kto rozstrzyga o dostępności noclegu i blokadzie przy zmianie kanału, przydziału lub gotowości jednostki? Jak działa zmiana zaakceptowanej ceny, anulowanie i no-show? | Właściciel z recepcją, sprzedażą i obsługą obiektu. Próba ostatniego miejsca i zmiany przydziału, z uzgodnionym wynikiem. Listy i kalendarz Cezara pozostawiają te relacje otwarte. [DASH-03/09][dash] · [PUB-02/09][pub] |
| `OPEN_QUESTION` · [D-04], [D-10] | Jak pakiet zużywa wspólną pojemność i co dokładnie gwarantuje? Jak obsłużyć chwilowe wyjście z pakietu jednokrotnego, dopłatę za dodatkowy czas oraz wyjątek przy pełnej puli? | Właściciel z recepcją. Scenariusze pełnej kolejnej godziny, przedłużenia i niedostępnej składowej pakietu. Jedna pula oraz pierwszeństwo potwierdzonych wejść są już ustalone. [DASH-04/09][dash] · [PUB-03/09][pub] |
| `OPEN_QUESTION` · [D-05] | Jak obsłużyć błędny adres i ponowną wysyłkę linku do zarządzania wejściem w przyszłej samoobsłudze? | Właściciel. Przypadek zapisanego terminu i niedostarczonej wiadomości w [próbach przed specyfikacją](../../../product/reception-discovery.md#próby-przed-specyfikacją). Audyt publiczny zatrzymał się przed wysłaniem formularzy. [PUB-05/09][pub] |
| `OPEN_QUESTION` · [D-03], [D-08] | Jak potwierdzać przelew, obsłużyć spóźnioną wpłatę, rezerwację blisko przyjazdu i zwrot? Kto i kiedy wybiera moment dopłaty? | Właściciel z recepcją i księgowością. Przykład terminu już ponownie sprzedanego oraz potwierdzenia wpłaty po zwolnieniu puli. Wysokość i standardowe terminy zaliczki są już ustalone. [PUB-08/09][pub] |
| `OPEN_QUESTION` · [D-02], [D-08], [D-10] | Kto jest klientem rachunku grupowego i jak korygujemy pozycję, czas albo alokację po częściowej wpłacie? Kto może wykonać korektę i jaki dokument powstaje? | Właściciel z recepcją i księgowością. Przypadek częściowej wpłaty z oczekiwanym saldem i rolą, na [scenariuszu grupowym](../../../product/reception-discovery.md#pobyt-grupowy-z-zaliczką). [DASH-04/09][dash] |
| `OPEN_QUESTION` · [D-09], [D-10] | Jak liczymy przychody, koszty wspólne i marżę oraz jak uzgadniamy je z wpłatami, zwrotami i dokumentami? Kto widzi wynik? | Właściciel z księgowością. Jeden syntetyczny okres, z uzgodnioną definicją, źródłem i uprawnieniami do każdej miary. Widok kasowy daje punkt porównania bez dowodu wyliczeń. [DASH-07/09][dash] |

## Braki materiału źródłowego

- `OPEN_QUESTION`: dashboard pozostawia nieustalone m.in. zapis i skutki operacji, zachowanie niewyrenderowanych raportów, zasady dostępu, połączenia rekordów i eksport. Zależności kadrowe, sprzątania i kosztów potrzebują dowodów z przebiegu, zgodnie z [D-06], [D-07], [D-09] i [D-10]. Dostępność dodatkowego, oczyszczonego materiału dotyczy [Issue #3]. [DASH-07–09][dash]
- `OPEN_QUESTION`: publiczna strona dostarcza próbek UX, SEO i osadzonych usług. Skuteczność formularzy i integracji, wydajność na rzeczywistych urządzeniach oraz kwalifikacja zgód pozostają otwarte. W przyszłej próbie nie należy mieszać wyników dostępności, dostarczenia kontaktu i decyzji o prywatności. [PUB-05–09][pub], [D-05], [D-11], [D-12]
- `OPEN_QUESTION`: oba audyty nie wystarczają do wyboru dostawców, zakresu migracji ani procedury awarii. Potrzebny jest sprawdzony eksport i uzgodnienie danych, w tym rezerwacji, sald i voucherów, oraz scenariusz ręcznego odzyskania pracy. [D-11], [D-12], [D-13]
- `OPEN_QUESTION`: pełna treść prywatnej rozmowy ChatGPT i zawartość wcześniejszego archiwum discovery nie były dostępne do tej konsolidacji. Bieżące ustalenia właściciela są cytowane z wersjonowanego Markdown. [Issue #4] obejmuje odzyskanie i porównanie dodatkowego materiału.

## Co można projektować dalej

- **Day SPA** ma podstawę do rozpisania przebiegu od sprawdzenia dostępności na stronie i rezerwacji przez telefon, przez wejście i obecność, do rozliczenia i zwolnienia miejsca. Istnieją już przypadki spóźnienia, częściowego przybycia i chwilowego wyjścia. Decyzje o wyjątkach, taryfach i korektach są przy [D-02], [D-04] i [D-08]. [Warsztat recepcji](../../../product/reception-discovery.md#day-spa-bez-noclegu)
- **Oferta noclegowa** ma podstawę do rozpisania wyboru opcji i pakietu, blokady puli, wpłaty zaliczki, potwierdzenia i przydziału przez recepcję. Obsługa wpłaty po terminie, zmiany i anulowania pozostają przy [D-03] i [D-08]. [Ustalenia właściciela](../../../discovery.md#wywiad-z-właścicielem--oferta-noclegowa-2026-11-19)
- **Rachunek grupy** ma podstawę do przejścia przykładu z noclegiem, zakupami i wpłatami. Generowanie dokumentu, korekty, zakres uprawnień i uzgodnienie finansów wymagają rozstrzygnięć z [D-02], [D-08], [D-09] i [D-10]. [Scenariusz warsztatowy](../../../product/reception-discovery.md#pobyt-grupowy-z-zaliczką)

### Propozycje aktualizacji po przeglądzie

1. `PROPOSED` · W [mapie możliwości](../../../product/capability-map.md) link z `BKG-03` powinien prowadzić do ustalonego potwierdzenia noclegu po zaliczce. W `CRM-02` warto rozróżnić telefoniczne potwierdzenia Day SPA i e-maile dla przyszłej samoobsługi.
2. `PROPOSED` · W [D-03] wskazać źródło obserwacji o utracie kontekstu opcji noclegowej. W [D-09] odsyłać do obserwowanych widoków raportowych z zastrzeżeniem pokrycia. Scenariusze w [benchmarku](../../../research/hotel-spa-benchmark.md#wspólny-skrypt-demo) już obejmują potrzebne próby. Wystarczy uzupełnić ich źródła w ramach późniejszej aktualizacji.

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
[Issue #3]: https://github.com/MateuszGacek/rive-platform/issues/3
[Issue #4]: https://github.com/MateuszGacek/rive-platform/issues/4
