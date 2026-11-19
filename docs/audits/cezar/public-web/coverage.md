# Pokrycie, dowody i ograniczenia

**Data obserwacji:** 2026-11-19. **Zakres:** publiczna strona sauna-cezar.pl, publiczny widok rezerwacji noclegu na panel.sauna-cezar.pl oraz bezpieczne odnośniki z tych widoków. Dashboard, strefa konta i procesy po wysłaniu danych są poza zakresem.

## Liczby

| Element | Wynik |
| --- | ---: |
| Unikalne adresy treści w odkrytej kolejce | 47 |
| Odwiedzone adresy treści | 47/47, każdy HTTP 200 |
| Widok panelu rezerwacji HTTPS | 1, HTTP 200 |
| Stare linki pokoi z panelu sprawdzone na odpowiednikach HTTPS | 8/8, HTTP 404 |
| Standardowy sitemap.xml | HTTP 404 |
| robots.txt | Dostępny |
| Formularze wysłane / rezerwacje / płatności | 0 / 0 / 0 |

Adresy z parametrami i fragmentami scalono. /restauracja oraz /node/15 pokazują tę samą treść, ale odnotowano oba adresy, ponieważ oba występują w nawigacji. Angielską wersję strony głównej odwiedzono jako próbkę; podstron /en/... nie liczono ponownie jako osobnych widoków.

## Rejestr dowodów

| ID | Dowód i metoda | Wspiera |
| --- | --- | --- |
| E01 | Snapshot DOM, Network i Console każdej z [47 stron](site-map.md), zapisane w prywatnym workspace audytu. | Mapa, funkcje, formularze, statusy i powtarzające się problemy Console. |
| E02 | [Strona główna](https://sauna-cezar.pl/) i [panel HTTPS](https://panel.sauna-cezar.pl/rezerwacja-zewnetrzna): odczyt linku HTTP, próba otwarcia HTTP i otwarcie HTTPS. | I-01, ścieżka noclegowa. |
| E03 | Snapshot panelu i otwarcie ośmiu odpowiedników HTTPS starych linków .html; wszystkie 404. | I-02. |
| E04 | [Cennik](https://sauna-cezar.pl/cennik): snapshot DOM oraz oględziny desktop/mobile po przewinięciu. | I-03, struktura taryf, lazy loading. |
| E05 | [Lista wydarzeń](https://sauna-cezar.pl/wydarzenia), [Sylwester](https://sauna-cezar.pl/node/130) i [wydarzenie 2027](https://sauna-cezar.pl/node/126): snapshot i oględziny. | I-05, I-06. |
| E06 | Emulacja strony głównej 390 × 844 i 768 × 1024, kliknięcie menu oraz podmenu „Nocleg”; oględziny panelu 390 px. | Nawigacja mobilna, I-09 i UX panelu. |
| E07 | Odpowiedź dokumentu HTML strony głównej i pięciu podstron: title, canonical, meta description; Network /sitemap.xml i /robots.txt. | I-07, I-08, SEO. |
| E08 | Nowy izolowany kontekst Chrome: start bez banera, potem [kontakt](https://sauna-cezar.pl/kontakt) z iframe Google Maps i 21 żądaniami do usług map. | I-10, obserwacja mechanizmu zgód. |
| E09 | Lighthouse snapshot mobilnej strony głównej: Accessibility 73, Best Practices 83, SEO 67; dziewięć niezaliczonych audytów. | I-04 oraz obserwacje techniczne. |
| E10 | Console panelu HTTPS: błąd inicjalizacji reCAPTCHA oraz uwagi dotyczące etykiet i autocomplete. | I-11. |

Prywatne surowe snapshoty i wyniki Console są w workspace audytu. Publiczne raporty zawierają tylko ustalenia i odnośniki do publicznych stron; nie zawierają danych klientów, kluczy z żądań, zrzutów formularzy ani pełnych logów.

## Druga kontrola

- **OBSERVED:** kolejka odkrytych bezpiecznych adresów treści jest pusta po 47 wizytach; trzy rozwijane gałęzie menu i linki z treści zostały uwzględnione.
- **OBSERVED:** przetestowano desktop, tablet i mobile oraz rozwinięcie menu mobilnego.
- **OBSERVED:** przejścia do oferty, kontaktu, noclegu, panelu, promocji i wydarzeń opisano w [user-journeys.md](user-journeys.md).
- **OBSERVED:** każdy problem w [issues.md](issues.md) ma URL, wynik narzędzia lub konkretny widok jako dowód.
- **OBSERVED:** statusy OBSERVED, INFERRED i PROPOSED są rozdzielone w raportach.

## Niezweryfikowane obszary

- Nie wysyłano formularzy, zapytań o dostępność, rezerwacji, rejestracji ani płatności. Nie potwierdzono wiadomości e-mail, walidacji serwera, cen w kolejnych krokach, anulowania, salda voucherów i integracji z recepcją.
- Oryginalne linki HTTP z panelu były blokowane w testowanym Chrome. Dla starych adresów sprawdzono odpowiedniki HTTPS; zachowanie HTTP w innych przeglądarkach wymaga osobnej próby.
- Nie audytowano wszystkich podstron angielskich, galerii jako osobnych plików, stron społecznościowych, logowania ani obszaru dashboardu.
- Lighthouse wykonano na mobilnej stronie głównej, nie na całym serwisie. Nie przeprowadzono pełnego testu czytnikiem ekranu, testu klawiaturą dla wszystkich widoków, pomiarów wydajności ani oceny prawnej cookies.
- Odkrywanie bazowało na menu, stopce i linkach dostępnych w snapshotach. Nie można wykluczyć niepodlinkowanych stron CMS lub treści ujawnianych dopiero po interakcji wymagającej wysłania danych.

**INFERRED:** pokrycie jest kompletne dla odkrytej, bezpiecznej kolejki, ale nie stanowi 100% całej możliwej zawartości serwisu.
