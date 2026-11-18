---
type: idea
status: new
area: "15 Inżynieria i ciągłość działania"
source: "Analiza poradnika AI, 2026-11-18"
created: 2026-11-18
updated: 2026-11-18
---

# MCP do odczytu stanu wdrożeń

## Problem

Przy diagnozowaniu nieudanego wdrożenia agent może potrzebować informacji z panelu dostawcy lub logów CI.

## Pomysł

**Proposed** — porównać odczyt stanu i logów przez MCP z odczytem w panelu lub CI. Rozpatrzeć dostęp tylko do odczytu w środowisku testowym. [Przykład w dokumentacji Vercel MCP](https://vercel.com/docs/agent-resources/vercel-mcp)

## Alternatywy

Odczyt przez człowieka w panelu lub udostępnienie agentowi tylko potrzebnego, oczyszczonego fragmentu logu.

## Zależności

[Istniejąca notatka o hostingu przyjaznym agentom](../discovery.md#pomysł-do-oceny--hosting-przyjazny-agentom-2026-11-17) i dostępność ograniczonego dostępu do środowiska testowego.

## Pytania

**Open question** — czy da się oddzielić odczyt logów od operacji na wdrożeniach i czy taka integracja skraca diagnozę?

## Historia

2026-11-18 — zapisano inspirację z analizy poradnika AI.

## Następny krok

Wrócić do oceny, gdy będą znane przyszłe środowiska i potrzebne uprawnienia.
