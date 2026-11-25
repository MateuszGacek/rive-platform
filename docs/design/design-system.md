# rivé — Design System v0.1

- **Version** — 0.1
- **Status** — Draft / Discovery
- **Source** — Owner-provided brand direction, June 2026
- **Last reviewed** — 2026-11-13

**Quiet Luxury × Forest Wellness × Editorial Minimalism** guides the visual direction for both Public Web and Dashboard / CRM.

## Brand palette

**Confirmed** — The seven colors below are the recovered historical rivé palette. The interface roles are **Proposed**.

| Color | HEX | Proposed role |
| --- | --- | --- |
| Warm Ivory | `#F5F1E8` | Main background and label on the primary action |
| Natural Linen | `#E9E1D6` | Surface background |
| Sand Beige | `#DCCFBE` | Surface background |
| Oak Wood | `#C2A37D` | Accent |
| Sage Green | `#6F7A64` | Accent |
| Forest Green | `#264033` | Primary text and primary action background |
| Water Reflection | `#B9D1CF` | Accent |

Historical variants[^historical-variants] appear in earlier brand material.

[^historical-variants]: Earlier values included Oak `#C2A370` and Sage `#6F7A44`. The table records the values selected for the recovered palette.

**Proposed** — Use Chocolate Brown `#5A3D32` as a warm accent and Light Cocoa `#E8D8CB` as a complementary surface in editorial sections.

**Open question** — Select specific font families and colors for error, success, warning, and focus states.

## Visual principles

**Proposed** — Public Web and Dashboard / CRM share the same brand and adapt it to different tasks.

| Area | Public Web | Dashboard / CRM |
| --- | --- | --- |
| Priority | Atmosphere and conversion | Readability and efficiency |
| Layout | Spacious, editorial layouts | Structured, denser layouts |
| Typography | Serif headings and sans-serif body text | Predominantly sans-serif |
| Color | Natural backgrounds and larger areas of accent color | Neutral backgrounds and sparing use of accents |
| Photography | Central to communication | Secondary |

Favor natural materials, authentic photography of the property, generous space, and restrained compositions. Avoid ostentatious luxury, gold gradients, neon colors, and generic SaaS styling. Label visualizations of spaces that do not yet exist as concepts.

## Accessibility

