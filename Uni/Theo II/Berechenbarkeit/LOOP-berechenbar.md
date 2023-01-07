---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: LOOP-berechenbar
date-of-creation: 2022-08-06
mod-date: 2022-08-19
linter-yaml-title-alias: LOOP-berechenbar
---

# LOOP-berechenbar

## Definition: #fc
- Eine Funktion $f: \mathbb{N}^k \rightarrow \mathbb{N}$ ist *LOOP-berechenbar*, wenn es ein [[LOOP|LOOP-Programm]] $P$ gibt, das mit den Variablen $x_1,\dots,x_k$ gestartet nach *endlich vielen Schritten* hält und das Ergebnis von $f(n_1,\dots,n_k)$ in $x_0$ hat
	→ Die restlichen Variablen müssen gleich 0 gesetzt sein
^1660911028607

## Eigenschaften: #fc
- $LOOP \subsetneq WHILE \cap TOTAL \subsetneq WHILE$
- Alle LOOP-berechenbaren $\subsetneq$ *totale Funktionen*
	→[[Ackermann-Funktion|Ackermann-Funktion]] $\notin\text{LOOP}\wedge\in\text{TOTAL}$
- Wenn eine Funktion LOOP-berechenbar ist, dann ist sie auch [[Applikativ/Primitive Rekursion|primitiv rekursiv]]
^1660911028618
