# Mapa publicznej strony Cezar

**OBSERVED — 2026-11-19.** Odkrywanie zaczęto od strony głównej, trzech rozwijanych gałęzi menu oraz linków w treści i stopce. Adresy z parametrami, fragmentami i wariantami językowymi tego samego widoku scalono. Każdy poniższy adres otwarto w Chrome DevTools MCP; wszystkie 47 zwróciły HTTP 200. Szczegóły pokrycia: [coverage.md](coverage.md).

## Strony startowe i język

| Strona | Status i uwaga |
| --- | --- |
| [`/`](https://sauna-cezar.pl/) | 200 |
| [`/en`](https://sauna-cezar.pl/en) | 200; próbka wersji EN |

## Cennik, promocje i vouchery

| Strona | Status i uwaga |
| --- | --- |
| [`/cennik`](https://sauna-cezar.pl/cennik) | 200 |
| [`/pakiety`](https://sauna-cezar.pl/pakiety) | 200 |
| [`/node/121`](https://sauna-cezar.pl/node/121) | 200 |
| [`/node/9`](https://sauna-cezar.pl/node/9) | 200 |
| [`/node/8`](https://sauna-cezar.pl/node/8) | 200 |
| [`/pierwszy-raz-za-darmo`](https://sauna-cezar.pl/pierwszy-raz-za-darmo) | 200; formularz promocji |
| [`/bony-prezentowe`](https://sauna-cezar.pl/bony-prezentowe) | 200 |

## Wydarzenia

| Strona | Status i uwaga |
| --- | --- |
| [`/wydarzenia`](https://sauna-cezar.pl/wydarzenia) | 200 |
| [`/node/129`](https://sauna-cezar.pl/node/129) | 200 |
| [`/node/130`](https://sauna-cezar.pl/node/130) | 200 |
| [`/node/126`](https://sauna-cezar.pl/node/126) | 200; pusta treść wydarzenia |

## Noclegi

| Strona | Status i uwaga |
| --- | --- |
| [`/domek-w-lesie`](https://sauna-cezar.pl/domek-w-lesie) | 200 |
| [`/apartament`](https://sauna-cezar.pl/apartament) | 200 |
| [`/pokoj-z-sauna`](https://sauna-cezar.pl/pokoj-z-sauna) | 200 |
| [`/pokoj-standard`](https://sauna-cezar.pl/pokoj-standard) | 200 |
| [`/chatka-beskidzka`](https://sauna-cezar.pl/chatka-beskidzka) | 200 |
| [`/lux`](https://sauna-cezar.pl/lux) | 200 |
| [`/pokoj-z-grillem`](https://sauna-cezar.pl/pokoj-z-grillem) | 200 |
| [`/studio`](https://sauna-cezar.pl/studio) | 200 |
| [`/apartament-z-kotem`](https://sauna-cezar.pl/apartament-z-kotem) | 200 |
| [`/kemping`](https://sauna-cezar.pl/kemping) | 200 |

## Obiekt, gastronomia i SPA

| Strona | Status i uwaga |
| --- | --- |
| [`/basen`](https://sauna-cezar.pl/basen) | 200 |
| [`/sauna`](https://sauna-cezar.pl/sauna) | 200 |
| [`/jacuzzi`](https://sauna-cezar.pl/jacuzzi) | 200 |
| [`/ogrod`](https://sauna-cezar.pl/ogrod) | 200 |
| [`/altana`](https://sauna-cezar.pl/altana) | 200 |
| [`/ognisko`](https://sauna-cezar.pl/ognisko) | 200 |
| [`/gry-rekreacyjne`](https://sauna-cezar.pl/gry-rekreacyjne) | 200 |
| [`/pole-golfowe`](https://sauna-cezar.pl/pole-golfowe) | 200 |
| [`/gimnastyka-w-wodzie`](https://sauna-cezar.pl/gimnastyka-w-wodzie) | 200 |
| [`/joga`](https://sauna-cezar.pl/joga) | 200 |
| [`/wycieczki-gorskie`](https://sauna-cezar.pl/wycieczki-gorskie) | 200 |
| [`/masaze`](https://sauna-cezar.pl/masaze) | 200 |
| [`/zabiegi`](https://sauna-cezar.pl/zabiegi) | 200 |
| [`/restauracja`](https://sauna-cezar.pl/restauracja) | 200 |
| [`/node/15`](https://sauna-cezar.pl/node/15) | 200; ten sam widok co `/restauracja` |

## Informacje i kontakt

| Strona | Status i uwaga |
| --- | --- |
| [`/kontakt`](https://sauna-cezar.pl/kontakt) | 200 |
| [`/godziny-otwarcia`](https://sauna-cezar.pl/godziny-otwarcia) | 200 |
| [`/dojazd`](https://sauna-cezar.pl/dojazd) | 200 |
| [`/okolica`](https://sauna-cezar.pl/okolica) | 200 |
| [`/polityka-prywatnosci`](https://sauna-cezar.pl/polityka-prywatnosci) | 200 |
| [`/jak-korzystac-z-sauny`](https://sauna-cezar.pl/jak-korzystac-z-sauny) | 200 |
| [`/o-nas`](https://sauna-cezar.pl/o-nas) | 200 |
| [`/naturyzm`](https://sauna-cezar.pl/naturyzm) | 200 |
| [`/node/449`](https://sauna-cezar.pl/node/449) | 200 |

## Adresy powiązane, poza 47 podstronami

- [Publiczny panel rezerwacji noclegu](https://panel.sauna-cezar.pl/rezerwacja-zewnetrzna) — osobny host; HTTPS otwiera kalendarz, daty pobytu i liczbę osób. Link na stronie głównej ma schemat `http`.
- [`/robots.txt`](https://sauna-cezar.pl/robots.txt) — 200; zawiera wykluczenia ścieżek systemowych.
- [`/sitemap.xml`](https://sauna-cezar.pl/sitemap.xml) — 404.
- Osiem starych adresów `.html` podlinkowanych z panelu rezerwacji: odpowiedniki HTTPS zwróciły 404. Lista i metoda w [issues.md](issues.md#i-02).
- Zewnętrzne odnośniki: Facebook, strona wykonawcy oraz panel rezerwacji. Wbudowana mapa kontaktowa pobiera zasoby Google Maps. Zewnętrznych serwisów społecznościowych nie audytowano.
