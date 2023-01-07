---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases: Rekursionssatz
linter-yaml-title-alias: Rekursionssatz
date-of-creation: 2022-11-02
mod-date: 2022-11-07
---

# Rekursionssatz

## Definition #fc
- Sei $A\neq\emptyset$ eine Menge und $a_0\in A$ fest und sei $\forall n\in\mathbb{N}_0$ die Abbildung $h_n:A\rightarrow A$ definiert.
	→ Zum Beispiel: $a=2, h:\mathbb{Q}_{>0}\rightarrow\mathbb{Q}_{>0},n\mapsto\frac{1}{2}(n+\frac{2}{n})\quad\forall n>0$
- Dann existiert *genau eine* Abbildung $F:\mathbb{N}_0\rightarrow A$ mit $$F(0)=a_0\quad\wedge\quad F(n+1)=h_n(F(n))\quad\forall n\in\mathbb{N}_0$$
→ Zum Beispiel: $a_{n+1}=F(a_{n+1})=h(F(a_n))=h(a_n)=\frac{1}{2}(a_n+\frac{2}{a_n})$
^1667419301346
