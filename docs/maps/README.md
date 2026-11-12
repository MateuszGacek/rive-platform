# Mapa produktu — Obsidian Canvas

**Board:** [rive-product-map.canvas](rive-product-map.canvas)  
**Kanon opisów i statusów biznesowych:** [capability-map.md](../product/capability-map.md)

## Jak otworzyć

1. Sklonuj repozytorium na komputer. Dopóki PR #2 jest szkicem, przełącz się na gałąź `docs/discovery-business-areas`.
2. Otwórz **Obsidian → Open folder as vault** i wybierz folder `rive-platform`.
3. Włącz wbudowaną wtyczkę **Canvas** (jeśli jest wyłączona).
4. Otwórz `docs/maps/rive-product-map.canvas` i użyj **Zoom to fit**.
5. Przesuwaj karty, grupuj, dodawaj nowe wątki. Karty z plikami prowadzą do rozdziałów `capability-map.md`.

## Do czego służy

- **Canvas**: wizualne rozłożenie funkcji i relacji; można go edytować ręcznie.
- **Markdown**: zatwierdzane wymagania, reguły, niejasności i fakty. To główne źródło wiedzy dla agentów.
- **GitHub Projects** (później): epiki, Issues i faktyczny postęp implementacji. Nie kopiuj statusów wdrożenia do Canvas.
- **OpenSpec** (później): szczegółowy opis zmian, które mają zostać zaimplementowane.

Obecna mapa jest **ręcznym, edytowalnym widokiem** zbudowanym z danych discovery, nie automatycznie aktualizowanym diagramem. Po istotnej zmianie listy możliwości lub zależności aktualizujemy **Markdown i Canvas w tym samym PR**. Same przesunięcia wizualne nie wymagają aktualizacji Markdown.

Nie trzeba tworzyć osobnego dokumentu na każdą kartę. Gdy dany obszar stanie się wystarczająco złożony, można utworzyć osobną notatkę i/lub podrzędny Canvas i powiązać go z mapą ogólną.

## Statusy i interpretacja

- ✅ **Wymagane** — właściciel wskazał cel dla przyszłego produktu; to nie oznacza ukończonej implementacji.
- 🔎 **Do weryfikacji** — hipoteza, wariant lub wcześniejsza idea do potwierdzenia.
- ❓ **Do wyjaśnienia** — kwestia otwarta, najpierw rozmawiamy o procesie.

Kolory służą orientacji; **status określa tekst i dokumentacja**, nie sam kolor.

## Praca z agentami

Agent ma dostęp do plików Git. Przed planowaniem danego obszaru powinien przeczytać `AGENTS.md`, `docs/product/capability-map.md` i odpowiedni fragment `docs/discovery.md`. JSON Canvas jest dodatkową mapą wizualną zależności. Nie należy wyciągać z samej strzałki wniosku, że decyzja architektoniczna została zatwierdzona.

Canvas jest zwykłym plikiem JSON (format JSON Canvas 1.0). GitHub nie zapewnia dla niego takiego edytora wizualnego jak Obsidian. Aby zobaczyć i przesuwać karty, otwórz go lokalnie w Obsidianie, a zmiany commituj do repo.

**Uwaga:** repozytorium jest publiczne. Nie wstawiaj do kart danych prawdziwych gości, personelu, tajnych cen ani innych poufnych informacji.
