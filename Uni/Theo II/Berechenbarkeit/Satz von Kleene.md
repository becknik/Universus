---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Satz von Kleene
date-of-creation: 2022-08-08
mod-date: 2022-08-19
linter-yaml-title-alias: Satz Von Kleene
---

# Satz von Kleene

## Definition & Prinzipieller Beweis: #fc
- Sei $f:\mathbb{N}\rightarrow\mathbb{N}$ eine [[Modelle/Applikativ/µ-Rekursion|µ-rekursive]] Funktion, dann $\exists$ die zwei $(n+1)-$stellige
 [[Modelle/Applikativ/Primitive Rekursion|primitiv rekursiv]] Funktionen $p,q$ mit $$f(x_1,\dots,x_n)=p(x_1,\dots,x_n,\mu q(x_1,\dots,x_n))$$
^1660502649557

## Eigenschaften: #fc
- [[Modelle/WHILE|WHILE]] $=\text{μ-rekursiv}$
- Sagt aus, dass *eine WHILE-Schleife* ausreicht, um intuitiv berechenbare Programme zu berechnen
	→ [[Church-Turing-These|Church-Turing-These]]
- [[Modelle/Applikativ/Primitive Rekursion|primitiv rekursiv]] $\subsetneq\mu-$rekursiv
- Nicht jede $\mu-$rekursive Funktion ist total
^1664742637549

### Beweis:
- Wandle die gegeben $\mu$-rekursive Funktion in ein [[Modelle/WHILE|WHILE-Programm]] mit nur einer Schleife um
- Die Konstruktion für den Beweis (F12.2) von [[Modelle/Applikativ/µ-Rekursion|µ-rekursiv]] = [[WHILE-berechenbar|WHILE-berechenbar]] wandelt das Programm in eine Funktion mit einem $\mu$-Operator für die WHILE-Schleife um
