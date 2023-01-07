---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: L
linter-yaml-title-alias: L
date-of-creation: 2022-08-11
mod-date: 2022-10-24
---

# L
→ [[Logspace-Transducer|Logspace-Transducer]], [[../Logspace-Reduktion|Logspace-Reduktion]]

## Definition:
$$L = DSPACE(\log n)$$

## Eigenschaften: #fc
- [[../Translationssätze|Translationssatz für Platzklassen]]: $DSPACE(n)\subsetneq NSPACE(n)\Rightarrow L\subsetneq NL$
^1660860512048

## Beispiele:
- $\{a^n b^n c^n~|~1 \leq n\}$
- $\{w\#w~|~w \in \Sigma^{Stern}\}$
- $\{ww^R~|~w \in \Sigma^{Stern}\}$
- $\{ww~|~w \in \Sigma^{Stern}\}$
	→ "Virtueller Zeiger zwischen den Worten"
- Erreichbarkeit bei Bäumen
	→ Beweis wie beim [[../Probleme/Grapherreichbarkeitsproblem|GAP]]
	→ Diese Probleme sind im Gegensatz zur Universalität von NFAs/DFAs noch dicht beieinander, weshalb $L=NL$ prinzipiell möglich ist
