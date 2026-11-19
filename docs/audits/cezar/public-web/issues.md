# Problemy i priorytety

**Stan 2026-11-19.** P0 = krytyczny brak działania potwierdzony w kluczowej ścieżce; P1 = istotny problem sprzedaży lub dostępności; P2 = lokalny błąd albo ryzyko do weryfikacji. **P0: 0 · P1: 4 · P2: 8.** Każda pozycja odwołuje się do obserwacji Chrome; wpływ niezweryfikowanych kroków oznaczono ostrożnie.

## I-01

**P1 — link do kalendarza noclegów używa HTTP.** **OBSERVED:** CTA „Kalendarz wolnych pokoi” na [stronie głównej](https://sauna-cezar.pl/) oraz „Zarezerwuj nocleg” w menu wskazują http://panel.sauna-cezar.pl/rezerwacja-zewnetrzna. Chrome DevTools MCP zwrócił dla tego URL ERR_BLOCKED_BY_CLIENT; [HTTPS](https://panel.sauna-cezar.pl/rezerwacja-zewnetrzna) otworzył panel z HTTP 200. **INFERRED:** schemat HTTP tworzy ryzyko przerwania lub niepotrzebnego przekierowania na kluczowym CTA; wynik nie dowodzi awarii u wszystkich użytkowników. **PROPOSED:** zmienić adresy źródłowe na HTTPS i sprawdzić kliknięcie w zwykłej przeglądarce.

## I-02

**P1 — odnośniki opisów pokoi w panelu wskazują stare ścieżki.** **OBSERVED:** [panel](https://panel.sauna-cezar.pl/rezerwacja-zewnetrzna) pokazuje osiem linków HTTP do starego hosta: /domek.html, /pokoj-z-wanna.html-0, /lux.html, /chatka-beskidzka.html, /pokój-z-grillem.html, /studio.html, /pokoj-z-sauną.html, /apartament.html. Każdy odpowiednik HTTPS dał HTTP 404 w teście. Link „Nadlux” prowadzi z powrotem do panelu. **INFERRED:** z kalendarza trudno wrócić do aktualnych opisów jednostek; zachowanie pierwotnych odnośników HTTP poza testowanym Chrome pozostaje niezweryfikowane. **PROPOSED:** podmienić odnośniki na aktualne kanoniczne URL i sprawdzić całą tabelę.

## I-03

**P1 — stawki cennika są wyłącznie na grafikach.** **OBSERVED:** [cennik](https://sauna-cezar.pl/cennik) wizualnie pokazuje taryfy wejść, noclegów i pakietów w czterech obrazach; snapshot DOM ma H1 i pustą treść główną. **INFERRED:** użytkownik czytnika ekranu i wyszukiwarka nie otrzymują tekstu stawek; kopiowanie i aktualizacja cen są utrudnione. **PROPOSED:** opublikować ceny jako semantyczne tabele/listy HTML, a obrazy zostawić dekoracyjne.

## I-04

**P1 — systemowe problemy dostępności w nagłówku i formularzach.** **OBSERVED:** mobilny Lighthouse strony głównej dał Accessibility 73; wykazał brak lang na html, nazwy przycisku menu, alt trzech obrazów, wystarczającego kontrastu, poprawnego aria-expanded i powiązanej etykiety newslettera. Konsola powtarza błąd label na podstronach. **INFERRED:** nawigacja i treści mogą być trudne dla użytkowników technologii asystujących. **PROPOSED:** poprawić wskazane elementy, a potem ponownie ocenić klawiaturę i czytnik ekranu na reprezentatywnych widokach.

## I-05

**P2 — opublikowane wydarzenie ma pusty widok szczegółowy.** **OBSERVED:** [lista wydarzeń](https://sauna-cezar.pl/wydarzenia) linkuje do [wydarzenia 2027](https://sauna-cezar.pl/node/126); adres zwraca 200, ale main jest pusty w snapshot i na ekranie. **PROPOSED:** uzupełnić treść albo wycofać wpis z listy do czasu publikacji.

## I-06

**P2 — niespójna data Sylwestra.** **OBSERVED:** [lista wydarzeń](https://sauna-cezar.pl/wydarzenia) pokazuje „31.12.2026 - 31.12.2025” przy „Sylwestrze 2026”. **PROPOSED:** skorygować datę końcową po sprawdzeniu źródła wydarzenia.

## I-07

**P2 — standardowa ścieżka sitemap zwraca 404.** **OBSERVED:** [sitemap.xml](https://sauna-cezar.pl/sitemap.xml) zwróciła HTTP 404, podczas gdy [robots.txt](https://sauna-cezar.pl/robots.txt) jest dostępny. **PROPOSED:** ustalić właściwą mapę strony, opublikować ją i wskazać w robots.txt. Nie wnioskować, że mapa nie istnieje pod innym adresem.

## I-08

**P2 — brak meta description na próbkowanych stronach.** **OBSERVED:** w HTML strony głównej, cennika, kontaktu, wydarzeń, szczegółu wydarzenia i formularza promocji jest title i canonical, ale brak meta description. Lighthouse strony głównej również zgłasza ten brak. **PROPOSED:** dodać opis dopasowany do strony i sprawdzić szablony treści.

## I-09

**P2 — konflikt elementów nagłówka przy 768 px.** **OBSERVED:** na tablecie zielony komunikat o rezerwacji nachodzi na logo na [stronie głównej](https://sauna-cezar.pl/), także po przeładowaniu. **PROPOSED:** poprawić układ nagłówka dla pośrednich szerokości i sprawdzić 768 px oraz sąsiednie rozmiary.

## I-10

**P2 — mapa ładuje się bez widocznej decyzji o cookies.** **OBSERVED:** w nowym, izolowanym kontekście nie było banera zgody; [kontakt](https://sauna-cezar.pl/kontakt) automatycznie pobrał 21 żądań do Google Maps. **INFERRED:** warto zweryfikować zgodność tego zachowania z aktualną polityką prywatności i wymogami zgody; audyt nie rozstrzyga kwestii prawnej. **PROPOSED:** wspólnie z osobą odpowiedzialną za prywatność ustalić, czy mapa wymaga odroczenia lub jawnej informacji.

## I-11

**P2 — błąd reCAPTCHA w konsoli panelu.** **OBSERVED:** Console [panelu rezerwacji](https://panel.sauna-cezar.pl/rezerwacja-zewnetrzna) zgłasza „reCAPTCHA placeholder element must be an element or id”. **INFERRED:** możliwy wpływ na formularze wymagające CAPTCHA, lecz nie potwierdzono go bez wysyłania danych. **PROPOSED:** odtworzyć w środowisku testowym i naprawić inicjalizację.

## I-12

**P2 — opis jednostki nie prowadzi bezpośrednio do jej rezerwacji.** **OBSERVED:** na stronach pokoi, np. [Studio](https://sauna-cezar.pl/studio), w głównej treści są opis i galeria, ale nie ma CTA do kalendarza konkretnego typu. Ogólny link jest w menu lub na stronie głównej. **INFERRED:** wybór pokoju gubi kontekst przed przejściem do panelu. **PROPOSED:** dodać bezpośredni krok „sprawdź dostępność” z zachowaniem wybranej opcji.
