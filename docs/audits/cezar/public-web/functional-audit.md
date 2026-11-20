# Audyt funkcjonalny i oferta

**Zakres:** publiczna strona Cezar, stan zaobserwowany 2026-11-19 w Chrome DevTools MCP. Etykiety opisują status twierdzeń, a nie decyzję produktową. [Mapa adresów](site-map.md) · [Pokrycie](coverage.md).

## Nawigacja i kontakt

**OBSERVED.** Menu główne prowadzi do cennika, wydarzeń i promocji oraz rozwija grupy „Poznaj nas”, „Nocleg” i „Info&Kontakt”. Stopka ma regulamin, telefon, e-mail i formularz newslettera. Na [kontakcie](https://sauna-cezar.pl/kontakt) są pola imię i nazwisko, e-mail oraz treść wiadomości, a także mapa Google. W badaniu nie wysłano żadnego formularza.

**OBSERVED.** Nagłówek wymaga wcześniejszej rezerwacji telefonicznej na wstęp. Formularz kontaktowy i newsletter istnieją, lecz nie było podstaw do potwierdzenia dostarczenia wiadomości ani zapisu.

## Noclegi i sprzedaż

**OBSERVED.** Menu prezentuje dziewięć stron jednostek noclegowych: [domek](https://sauna-cezar.pl/domek-w-lesie), [apartament](https://sauna-cezar.pl/apartament), [pokój z sauną](https://sauna-cezar.pl/pokoj-z-sauna), [pokój standard](https://sauna-cezar.pl/pokoj-standard), [chatkę beskidzką](https://sauna-cezar.pl/chatka-beskidzka), [Lux](https://sauna-cezar.pl/lux), [pokój z grillem](https://sauna-cezar.pl/pokoj-z-grillem), [studio](https://sauna-cezar.pl/studio) i [apartament z kotem](https://sauna-cezar.pl/apartament-z-kotem). Jest też [kemping](https://sauna-cezar.pl/kemping). Strony opisują wyposażenie i pokazują galerie. Nie mają widocznego w głównej treści przycisku rezerwacji konkretnego typu.

**OBSERVED.** Strona główna i podmenu „Nocleg” linkują do zewnętrznego [panelu dostępności](https://panel.sauna-cezar.pl/rezerwacja-zewnetrzna) przez adres HTTP. Wariant HTTPS otwiera formularz dat przyjazdu i wyjazdu, wybór 1–10 osób oraz kalendarz typów noclegu. Panel pokazuje login/rejestrację oraz informacje o anulowaniu. Badanie zatrzymało się przed „Sprawdź termin”, rejestracją i rezerwacją. Osiem linków do opisów pokoi w panelu wskazuje stare adresy HTTP z końcówką .html; ich warianty HTTPS dały 404.

**OBSERVED.** [Cennik](https://sauna-cezar.pl/cennik) przedstawia osobno wejścia godzinowe, dopłatę za dostęp do ośrodka przy noclegu, nocleg bez dostępu i kemping. Stawki są naniesione na grafiki; snapshot tekstowy nie odczytuje tych stawek. Nie utrwalono kwot w raporcie, bo mogą się zmieniać.

## Ośrodek i usługi

**OBSERVED.** Dostępne są strony [sauny](https://sauna-cezar.pl/sauna), [basenu](https://sauna-cezar.pl/basen), [jacuzzi](https://sauna-cezar.pl/jacuzzi), ogrodu, altany, ogniska, gier i pola golfowego. [Masaże](https://sauna-cezar.pl/masaze) opisują pięć rodzajów masażu, a [zabiegi](https://sauna-cezar.pl/zabiegi) dwa rytuały. Strony jogi, gimnastyki w wodzie i wycieczek górskich zawierają opisy zajęć. Nie znaleziono publicznego formularza rezerwacji wejścia godzinowego ani terminu zabiegu na tych stronach.

**OBSERVED.** [Restauracja](https://sauna-cezar.pl/restauracja) wymienia kategorie jedzenia i napojów oraz informuje o przygotowywaniu dań na świeżo. Nie ma widocznego zamówienia online. [Bony prezentowe](https://sauna-cezar.pl/bony-prezentowe) opisują kupon o wartości do ustalenia i kierują do kontaktu, bez koszyka lub płatności.

**OBSERVED.** [Promocje](https://sauna-cezar.pl/pakiety) obejmują „Pierwszy raz za darmo”, „Ranne ptaszki” i „Promocję wieczorną”. Pierwsza prowadzi do [formularza](https://sauna-cezar.pl/pierwszy-raz-za-darmo) z polami imię, nazwisko, miasto, telefon, e-mail, wyborem newslettera i opcjonalnym hasłem do konta rezerwacyjnego. Formularza nie wysłano. Pozostałe promocje opisują czas i cenę, bez bezpośredniego zakupu.

**OBSERVED.** [Lista wydarzeń](https://sauna-cezar.pl/wydarzenia) zawiera trzy wpisy. Dwa opisy wskazują rezerwację telefoniczną; [trzeci](https://sauna-cezar.pl/node/126) ma pustą treść pomimo widocznego wpisu na liście. Data przy „Sylwestrze 2026” ma zakres 31.12.2026–31.12.2025.

## Interpretacja dla rivé

**INFERRED.** Obecny serwis jest głównie katalogiem treści z osobnym kalendarzem noclegowym. Nie potwierdzono kompletnego zakupu wejścia, pakietu, vouchera, gastronomii ani SPA przez WWW. Sam fakt obecności ikon Autopay w panelu nie potwierdza skutecznego procesu płatności.

**PROPOSED.** Przy projektowaniu rivé zachować rozróżnienie „nocleg bez dostępu” oraz „nocleg + dostęp”, a ścieżki sprzedaży zdefiniować na podstawie zatwierdzonych reguł w [mapie możliwości](../../../product/capability-map.md). Nie kopiować automatycznie starych typów pokoi, taryf ani zasad panelu bez potwierdzenia przez właściciela.
