---
tags: uni dsa practical-cs struct graph
cards-deck: Uni::Courses::DSA
completed: true
aliases: Knotenliste
linter-yaml-title-alias: Knotenliste
date-of-creation: 2022-07-25
mod-date: 2022-09-05
---

# Knotenliste

## Eigenschaften: #fc
- Der erste Wert zeigt die Anzahl der Knoten an
- Der zweite Wert zeigt die Anzahl der Kanten im Graphen an
- Danach: Der erste Wert gibt die Anzahl der (ausgehenden) Kanten an, danach folgen die Zielknoten in eben dieser Anzahl
→ Benötigt bei dichten Graphen weniger Speicherplatz als die [[Kantenliste]], bieten dafür aber eine höhere Zeitkomplexität
^1653919478962

## Knoten hinzufügen:
- Der Knotenzähler wird um Eins hochgezählt
- Setze den Knotengrad des neuen Knotens auf 0

## Kante hinzufügen: #fc
- Prüfe, ob beide Knoten existieren
- Erhöhe den Kantenzähler an $F[1]$ um Eins
- Suche die Position des Quell-Knotens im Array und füge den Zielknoten der Kante ein
^1658939232327
