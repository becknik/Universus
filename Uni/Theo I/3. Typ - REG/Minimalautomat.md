---
tags: uni theo-1 theoretical-cs automata algorithm
cards-deck: Uni::Courses::Theo-I
completed: true
aliases: Minimalautomat
linter-yaml-title-alias: Minimalautomat
date-of-creation: 2022-09-20
mod-date: 2022-09-20
---

# Minimalautomat

## Algorithmus: #fc
- Gegeben: Ein nicht-minimaler [[Deterministischer Endlicher Automat|DFA]] $M=(V,\Sigma,\delta,z_0,E)$
1. Erstelle eine untere Dreiecksmatrix $M_{|V|}$ (mit dem Zusatz, dass $i=j\Rightarrow a_{ij}=0$, also die mittlere Diagonale auch 0en enthält)
	→ Die Darstellung als Matrix macht das Zeichnen in der Anwendung einfacher
2. Markiere die Zustandspaare $(p,q),$ für die $(q\in E\wedge q\notin E)\vee(q\notin E\wedge q\in E)$ erfüllt ist
3. *Wiederhole, bis keine Markierungen mehr möglich*:
	- Suche in den *unmarkierten Paaren* nach $(p,q),$ für die $\exists a\in\Sigma,$ sodass das Paar $(\delta(p,a),\delta(q,a))$ schon markiert ist
4. Verschmelze die unmarkierten Zustandspaare
	 → Der entstandene Automat ist ein [[Myhill-Nerode|Myhill-Nerode]] Minimalautomat $M_0$
^1664630759137