- Use a minimum contrast ratio of **4.5:1** for normal text and **3:1** for large text. For text over photography, gradients, or overlays, check the rendered background in the least contrasting area behind the text. [WCAG 2.2 SC 1.4.3 — Contrast (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html)
- Use at least **3:1** contrast against adjacent colors for the visual information needed to identify controls, their states, and meaningful parts of graphics. [WCAG 2.2 SC 1.4.11 — Non-text Contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html)
- Pair status colors with a text label or another clear visual cue. The Level A use-of-color criterion also applies when targeting Level AA. [WCAG 2.2 SC 1.4.1 — Use of Color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html)

| Color on Warm Ivory | Contrast | Meets the minimum for normal text |
| --- | ---: | --- |
| Forest Green | 10.00:1 | Yes |
| Sage Green | 4.01:1 | No |
| Chocolate Brown | 8.67:1 | Yes |

Compare the unrounded ratio with the threshold. These results apply to the listed pairs on solid Warm Ivory.

## Change management

1. Record each new color or pattern as **Proposed**. Move it to **Confirmed** only after the owner explicitly approves it. Record the decision source and date.
2. Maintain the canonical specification in this repository.
3. After the UI library exists, use `/design-sync` from Claude Code as a separate step to import approved changes into Claude Design. Existing designs retain the copy they were created with and need an explicit update. [Claude Help Center](https://support.claude.com/en/articles/14604416-get-started-with-claude-design) · [Claude Academy](https://academy.claude.com/tutorials/create-a-design-system-with-claude)

## Interfejs gościa i pracownika · Proposed, 2026-11-25

Persony robocze opisują zadanie. **Confirmed** są czynności w [discovery](../discovery.md) i [scenariuszach recepcji](../product/reception-discovery.md). Częstotliwość użycia, urządzenia i preferencje odbiorców to hipotezy.

| Osoba i potrzeba | Wejście oraz droga do celu | Co sprawdzić na urządzeniu |
| --- | --- | --- |
| Organizator pobytu chce znać pełny koszt | Noclegi → karta typu → daty, pakiet i cena → zaliczka → potwierdzenie → link zarządzania. Po potwierdzeniu może dobrać śniadanie do rachunku. | Telefon, utrata połączenia po płatności, powrót do tego samego typu i informacji o wpłacie. |
| Gość dzienny chce zaplanować wizytę | Day SPA → godziny, zasady i dostępność dnia → „Zadzwoń”. Osoba z pakietem widzi, które wejścia obejmuje pobyt. | Klikalny numer oraz numer jako tekst. Dostępność dnia nie obiecuje terminu dla całej grupy. |
| Kupujący prezent lub bilet | Vouchery lub wydarzenia → warunki, termin i cena → zakup → potwierdzenie. Rozróżnić dane do zakupu od danych potrzebnych do realizacji. | Czy obdarowany potrafi odczytać, co mu przysługuje i jak umówić usługę? |
| Recepcja rozpoznaje gościa i wyjątki | „Dziś” → „Nowa rezerwacja” / „Wejście” → obecność → rachunek → wpłata. Do zmiany jednostki służy kalendarz noclegów. | Na tablecie główne akcje widoczne bez najechania myszą. Na desktopie klawiatura umożliwia znalezienie rachunku i powrót do listy. |
| Gastronomia, sprzątanie, personel, właściciel | Każda rola otwiera swoje zadanie: dopisanie zamówienia, lista jednostek wg przyjazdu, „Rozpocznij/Zakończ”, wynik wg gałęzi z datą i podstawą. | Ograniczyć widok do dozwolonych danych. Przy kilku/kilkunastu pozycjach wystarczą lista i proste wyszukanie. |

**Proposed — nawigacja.** Publiczne sekcje: Noclegi, Day SPA, pakiety, wydarzenia, vouchery, obiekt i dojazd. Pokazywać pozycję gdy ma aktualną ofertę. Panel udostępnia wspólne rekordy przez widoki zależne od roli. Sprzątanie widzi jednostkę i zadanie. Gastronomia widzi minimum do rozpoznania rachunku i własne zamówienia. Porównać z układem według działów opisanym w [wariantach architektury](../product/mvp-architecture.md). Redaktor może opublikować kartę w podglądzie mobilnym i desktopowym. Właściciel rozstrzyga nazwy kategorii i kolejność w menu po wskazaniu priorytetowych ofert.

**Proposed — tokeny i komponenty.** Paleta historyczna → rola semantyczna (tło, tekst, powierzchnia, akcja, fokus, błąd) → użycie w komponencie. Proponowana skala odstępów 4/8/12/16/24/32/48 px. Większy oddech i zdjęcia na WWW, mniejsze odstępy i cyfry tabelaryczne dla kwot i godzin w panelu. Serif w nagłówkach redakcyjnych, sans-serif w treści i operacjach. Fonty sprawdzić z polskimi znakami, wagą plików i czytelnością na tablecie. Potwierdzone barwy zachowują wartości z palety. Role ostrzeżenia, błędu i sukcesu wymagają prób kontrastu oraz etykiety tekstowej.

Wspólne: przycisk, pole z opisem błędu, wybór daty z alternatywą klawiaturową, kwota, status, komunikat. Publiczne: karta opcji noclegu, oferta prezentowa, podsumowanie zakupu. Operacyjne: wykaz wejść, przydziały jednostek, pozycja rachunku z alokacją i wpłatą. Łączyć komponenty, gdy mają wspólne zachowanie i semantykę. Tabela pracownicza i kalendarz gościa mają inne zadania.

| Stan | Publiczna sprzedaż | Panel |
| --- | --- | --- |
| Ładowanie / brak danych | Oznaczyć sprawdzanie dat. Odróżnić brak miejsc od niedostępności źródła, umożliwić telefon. | Zachować kontekst. Pusta lista opisuje dzień lub brak dopasowania. |
| Niepewny wynik / błąd | Po powrocie od operatora odczytać stan płatności. Wyjaśnić dalszy krok bez ponownego obciążenia. | Przy błędzie zapisu zachować wpis. Przy niepewnym wyniku najpierw odczytać stan, pokazać konflikt i możliwą czynność. |
| Sukces | Odróżnić przyjęcie formularza i oczekiwanie na wpłatę od potwierdzenia rezerwacji. | Wskazać, czego dotyczył zapis, zaktualizować saldo lub obecność; rutynowy sukces nie wymaga kolejnego kliknięcia. |

**Odbiór projektu.** Scenariusz → warianty elementu na danych syntetycznych → semantyczne tokeny → próba klawiaturą, czytnikiem i dotykiem. Sprawdzić widoczny fokus, powiększenie, ogłaszanie wyników formularza, etykiety pól oraz nagłówek na szerokości tabletu. Sprawdzić powrót z kalendarza do wybranej karty, nazwę i stan rozwinięcia menu mobilnego oraz atomową zamianę dwóch przydziałów wyborem z listy bez przeciągania. Storybook albo prosty katalog przykładów w repo dopiero przy bibliotece współdzielonej. Dla stanów komponentów stosować porównania wizualne, dla płatności także próbę kompletnej transakcji. [WCAG 2.2](https://www.w3.org/TR/WCAG22/) · [Audyt publicznej strony](../audits/cezar/public-web/issues.md)

## Wspólne elementy przy niezależnych wydaniach

**Proposed — druga sesja 2026-11-25.** Współdzielenie zaczyna się od znaczenia elementu. Nazwy ról kolorów, format prezentacji kwoty z walutą, etykiety formularzy, fokus i obsługa komunikatu o błędzie mogą mieć jedną specyfikację nawet przy różnych frameworkach. Wspólna biblioteka kodu ma sens, gdy oba interfejsy mogą używać jej bez wymuszania tego samego sposobu renderowania. Przy różnych stosach można współdzielić tokeny i przypadki odbioru, utrzymując dwie cienkie implementacje.

| Zakres | Kontrakt elementu | Co należy do aplikacji |
| --- | --- | --- |
| Wybór daty | Wybór klawiaturą i dotykiem, etykieta odczytywana przez czytnik, zachowanie wyboru po zmianie miesiąca i powrót fokusu. | WWW pokazuje dzień z możliwym terminem Day SPA dla jednej osoby. Recepcja rozpatruje konkretną grupę i może zapisać wyjątek. Nocleg wymaga dostępności przez cały okres. |
| Cena i status | Format kwoty, tekstowe znaczenie statusu, komunikat o zmianie. | „Od”, pełna cena pobytu, pozostałe saldo i wpłacona zaliczka mają osobne etykiety i źródła. Kolor lub jeden wspólny status „sukces” nie wyjaśni, czy zapisano formularz czy potwierdzono wpłatę. |
| Nawigacja i gęstość | Czytelny fokus, nazwy akcji i zachowanie po powrocie. | Publiczna karta wykorzystuje fotografię i rytm marki. Panel utrzymuje pozycję na liście i ostatni kontekst obsługi po powrocie z rachunku. |

**Proponowany sposób zmiany.** Gdy drugi ekran potrzebuje tego samego zachowania, autor wskazuje dwóch odbiorców i próbę dla każdego. Zmiana wspólnego elementu przechodzi sprawdzenie klawiaturą, czytnikiem i na tablecie w obu kontekstach. Niezależne wdrożenia dodatkowo sprawdzają starszy interfejs z nowym kontraktem. Do czasu pojawienia się drugiego odbiorcy wzorzec może pozostać lokalny; decyzję o bibliotece i narzędziu wizualnych testów można podjąć później.

**Próba czytnikiem ekranu.** Gość zmienia dzień klawiaturą. Przy pojedynczym wolnym miejscu od 19:00 do 20:00 słyszy „Są wolne terminy”, bez obietnicy dla grupy. Przy wyczerpaniu puli słyszy „Brak wolnych terminów”, a przy awarii „Nie udało się sprawdzić dostępności” z dostępną akcją „Zadzwoń”. Po ponownym odczycie informacja dotyczy aktualnie wybranego dnia. [Reguła publicznej dostępności](../product/reception-discovery.md#potwierdzenie-rezerwacji-przez-www)
