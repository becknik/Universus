---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
complete: true
aliases: Rekursionssatz
linter-yaml-title-alias: Rekursionssatz
date: 2022-11-02
mod-date: 2022-11-02
---

# Rekursionssatz

## Definition: #fc
- Sei $A$ eine nicht-leere Menge und $a_0\in A$ fest
	-> z.B. $a=2$
- $\forall n\in\mathbb{N}_0$ sei die Abbildung $h_n:A\rightarrow A$ gegeben
	-> z.B.: $h:\mathbb{Q}_{>0}\rightarrow\mathbb{Q}_{>0},h(x)=\frac{1}{2}(x+\frac{2}{x})$
- Dann gibt es *genau eine* Abbildung $F:\mathbb{N}_0\rightarrow A$ mit $$F(0)=a_0\quad\wedge\quad F(n+1)=h_n(F(n))\quad\forall n\in\mathbb{N}_0$$
^1667419301346
