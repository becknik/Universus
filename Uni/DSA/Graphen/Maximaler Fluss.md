---
tags: uni dsa practical-cs graph flow
cards-deck: Uni::Courses::DSA
completed: true
aliases: Maximaler Fluss
linter-yaml-title-alias: Maximaler Fluss
date-of-creation: 2022-07-26
mod-date: 2022-09-03
---

# Maximaler Fluss

## Definition: #fc
- Berechnung der Werte eines [[Fluss|Flusses]] $F$ im Graphen $G$: $$val(G,F,s) = \sum_{u \in V} f(s,u)$$
	→ $F$ bestimmt den Wert für jede Kante $u$
- So ist der maximale Durchfluss: $$\max\{ val(G, F, s)\mid F \text{ ist ein korrekter Fluss in } G \text{ bezüglich } s,t\}$$
^1655041696342

## Eigenschaften:
- Kann mithilfe vom [[Algorithmen/Ford-Fulkerson|Ford-Fulkerson Algorithmus]] berechnet werden
