---
tags: uni dsa practical-cs graph bipartit
cards-deck: Uni::Courses::DSA
completed: true
aliases: Matching
linter-yaml-title-alias: Matching
date-of-creation: 2022-07-24
mod-date: 2022-09-03
---

# Matching

## Definition: #fc
- Die Kantenmenge $M\subseteq E$ heißt Matching, wenn
	- $M$ *keine Schleifen* enthält und
	- die Kantenmenge $M$ *inzident* ist (=kein *Knoten* in zwei Kanten *doppelt* vorkommen)
^1655391191119

## Varianten: #fc
- **Gesättigtes Matching**: $M_0(G)$ ist gesättigt, wenn es kein $M$ gibt mit $M_0 \subsetneq M \wedge M_0 \neq M$
	→ $M_0$ nicht erweiterbar ist
- **Maximum Matching**: Für das Matching $M$ gibt es kein Matching $M'\text{ mit }|M|<|M'|$
	→ $M$ beinhaltet die größtmögliche Kantenzahl
- **Maximales [[Bipartite Graphen|Bipartite Graphen]]-Matching**: Es ist $S \subseteq A \times B$ für $G=(A\cup B,E)$ gesucht, so dass $S$ ein *maximales Matching* ist
	→ [[Algorithmen/Ungarische Methode|Ungarische Methode]]
	→ Alternativ: Der [[Algorithmen/Ford-Fulkerson|Ford-Fulkerson Algorithmus]] lässt sich auf den maximalen Fluss [[../../../Theo II/Reduktion|reduzieren]]
- **Perfektes Matching**: Für den Graphen $G = (V,E)$ existiert ein Teilgraphen $G_M = (V_M, M)$ mit $V = V_M$
^1655391711309
