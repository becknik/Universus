---
tags: uni theo-2 theoretical-cs computability
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Ackermann-Funktion
linter-yaml-title-alias: Ackermann-Funktion
date-of-creation: 2022-08-08
mod-date: 2022-10-20
---

# Ackermann-Funktion

## Definition nach Péter: #fc
- $a(0,y)=y+1$
- $a(x,0)=a(x-1,1)\quad 0<x$
- $a(x,y)=a(x-1,a(x,y-1))\quad 0<x,y$
^1660502508932

## Eigenschaften: #fc
- Die Ackermann-Funktion ist [[../../Maths I/Wohldefiniertheit|wohldefiniert]] und total
- Die Ackermann-Funktion ist [[WHILE-berechenbar|WHILE-berechenbare]], totale, [[Modelle/Applikativ/µ-Rekursion|µ-rekursive]], aber nicht [[Modelle/Applikativ/Primitive Rekursion|primitiv rekursive]] Funktion
	→ Simulation eines [[../../Ro I/OS & Environment/Stack|Stacks]] ist notwendig
	→ "Für jede Eingabe müsste es eine LOOP-Schleife geben"
^1660910801055

## Lemmas: #fc
- *Lemma A*: $\forall x,y\in\mathbb{N}:y<a(x,y)$
- *Lemma B*: $\forall x,y\in\mathbb{N}:a(x,y)<a(x,y+1)$
- *Lemma D*: $\forall x,y\in\mathbb{N}:a(x,y)<a(x+1,y)$
- *Lemma C*: $\forall x,y\in\mathbb{N}:a(x,y+1)\leq a(x+1,y)$
- *Lemma E*: Für jedes [[Modelle/LOOP|LOOP-Programm]] $P\exists k,$ sodass $\forall n: f_p(n)<a(k,n)$
	→ [[Modelle/LOOP|Wachstum von LOOP-Programmen]]
^1660502508942
