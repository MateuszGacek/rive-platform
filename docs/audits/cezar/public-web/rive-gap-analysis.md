# Analiza luk: Cezar → rivé Public Web

**Podstawa — 2026-11-19.** Cezar to obserwowany serwis; rivé jest w fazie discovery. „Potwierdzone” niżej oznacza intencję lub możliwość zapisaną przez właściciela, nie zatwierdzone MVP ani projekt techniczny. Źródła: [wizja](../../../product/vision.md), [mapa możliwości](../../../product/capability-map.md), [ustalenia noclegowe](../../../discovery.md#wywiad-z-właścicielem--oferta-noclegowa-2026-11-19), [ustalenia wejść](../../../product/reception-discovery.md#day-spa-bez-noclegu) i [design system](../../../design/design-system.md).

| Obszar | OBSERVED: obecny serwis | Potwierdzony kierunek rivé | Luka / następny krok |
| --- | --- | --- | --- |
| Noclegi online | Opisy dziewięciu jednostek + kemping; osobny panel z datami, liczbą osób i kalendarzem. Nie badano finalizacji. | WEB-02/05 oraz BKG-01–03: oferta, dostępność i rezerwacja online ze wspólną pulą dla WWW i recepcji. | **PROPOSED:** powiązać opis opcji z jej dostępnością i zachować wybór podczas przejścia do rezerwacji. Reguły zmiany, anulowania i taryf rozstrzyga D-03. |
| Nocleg bez dostępu i pakiet | Grafika cennika rozdziela nocleg i dopłatę za ośrodek; panel nie pokazał w badanym widoku jawnego wyboru wariantu dostępu. | CAT-01 i EVT-03: sama jednostka jest bez dostępu; pakiet może obejmować cały pobyt albo pojedyncze wejście, także dla części gości. | **INFERRED:** informacja handlowa istnieje, lecz brak potwierdzonej spójnej konfiguracji pakietu w publicznej ścieżce. **PROPOSED:** w discovery sprawdzić wycenę jednostki, liczbę osób z dostępem i dostępność składowych. |
| Wejścia godzinowe | Cennik przedstawia taryfy godzinowe; strona każe rezerwować wstęp telefonicznie. Nie znaleziono formularza zakupu wejścia. | EVT-05/06: rezerwacja przez WWW bez konta, wspólna pula ośrodka i pomiar faktycznej obecności; domyślnie dwie godziny, rozliczenie przy wyjściu. | **PROPOSED:** opisać ścieżkę wyszukania terminu, komunikat o pojemności i potwierdzenie bez przedpłaty zgodnie z potwierdzonym procesem. Szczegóły taryf i wyjątków pozostają w D-04. |
| Gastronomia i dodatki | Restauracja opisuje ofertę, a SPA usługi; brak zaobserwowanego zamówienia online lub wyboru terminu zabiegu. | POS-01/02 i EVT-02: katalog gastronomii, zakupy na właściwym rachunku, dostępność usług SPA zależna od zasobów. | **PROPOSED:** zachować osobne odkrywanie oferty i procesu zakupu; nie zakładać, że wszystkie dodatki muszą być sprzedawane na stronie w pierwszym wydaniu. |
| Vouchery i wydarzenia | Bon jest uzgadniany przez kontakt; wydarzenia mają osobne wpisy, głównie z rezerwacją telefoniczną. | WEB-04 i EVT-04: okresowa publikacja; sprzedaż, saldo voucherów i rezerwacje grupowe jako potwierdzony kierunek, zasady otwarte. | **PROPOSED:** najpierw ustalić model oferty i publikacji; nie kopiować pustych wpisów ani błędnych dat. |
| Strona i treści | Drupal, menu wielopoziomowe, galerie i cennik w grafikach. Lighthouse mobile: Accessibility 73, SEO 67. | WEB-01: szybka strona z edycją treści; [design system v0.1](../../../design/design-system.md) opisuje paletę i zasady kontrastu, a decyzja o CMS jest otwarta. | **PROPOSED:** uporządkować semantyczny HTML, tekstowy cennik, CTA i proces publikacji. Nie wybierać CMS ani frameworka na podstawie samego audytu. |

## Granice wnioskowania

**OBSERVED.** W HTML panelu są zasoby Autopay i reCAPTCHA, ale nie badano płatności, kont, potwierdzeń e-mail ani zapisu w recepcji.

**INFERRED.** Obecna strona dostarcza treści i punktów kontaktu, lecz nie jest dowodem na spełnienie potwierdzonych reguł wspólnej dostępności, zaliczek, wejść czasowych i pakietów.

**PROPOSED.** Do dalszego discovery przenieść konkretne pytania D-03/D-04: źródło dostępności, reguły taryf, blokady noclegów, zestawianie pakietu oraz pojemność wejść. Ten raport nie zatwierdza funkcji, architektury ani kolejności wdrożenia.
