# Audyt techniczny

**Metoda — 2026-11-19.** Chrome DevTools MCP: snapshot dostępności, Network i Console dla 47 adresów, wgląd w odpowiedź HTML wybranych stron, emulacja 390/768 px oraz Lighthouse w trybie snapshot dla mobilnej strony głównej. Nie wykonano testu obciążenia, pomiaru Core Web Vitals ani skanowania podatności. [Pokrycie](coverage.md).

## DOM i dostępność

**OBSERVED.** Strona główna ma obszary banner, navigation, main i contentinfo, ale promuje sekcje nagłówkami poziomu 4 bez widocznego H1 w snapshot. Cennik ma H1, podczas gdy same stawki są obrazami i nie pojawiają się w drzewie tekstowym. Galerie pokoi wystawiają przyciski o nazwach przypominających ciąg JSON zamiast opisu zdjęcia.

**OBSERVED.** Lighthouse mobile snapshot strony głównej: Accessibility 73, Best Practices 83, SEO 67. Niepowodzenia obejmują brak atrybutu lang na html, brak alt dla trzech obrazów, zbyt niski kontrast, brak nazwy przycisku menu mobilnego, niepoprawne aria-expanded na elementach span rozwijanego menu i brak powiązanej etykiety pola newslettera. Konsola strony głównej zgłasza też brak jawnych wymiarów 17 obrazów lazy-loaded oraz niepoprawne użycie label; analogiczne komunikaty powtarzają się na podstronach.

**OBSERVED.** Formularz kontaktowy oznacza imię/nazwisko i e-mail jako wymagane, ale nie oznacza treści wiadomości jako wymaganej po stronie klienta. Formularz promocji wymaga pięciu danych oraz wyboru newslettera. Nie uruchamiano walidacji wysłaniem formularzy, więc nie potwierdzono odpowiedzi serwera, antyspamu ani dostarczania powiadomień.

## Network, Console i integracje

**OBSERVED.** Wszystkie 47 stron treści zwróciły HTTP 200. W zebranych listach żądań tych stron nie pojawił się status 4xx/5xx; część zasobów mapy kontaktowej pozostawała oznaczona jako pending w chwili odczytu. Strona główna wykonała 119 żądań, kontakt 135 w testowanym przebiegu. To liczba żądań, nie miara czasu ładowania.

**OBSERVED.** Panel noclegowy działa pod HTTPS i wykonał 58 żądań w jednej obserwacji. Ładuje Google reCAPTCHA i zasoby Autopay. Console zawiera błąd „reCAPTCHA placeholder element must be an element or id” oraz problemy z etykietami/autocomplete. Nie sprawdzano, czy błąd blokuje konkretną akcję. W panelu jest osiem linków do dawnych adresów HTTP .html; ich odpowiedniki HTTPS zwracają 404.

**OBSERVED.** Strona kontaktu automatycznie osadza mapę Google. W czystym, izolowanym kontekście przeglądarki nie pojawił się baner cookies, a Network pokazał 21 żądań do usług map. To obserwacja zachowania; kwalifikacja prawna i zasady zgody wymagają osobnej oceny.

## SEO i indeksowanie

**OBSERVED.** Strona główna i pięć próbkowanych podstron (cennik, kontakt, wydarzenia, wydarzenie szczegółowe, formularz promocji) mają title i canonical, ale nie mają meta description w nagłówku HTML. Tytuł strony głównej brzmi „Home | SAUNA CEZAR”. Odpowiedź HTML ujawnia meta Generator „Drupal 9”.

**OBSERVED.** robots.txt jest dostępny i wyklucza ścieżki administracyjne/systemowe. /sitemap.xml zwraca HTTP 404. Nie wykazano, czy istnieje mapa pod inną ścieżką. Wydarzenie /node/126 ma HTTP 200, lecz pusty main, co może utrudniać odkrycie treści użytkownikom i robotom.

## Responsive i wydajność obserwowalna

**OBSERVED.** Przy 390 px menu zwija się do przycisku i pozwala rozwinąć podmenu „Nocleg”. Cennik układa grafiki w jednej kolumnie; dolny obraz ładuje się po przewinięciu. Przy 768 px tekst zielonego komunikatu rezerwacji nachodzi na logo w nagłówku. Panel rezerwacji na 390 px pokazuje formularz i fragment szerokiej tabeli kalendarza, która wymaga poziomego dostępu do dalszych dat.

**INFERRED.** Obrazy cennika ograniczają dostępność, indeksowanie i łatwe aktualizowanie stawek. Liczba żądań oraz zgłoszenia o obrazach uzasadniają pomiar rzeczywistej wydajności, ale same nie dowodzą wolnego działania.

**PROPOSED.** Przenieść krytyczne informacje cenowe do HTML, naprawić elementy dostępności wskazane przez Lighthouse, udokumentować reguły osadzania mapy i zastąpić stare linki panelu aktualnymi HTTPS. W rivé oceniać wydajność na rzeczywistych urządzeniach po ustaleniu architektury; [design system](../../../design/design-system.md) określa docelowe progi kontrastu.
