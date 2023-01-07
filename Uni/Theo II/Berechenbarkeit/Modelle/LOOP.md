---
tags: uni theo-2 theoretical-cs computability
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: LOOP
date-of-creation: 2022-07-03
mod-date: 2022-08-20
linter-yaml-title-alias: LOOP
---

# LOOP
→ [[../LOOP-berechenbar|LOOP-berechenbar]]

## Syntax: #fc
- Variablen: $x_{i\in\{1,\dots,k\}}$ tragen die Funktionsparameter der Funktion $f:\mathbb{N}^k\rightarrow\mathbb{N}$
	→ Das Ergebnis der Berechnung befindet sich in $x_0$
	→ $x_i = x_j\pm c \mid i,j,c\in\mathbb{N}$
- Konstanten: $\in\mathbb{N}$
- Trennsymbole: $;~:=$
- Operationen: $+,\text{ (modifiziertes)}-$
- Schlüsselwörter: $\text{LOOP},\text{DO},\text{END}$
- $P_1;P_2\mid P_1,P_2\in \text{LOOP}$
- $\text{LOOP }x_i\text{ DO } P \text{ END}\mid i\in\mathbb{N},P\in\text{LOOP}$
^1660502741130

## Erweiterter Syntax: #fc
- *IF-Verzweigung*:
	- $\text{LOOP} x_c:=x_n-k; \quad\rightarrow\quad 0 < x_c \Leftrightarrow k < x_n$
	- $x_m=1;$
	- $\text{LOOP } x_c \text{ DO}$
		- $\text{LOOP } x_m \text{ DO } P \text{ END};$
		- $x_m:=0;$
	- $\text{END}$
- *Multiplikation*:
	- $x_0 := 0;$
	- $\text{LOOP } x_i \text{ DO}$
		- $\text{ LOOP } x_j \text{ DO}$
			- $x_0 :=x_0+1$
		- $\text{END};$
	- $\text{ END}$
^1660502741138

## Wachstum: #fc
- Für ein Programm $P:f_p(n) = \max\{\sum_{i \geq 0}~n_i' ~| \sum_{i \geq 0}~n_i \leq n\}$
	- $n_i$ sind die Anfangswerte der Variable $x_i$
	- $n_i'$ sind die Endwerte der Variable $x_i$ nach dem Ablauf von $P$
→ [[../Ackermann-Funktion|Ackermann-Funktion - Lemma E]]: $\forall\text{LOOP-Programme }P,\exists k,\text{sodass }\forall n: f_P(n)<a(k,n)$
^1660502741141
