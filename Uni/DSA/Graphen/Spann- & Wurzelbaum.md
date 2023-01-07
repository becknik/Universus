---
tags: uni dsa practical-cs graph 
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Spann- & Wurzelbaum
  - Spannbaum
  - Minimaler Spannbaum
  - Wurzelbaum
date-of-creation: 2022-07-23
mod-date: 2022-08-05
linter-yaml-title-alias: Spann- & Wurzelbaum
---

# Spann- & Wurzelbaum

## Definition: #fc
- Der Teilgraph $B = (V, E_B)$ des [[Ungerichtete Graphen|ungerichteten]] oder [[Gerichtete Graphen|gerichteten Graphen]] $G = (V, E)$ heißt Spann- bzw. Wurzelbaum, wenn $|E_B| = |V|-1$ gilt
	→ Baumstrukturen, die alle von einem Startknoten aus erreichbaren Knoten eines Graphen miteinander verbinden
- *Spannbaum*: Bei [[Ungerichtete Graphen|ungerichteter Graphen]]
- *Wurzelbäume*: Bei [[Gerichtete Graphen|gerichteten Graphen]]
	→ Jeder Knoten im Baum ist vom Startknoten aus erreichbar
^1653921444055

## Minimale Spannbäume: #fc
- Die Summe aller Gewicht eines [[Gewichteter Graph|gewichteten Graphen]] $G=(V,E,\gamma)$ erhält man durch die Funktion $\gamma(G) := \sum_{e \in E} \gamma(e)$
	→ Das Gewicht des Graphen
- Der Spannbaum $B$ ist minimal, wenn für $\forall B':\gamma(B) \leq \gamma(B')$
- Der [[Algorithmen/Dijkstra|Dijkstra Algorithmus]] und die [[Algorithmen/Breitensuche|Breitensuche]] ergeben unmodifiziert keinen minimalen Spannbaum
	→ Der [[Algorithmus von Prim]] und der [[Algorithmen/Kruskal|Algorithmus Von Kruskal]] hingegen schon
^1655037970085
