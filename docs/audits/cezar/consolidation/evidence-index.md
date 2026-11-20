# Cezar — indeks dowodów

[Powiązania z mapą rivé](capability-crosswalk.md) · [Rozbieżności i luki](conflicts-and-gaps.md) · [Project Brain](../../../README.md#project-brain)

Zakres obejmuje raporty dashboardu i publicznej strony, w tym publiczny widok kalendarza noclegów. Podstawą odczytu są raporty z 19 listopada 2026 i wymienione w nich wcześniejsze materiały. Odsyłacze prowadzą do raportów w tym samym repozytorium. Dashboard pochodzi z [PR #12] (`a48ae6af48938e766224869aa49687ea39f9f9bf`), a Public Web z [PR #13] (`d5f6bb7cbd29f66698efe988a22f39086cc4cc3e`). Punktem odniesienia dla reguł rivé jest `main` na `5619565`. Źródła biznesowe są przy odpowiednich wpisach w [mapowaniu](capability-crosswalk.md#potwierdzone-reguły-rivé).

## Jak czytać wpisy

- `LEGACY_OBSERVED` — obserwacja zapisana w audycie Cezara. Sprawdzona zmiana stanu kontrolki daje dowód działania interfejsu w konkretnym przebiegu. Widoczna kontrolka daje dowód jej obecności.
- `BUSINESS_CONFIRMED` — ustalenie właściciela zapisane w dokumentacji rivé, w granicach opisanych w źródle.
- `INFERRED` — wniosek z obserwacji, z podaną granicą pewności.
- `PROPOSED` — propozycja audytora lub dalszej pracy nad rivé.
- `OPEN_QUESTION` — brak dowodu lub sprawa wymagająca rozstrzygnięcia. Oryginalne `UNKNOWN`, `BLOCKED_WRITE` i `ACTION_NOT_EXECUTED` zachowują swoje różne znaczenia.

Identyfikatory `DASH-*` i `PUB-*` są odsyłaczami tej konsolidacji. `EV-*`, `W-*`, `RIV-*`, `E01–E10` oraz `I-01–I-12` pochodzą z raportów. Metryki pokrycia dotyczą osobnych inwentarzy i przebiegów. Prywatne snapshoty, logi i archiwalne materiały nie były ponownie weryfikowane.

## Dashboard

| Wpis | Status | Obserwacja i granica dowodu | Źródło |
| --- | --- | --- | --- |
| `DASH-01` | `LEGACY_OBSERVED` | `EV-11`: 57 znanych pozycji, 47 udokumentowanych ekranów, w tym 46 w tej rundzie, przekrojowo przez siedem sekcji nawigacji. Trzy potwierdzone interakcje w tym przebiegu. Siedem prób raportowych bez potwierdzonego renderu i trzy wejścia wyłączone z zakresu. | [Dashboard — podsumowanie][dash-readme], [pokrycie EV-11][dash-coverage] |
| `DASH-02` | `LEGACY_OBSERVED` | `EV-12`: ponowny odczyt 47 ekranów, 18 zmian stanu kontrolek liczonych per ekran i dwa przejścia do wcześniej udokumentowanych ekranów katalogu i raportu kasowego. Sprawdzono m.in. zakładki, menu i zmianę strony listy. Dodatkowa diagnostyka siedmiu tras raportowych nie dała nowego potwierdzonego renderu. | [Pokrycie EV-12][dash-ev12], [interakcje][dash-controls], [przejścia][dash-transitions] |
| `DASH-03` | `LEGACY_OBSERVED` | Listy rezerwacji według statusu i daty, lista rezerwowa z datami i statusem oraz osobne widoki imprez, voucherów i naparzania. Zmiany statusu i kontrolki zmieniające dane pozostały niewykonane. | `EV-11`, `W-11`, [macierz UI][dash-matrix], [procesy][dash-workflows] |
| `DASH-04` | `LEGACY_OBSERVED` | Lista gości pokazuje kategorie pól kontaktowych, punkty i rolę. Rachunki pokazują klienta, usługi i sumę. Widok ośrodka pokazuje liczbę osób i układ zakwaterowania. Te odczyty pozostawiają otwarte powiązania z rezerwacją, obecnością i rozliczeniem. | `EV-11`, [macierz UI][dash-matrix], [fragmenty procesu][dash-workflow-views] |
| `DASH-05` | `LEGACY_OBSERVED` | Produkty pokazują cenę i kategorię. Widoczne są m.in. promocje, sezony, opcje, konfiguracja kategorii i produkty za punkty. Reguły taryf, programu punktowego i przenoszenia ceny na rachunek nie zostały potwierdzone. | `EV-11`, [macierz UI][dash-matrix], [fragmenty procesu][dash-workflow-views] |
| `DASH-06` | `LEGACY_OBSERVED` | Widoki grafiku obejmują m.in. recepcję i sprzątanie. Ewidencja pokazuje datę, godziny od i do oraz sumę czasu. Widoki sprzątania pokazują punkty, grupy i komentarze. Zatwierdzanie czasu oraz wpływ grafiku i sprzątania na dostępność pozostają otwarte. | `EV-11`, [macierz UI][dash-matrix], [fragmenty procesu][dash-workflow-views] |
| `DASH-07` | `LEGACY_OBSERVED` | Odczytano wybrane widoki raportów kasowych, anulacji i pracowników oraz kontrolki formularzy i druku. Widać też ustawienia konta, pomoc i kontakty. Dostępne wyniki dotyczą widoków i nawigacji. | `EV-11`, `EV-12`, [macierz UI][dash-matrix], [pokrycie i luki][dash-coverage] |
| `DASH-08` | `LEGACY_OBSERVED` | `EV-01` i `EV-02` dokumentują pochodzenie listy i wcześniejszy odczyt. Kopie Claude i Codexa wymienione przy `EV-01` mają wspólne pochodzenie. `EV-07` i `EV-08` dokumentują zastany widok i DOM. `EV-09` to analiza statyczna. `EV-03`, `EV-04`, `EV-05` i `EV-10` dokumentują próby syntetyczne, które są wyłączone z pomiaru pokrycia panelu. | [Rejestr historyczny][dash-history] |
| `DASH-09` | `OPEN_QUESTION` | `W-01` (`BLOCKED_WRITE`) dotyczy przyjęcia i potwierdzenia rezerwacji oraz przydziału. `W-02–W-05` i `W-07–W-10` (`UNKNOWN`) obejmują m.in. przyjazd, wejście, pozycje, rozliczenie, grafik, sprzedaż i raporty. Otwarte są też reguły uprawnień, zakres eksportu i skutki serwerowe. | [Procesy i statusy źródłowe][dash-workflows], [granice pokrycia][dash-coverage] |
| `DASH-10` | `INFERRED` | `W-06`: lista może wspierać przegląd rezerwacji przez recepcję. Konkretna rola i jej uprawnienia pozostają niepotwierdzone. | [Procesy i statusy źródłowe][dash-workflows] |
| `DASH-11` | `PROPOSED` | `RIV-01–RIV-05` proponują scenariusze stanów rezerwacji, Day SPA, pobytu grupowego, grafiku i uzgodnienia raportów. Wykorzystują już istniejące pytania i scenariusze rivé. | [Rekomendacje dashboardu][dash-proposals], [scenariusze demo](../../../research/hotel-spa-benchmark.md#wspólny-skrypt-demo) |

## Public Web

| Wpis | Status | Obserwacja i granica dowodu | Źródło |
| --- | --- | --- | --- |
| `PUB-01` | `LEGACY_OBSERVED` | 47 z 47 odkrytych adresów treści zwróciło HTTP 200. Kalendarz noclegów HTTPS badano osobno. Inwentarz pochodzi z nawigacji, stopki i odsyłaczy z treści, z próbką języka angielskiego. | `E01`, `E02`, [pokrycie i dowody][pub-coverage], [inwentarz adresów][pub-map] |
| `PUB-02` | `LEGACY_OBSERVED` | Opisy dziewięciu noclegów i kempingu oraz osobny kalendarz z datami, liczbą osób, typami, logowaniem i informacją o anulowaniu. W głównej treści opisów brakowało przejścia do dostępności konkretnego typu. Link HTTP do panelu był blokowany w badanym kontekście, HTTPS otwierał panel. Osiem odpowiedników HTTPS starych linków dało 404. | `E01–E03`, `I-01`, `I-02`, `I-12`, [katalog i kalendarz][pub-functional], [ścieżki][pub-journeys], [problemy][pub-issues] |
| `PUB-03` | `LEGACY_OBSERVED` | Cennik rozróżnia wejścia godzinowe, sam nocleg, dostęp przy noclegu i kemping. Stawki są na grafikach. Nagłówek kieruje na telefon przy rezerwacji wejścia, a na obejrzanych stronach nie znaleziono formularza wejścia ani terminu zabiegu. | `E01`, `E04`, `I-03`, [oferta][pub-functional], [ścieżki][pub-journeys], [I-03][pub-price] |
| `PUB-04` | `LEGACY_OBSERVED` | Publiczny katalog obejmuje ośrodek, zabiegi, gastronomię, promocje, vouchery i wydarzenia. Widoczne ścieżki prowadzą m.in. do kontaktu, telefonu lub formularza promocji. Jedno wydarzenie ma pustą treść szczegółu, inne niespójny zakres dat. Restauracja pokazuje ofertę bez zaobserwowanej funkcji zamawiania. | `E01`, `E05`, `I-05`, `I-06`, [oferta][pub-functional], [ścieżki][pub-journeys], [problemy][pub-issues] |
| `PUB-05` | `LEGACY_OBSERVED` | Kontakt, newsletter i promocja pokazują pola i wymagania widoczne po stronie klienta, a kontakt automatycznie osadza mapę. W izolowanym przebiegu nie zaobserwowano banera. Skuteczność wysyłki, walidacja serwera i kwalifikacja zgód pozostają otwarte. | `E01`, `E08`, `I-10`, [oferta][pub-functional], [audyt techniczny][pub-technical], [I-10][pub-consent] |
| `PUB-06` | `LEGACY_OBSERVED` | Próbki wskazują problemy dostępności menu, formularzy, galerii i cennika oraz układu przy 768 px i kalendarza przy 390 px. Lighthouse to pojedyncza mobilna próbka strony głównej. | `E04`, `E06`, `E09`, `I-03`, `I-04`, `I-09`, [UX][pub-ux], [audyt techniczny][pub-technical], [problemy][pub-issues] |
| `PUB-07` | `LEGACY_OBSERVED` | Próbka HTML wykazała braki opisów meta. Standardowa ścieżka sitemap zwróciła 404. Zaobserwowano też liczbę żądań i komunikaty o obrazach. Zakres dowodu obejmuje badane ścieżki i próbki, więc pomiar rzeczywistego czasu ładowania pozostaje otwarty. | `E01`, `E07`, `E09`, `I-07`, `I-08`, [audyt techniczny][pub-technical], [problemy][pub-issues] |
| `PUB-08` | `LEGACY_OBSERVED` | Kalendarz ładuje zasoby Autopay i reCAPTCHA. W konsoli zgłoszono błąd reCAPTCHA. Krytyczność dla wysłania formularza i wynik płatności pozostają niezweryfikowane. | `E10`, `I-11`, [audyt techniczny][pub-technical], [I-11][pub-captcha] |
| `PUB-09` | `OPEN_QUESTION` | Audyt pozostawia otwarte wyniki finalizacji: walidację, zapis rezerwacji i synchronizację z recepcją, konto, e-mail, płatność, anulowanie, saldo vouchera i zachowanie cen po przejściu z oferty. | [Niezweryfikowane obszary][pub-limits], [granice analizy luk][pub-gap] |
| `PUB-10` | `INFERRED` | Powrót z opisu noclegu do ogólnego kalendarza może gubić kontekst wybranej opcji. Dla wejść i części usług zaobserwowany proces kieruje do telefonu. Audyt nie mierzył porzuceń ani wpływu na sprzedaż. | `I-12`, [ścieżki][pub-journeys], [UX][pub-ux], [analiza luk][pub-gap] |
| `PUB-11` | `PROPOSED` | Raport proponuje zachowanie wyboru noclegu, tekstowy cennik, sprawdzenie dostępności interfejsu i rozpisanie osobnych ścieżek noclegu, wejścia i pakietu. Propozycje mają podstawę w obserwacjach, a ich przydatność dla rivé należy ocenić względem istniejących wymagań. | [Analiza luk][pub-gap], [ścieżki][pub-journeys], [problemy][pub-issues] |

## Rozliczenie raportów

| Raport | Wykorzystanie |
| --- | --- |
| Dashboard — [README][dash-readme] | Pokrycie i rozdzielenie przebiegów `DASH-01/02`. |
| Dashboard — [business-workflows][dash-workflows] | Odczyt procesów, hipotezy i luki `DASH-02–06`, `DASH-09/10`. |
| Dashboard — [coverage-and-gaps][dash-coverage] | Wersje pomiaru, dowody historyczne i ograniczenia `DASH-01/02`, `DASH-07–09`. |
| Dashboard — [functional-matrix][dash-matrix] | Obserwacje widoków i kontrolek `DASH-02–07`. |
| Dashboard — [recommendations-for-rive][dash-proposals] | Hipotezy warsztatowe `DASH-11`, przypięte do istniejących `D-xx`. |
| Public Web — [coverage][pub-coverage] | Metoda, `E01–E10`, zakres `PUB-01–09`. |
| Public Web — [functional-audit][pub-functional] | Oferta, katalog i widoczne akcje `PUB-02–05`. |
| Public Web — [issues][pub-issues] | Wszystkie pozycje `I-01–I-12` scalone w `PUB-02–08`, propozycje w `PUB-11`. Priorytety źródłowe dotyczą Cezara. |
| Public Web — [rive-gap-analysis][pub-gap] | Granice wnioskowania `PUB-09/10`, propozycje `PUB-11`, potwierdzenia oparte ponownie o dokumentację rivé. |
| Public Web — [site-map][pub-map] | Inwentarz źródłowy `PUB-01`. Deduplikacja tematyczna w `PUB-02–05`; lista 47 adresów zostaje w raporcie. |
| Public Web — [technical-audit][pub-technical] | Próbki dostępności, SEO, integracji i wydajności `PUB-05–08`. |
| Public Web — [user-journeys][pub-journeys] | Przebiegi i miejsca przerwania `PUB-02–04`, `PUB-10/11`. |
| Public Web — [ux-audit][pub-ux] | Próbki responsywne i powtórzone obserwacje `PUB-02–06`, `PUB-10/11`. |

[PR #12]: https://github.com/MateuszGacek/rive-platform/pull/12
[PR #13]: https://github.com/MateuszGacek/rive-platform/pull/13
[dash-readme]: ../dashboard/README.md
[dash-coverage]: ../dashboard/coverage-and-gaps.md
[dash-history]: ../dashboard/coverage-and-gaps.md#stan-przed-eksploracją-ev-11
[dash-ev12]: ../dashboard/coverage-and-gaps.md#ev-12--pokrycie-działania
[dash-matrix]: ../dashboard/functional-matrix.md
[dash-controls]: ../dashboard/functional-matrix.md#ev-12--zweryfikowane-działanie-w-interfejsie
[dash-workflows]: ../dashboard/business-workflows.md
[dash-workflow-views]: ../dashboard/business-workflows.md#fragmenty-procesu-widoczne-w-ev-11
[dash-transitions]: ../dashboard/business-workflows.md#ev-12--przykłady-przejść-i-ograniczenia
[dash-proposals]: ../dashboard/recommendations-for-rive.md
[pub-coverage]: ../public-web/coverage.md
[pub-limits]: ../public-web/coverage.md#niezweryfikowane-obszary
[pub-functional]: ../public-web/functional-audit.md
[pub-issues]: ../public-web/issues.md
[pub-price]: ../public-web/issues.md#i-03
[pub-consent]: ../public-web/issues.md#i-10
[pub-captcha]: ../public-web/issues.md#i-11
[pub-gap]: ../public-web/rive-gap-analysis.md
[pub-map]: ../public-web/site-map.md
[pub-technical]: ../public-web/technical-audit.md
[pub-journeys]: ../public-web/user-journeys.md
[pub-ux]: ../public-web/ux-audit.md
