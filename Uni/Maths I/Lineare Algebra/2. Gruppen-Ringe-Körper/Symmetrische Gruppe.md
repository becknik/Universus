---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Symmetrische Gruppe
  - Permutationen
linter-yaml-title-alias: Symmetrische Gruppe
date-of-creation: 2022-10-31
mod-date: 2022-11-07
---

# Symmetrische Gruppe

## Definition #fc
- Sei $M$ eine [[../1. Logik-Mengenlehre-Relationen/Mengenlehre|Menge]], dann wird die Gesamtheit der bijektiven [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildungen]] auf ihr definiert als $$Sym(M):=\{f:M\rightarrow M\mid f\text{ ist bijektiv}\}$$
	→ $Sym(M)$ Bildet mit der *Verkettung von Abbildungen* eine [[Gruppen|Gruppe]]
	→ Verkettung von Abbildungen: $F:A\rightarrow B,~~G:B\rightarrow C,~~G\circ F:A\rightarrow C,\quad a\mapsto G(F(a))$
- Für den Spezialfall $M:=\{1,2,\dots,n\}$ schreibt man $Syn(n):=Syn(M)$
	→ Die Gruppe $Sym(n)$ hat $n!$ Elemente
^1667840542808

### Permutation #fc
- $n\in Sym(M)$ heißen *Permutationen* von $M$
- Eine Permutation für zum Beispiel $a\in Syn(3)$ notiert man als …
	- [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]]: $1\mapsto3,2\mapsto1,3\mapsto2$,
	- [[Matrizen|Matrix]]: $N_{2,n}(M):\begin{pmatrix}1 & 2 & 3\\3 & 1 & 2\end{pmatrix}$
^1667208430077
