# rivé — Product & Engineering Roadmap

**Uzgodniono 2026-11-25.** rivé to platforma dla własnej firmy właściciela, łącząca stronę i sprzedaż online, operacje obiektu, obsługę gości i finanse. Projektujemy współpracę modułów, danych i interfejsów dla całej platformy. Dostarczamy ją etapami, zgodnie z zależnościami. Day SPA jest jednym z modułów i dobrze opisanym przypadkiem do sprawdzania decyzji przekrojowych.

Roadmapa ustala kolejność i warunki zakończenia faz. Bieżącą fazę i punkt wznowienia zapisujemy w [PROJECT-STATUS.md](PROJECT-STATUS.md). Reguły biznesowe są w [dokumentacji produktu](product/capability-map.md), decyzje architektoniczne w [ADR](decisions/README.md), a zadania w [GitHub Issues](https://github.com/MateuszGacek/rive-platform/issues).

## Fazy i warunki przejścia

| Faza | Cel i zakres | Zależność, rezultat i kryterium zakończenia |
| --- | --- | --- |
| **0 · Knowledge & Discovery** | Zebrać wiedzę o obiekcie, materiały historyczne i obserwacje Cezara. | Z repozytorium, audytów i Project Brain powstaje indeks źródeł oraz luk. Właściciel wskazuje, które braki trzeba uzupełnić. |
| **1 · Product Vision & Scope** | Określić cele, użytkowników, priorytety i granice platformy. | Po przeglądzie źródeł właściciel zatwierdza wizję, zakres obiektu, główne ścieżki użytkowników i priorytety biznesowe. |
| **2 · Business & Domain Discovery** | Przejść 15 obszarów, ustalić reguły, wyjątki i zależności. | Punktem wyjścia są wizja i mapa możliwości. Właściciel zatwierdza reguły i scenariusze przekrojowe oraz rozstrzyga pytania blokujące architekturę. |
| **3 · Product Architecture** | Ustalić granice strony, dashboardu, portalu gościa, CMS, CRM i domen. | Na podstawie przebiegów biznesowych właściciel zatwierdza podział aplikacji, odpowiedzialność domen i systemy wiodące. |
| **4 · Technical Architecture** | Porównać frontend, backend, bazę, API, repozytorium, logowanie, integracje i hosting. | Na podstawie granic produktu i potrzeb jakościowych właściciel zatwierdza decyzje w ADR po porównaniu aktualnych alternatyw, kosztów i utrzymania. |
| **5 · Data Architecture** | Zaprojektować model domenowy, cykle życia, kontrakty, spójność, import, eksport i retencję. | Po ustaleniu granic odpowiedzialności właściciel akceptuje model i reguły zarządzania danymi. Przykłady obejmują współbieżne rezerwacje, wpłaty i korekty. |
| **6 · UX & Design System** | Opracować architekturę informacji, nawigację, kluczowe przebiegi, współdzielone tokeny i komponenty, mobile i dostępność. Rozstrzygnąć zakres PWA. | Po określeniu aplikacji i ról właściciel zatwierdza przebiegi oraz podstawy reużywalnego design systemu. |
| **7 · Engineering & Quality Strategy** | Ustalić standardy kodu, SEO, i18n, analitykę, prywatność, bezpieczeństwo, wydajność, testy, CI/CD i środowiska. | W oparciu o architekturę, dane i UX właściciel zatwierdza kryteria jakości, unit/integration/contract/E2E, testy wizualne i obciążeniowe adekwatne do ryzyka oraz monitoring, kopie i odtwarzanie. |
| **8 · Agent Development System** | Ustalić podział pracy agentów, specyfikacje, kontekst, integrację zmian i niezależne review. | Po ustaleniu granic i jakości właściciel zatwierdza sposób dostawy. Przykładowe zadanie można wznowić i zweryfikować na podstawie repozytorium. |
| **9 · Delivery Roadmap** | Wyznaczyć zależności implementacyjne, kamienie milowe, MVP, V1 i dalsze wydania. | Po akceptacji fundamentów z faz 2–8 właściciel zatwierdza kolejność, zakres pierwszej dostawy i kryteria odbioru. Zadania korzystają z GitHub Issues/Projects. |
| **10 · Implementation** | Zbudować fundamenty i kolejne działające przebiegi end-to-end. | Właściciel osobno otwiera development po zatwierdzeniu dostawy. Odbiór każdego przebiegu opiera się na specyfikacji, testach i review adekwatnym do ryzyka. |
| **11 · Production & Operations** | Przeprowadzić ewentualną migrację, wdrożenie, monitoring i utrzymanie. | Po odbiorze kodu i próbie odzyskiwania właściciel zatwierdza start produkcji, procedurę wycofania oraz odpowiedzialność za utrzymanie. |

Zgodę na przejście między fazami zapisujemy w punkcie wznowienia wraz z datą, decyzją właściciela, odsyłaczami do rezultatów i zakresem otwieranej fazy. Właściciel może dopuścić wcześniejszą analizę konkretnego zagadnienia z kolejnej fazy. POC wymaga osobnej zgody, pytania do sprawdzenia i określonego zakresu. Wnioski z modułu lub POC zasilają dalsze decyzje. Rozpoczęcie developmentu wymaga osobnej decyzji.

## Rundy discovery

Wykorzystujemy istniejącą [mapę 15 obszarów](product/capability-map.md) i [pytania D-01–D-13](product/open-questions.md). Dla każdego obszaru uzupełniamy użytkowników, funkcje, zaakceptowane reguły, wyjątki, zależności i możliwy rozwój w istniejących źródłach. Właściciel rozstrzyga decyzje bezpośrednio. Obserwację, warsztat lub demo dobieramy do konkretnej luki w wiedzy.

| Runda | Obszary i przedmiot analizy |
| --- | --- |
| **Oferta i sprzedaż** | **01–04.** Public web i CMS, katalog i taryfy, rezerwacje i dostępność, Day SPA, masaże, pakiety, wydarzenia i vouchery. |
| **Gość i operacje** | **05–09.** Tożsamość i komunikacja, recepcja i rachunek, gastronomia i POS, personel, sprzątanie i usterki. |
| **Pieniądze i dostęp** | **10–12.** Płatności, fiskalizacja i korekty, definicje finansowe i rentowność, role, uprawnienia i ślad działań. |
| **Systemy i ciągłość** | **13–15.** Integracje i własność danych, import, eksport, ewentualna migracja, retencja, obsługa awarii i odzyskiwanie pracy. |

Plan pracy dla konkretnego obszaru i kryteria odbioru rozwijamy w [planie pracy agentów](product/agent-delivery-plan.md). Złożone decyzje przechowujemy przy swoich źródłach, po zatwierdzeniu przez właściciela.
