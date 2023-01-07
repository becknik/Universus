---
tags: uni dsa practical-cs graph bipartit trait
cards-deck: Uni::Courses::DSA
completed: true
aliases: Bipartite Graphen
linter-yaml-title-alias: Bipartite Graphen
date-of-creation: 2022-07-24
mod-date: 2022-09-10
---

# Bipartite Graphen
→ [[Ungerichtete Graphen|Ungerichteter Graph]]

## Definition: #fc
- Ein Graph $G = (V,E), V = A \cup B$ heißt bipartit, wenn folgendes gilt:
	- $A,B \neq \emptyset$
	- $A \cap B = \emptyset$
	- $\forall e \in E: e \cap A \neq \emptyset \wedge e \cap B \neq \emptyset$
→ Jede Kante $e$ verbindet einen Knoten von $A$ mit einem Knoten von $B$
^1655220210167
