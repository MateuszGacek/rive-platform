# Audyt UX i widoków responsywnych

**OBSERVED — 2026-11-19.** Oglądano stronę główną, cennik i publiczny panel rezerwacji na desktopie, tablecie 768 px oraz mobile 390 px. Dla pozostałych 47 stron zapisano strukturę i linki, bez osobnych zrzutów dla każdej szerokości. [Pokrycie](coverage.md).

## Co użytkownik widzi

**OBSERVED.** Strona główna wyróżnia promocje, kalendarz noclegów, wydarzenia i restaurację. W nagłówku stale pojawia się informacja o konieczności rezerwacji telefonicznej na wstęp. Podmenu grupuje typy noclegu oraz informacje o obiekcie. Na mobile przycisk menu otwiera listę, a wybranie „Nocleg” pokazuje pokoje i link „Zarezerwuj nocleg”.

**OBSERVED.** Strony pokoi pokazują opisy i galerie, ale w głównej treści nie ma CTA do rezerwacji danego typu. Użytkownik wraca do menu albo strony głównej, by dotrzeć do wspólnego kalendarza. Panel kalendarza używa innych nazw części pokoi niż menu serwisu i zawiera odnośniki do starych adresów.

**OBSERVED.** Na cenniku cztery grafiki przedstawiają taryfy. Przy 390 px układają się pionowo i wymagają długiego przewijania. Tekstu stawek nie da się odnaleźć w snapshot DOM. Podczas pełnego zrzutu ekranu ostatnia grafika początkowo nie była załadowana, a po przewinięciu pojawiła się poprawnie; nie uznano tego za brakujący obraz.

**OBSERVED.** Przy 768 px zielony komunikat w nagłówku nachodzi na logo. Przy 390 px panel rezerwacji pokazuje tylko część poziomego kalendarza; dalsze daty nie są widoczne w pierwszym kadrze. Mobilny przycisk menu na stronie Cezar nie ma czytelnej nazwy dostępnej dla technologii asystujących (potwierdzone przez Lighthouse).

## Spójność przekazu

**OBSERVED.** Strona wydarzeń podaje niespójny zakres dat dla „Sylwestra 2026”, a szczegóły wydarzenia z 2027 r. są puste. Sekcja promocji „Pierwszy raz za darmo” kieruje do osobnego formularza zbierającego dane; strona bonów kieruje do kontaktu. Sposób rozpoczęcia zakupu zmienia się między ofertami.

**INFERRED.** Największe tarcie w ścieżce noclegowej wynika z przełączenia na osobny panel i braku zachowania kontekstu wybranego pokoju. W ofercie wejść i usług użytkownik częściej musi przejść na telefon, nawet po odczytaniu cennika.

**PROPOSED.** W przyszłej stronie rivé doprowadzić z każdej oferty do właściwego następnego kroku: dostępności noclegu, wyboru wejścia albo kontaktu przy usłudze, która wymaga ręcznego uzgodnienia. Stosować tekstowy cennik i sprawdzać nagłówek w szerokości tabletu. Wizualny kierunek pozostaje opisany jako szkic w [design systemie](../../../design/design-system.md); audyt nie projektuje nowego interfejsu.
