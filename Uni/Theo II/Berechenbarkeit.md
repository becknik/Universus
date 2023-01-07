---
tags: uni theo-2 theoretical-cs computability abstraction
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Berechenbarkeit
  - berechenbar
linter-yaml-title-alias: Berechenbarkeit
date-of-creation: 2022-07-03
mod-date: 2022-10-02
---

# Berechenbarkeit

## Definition:
- Eine Funktion $f: \mathbb{N}^k \rightarrow \mathbb{N}$ ist berechenbar, wenn sich ein Algorithmus formulieren lässt, der die Funktion berechnet
	→ [[Berechenbarkeit/Church-Turing-These|Church-Turing-These]]

## Beziehungen zwischen Algorithmenmodellen: #fc
- $\text{Primitive Rekursion}=\text{LOOP}$
	→ [[Berechenbarkeit/Ackermann-Funktion|Ackermann-Funktion]] $\in WHILE\setminus LOOP$
- $\text{GOTO}=\text{WHILE}=\text{TM}=\text{µ-rekursiv}=\text{intuitiv berechenbar}$
- Wurden definiert, um zu zeigen, dass die 23 Hibertschen Problemen lösbar sind
	→ Manche davon sind [[Entscheidbarkeit|unentscheidbar]]
- Die Menge aller [[Berechenbarkeit|berechenbaren]] Funktionen $R$ ist *aufzählbar*, da die Menge $A^{Stern}$, deren Elemente alle Algorithmen enthalten, aufzählbar ist[^1]
- Die Menge der einstelligen Funktionen $F=\{f\mid f:\mathbb{Z}\rightarrow\mathbb{Z}\}$ ist überabzählbar groß[^1]
	→ *Berechenbare Funktionen* sind unter allen Funktionen genauso "seltene" *Ausnahmen* wie ganze Zahlen unter $\mathbb{R}$
![[_Figures/Berechenbarkeit-Überblick.png|Carlos z06]]
[CC Carlos Camino, SS2020, source:](https://fmi.uni-stuttgart.de/files/ti/teaching/s20/ti2/erg/z07.pdf)
^1660502483505

## Beispiele aus der Vorlesung:
- *Berechenbare Funktionen*:
	- $h(n) = 1,$ wenn in der Dezimalbruchentwicklung von $\pi ~n$ Mal hintereinander eine 7 vorkommt
	- $i(n)=1,$ wenn das Problem X lösbar ist
- *Keine Ahnung*:
	- $g(n)=1,$ wenn $n$ in der Dezimalbruchentwickung von $\pi$ vorkommt
- *Nicht berechenbare Funktionen*:

## Referenzen:
- [[Berechenbarkeit/Modelle/Applikativ/Primitive Rekursion|Primitive Rekursion]] $=$ [[Berechenbarkeit/Modelle/LOOP|LOOP]]
- [[Berechenbarkeit/Modelle/GOTO|GOTO]] $=$ [[Berechenbarkeit/Modelle/WHILE|WHILE]] $=$ [[../Theo I/Turingmaschinen|TM]] $=$ [[Berechenbarkeit/Modelle/Applikativ/µ-Rekursion|µ-rekursiv]] $=$ [[Berechenbarkeit/Church-Turing-These|intuitiv berechenbar]]

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021. S.187
