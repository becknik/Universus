---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Ringe
  - unärere Ring
  - kommutativer Ring
linter-yaml-title-alias: Ringe
date-of-creation: 2022-10-31
mod-date: 2022-11-13
---

# Ringe

## Definition #fc
- Sei $R$ eine [[../1. Logik-Mengenlehre-Relationen/Mengenlehre|Menge]] mit den Verknüpfungen $+\text{ und }\cdot$ (Addition und Multiplikation) dann ist $(R,+,\cdot)$ einen *Ring*, wenn er folgende Eigenschaften erfüllt:
	1. - 4. $R$ ist eine [[Gruppen|abelsche Gruppe]] bezüglich der *Addition*
	2. Die *Multiplikation* ist *assoziativ*: $(a\cdot b)\cdot c=a\cdot(b\cdot c)$
	- Es gelten die *Distributivgesetze*:
		1. $\forall a,b,c\in R:a\cdot(b+c)=a\cdot b+a\cdot c$
		2. $\forall a,b,c\in R:(a+b)\cdot c=a\cdot c+b\cdot c$
^1667213744852

### Varianten #fc
- *Unitärer Ring*/ Ring mit Eins:
	- Es gibt zusätzliches ein *neutrales Element* (=*Eins-Element*) bezüglich der Multiplikation
- Ist die *Multiplikation* zusätzlich *kommutativ*, so nennt man den Ring auch so
^1667213901851

## Eigenschaften
- Im Allgemeinen existiert in einem Ring kein inverses Element bezüglich der Multiplikation
- Für jeden Ring $R$ und $\forall x\in R$ gilt: $0\cdot x=x\cdot 0=0$

## Beispiel: Polynome mit reellen Koeffizienten
- Polynome mit *reellen Koeffizienten* (Ausdrücke der Form $a_n\cdot t^n+a_{n-1}\cdot t^{n-1}+\dots+a_1t^1+a_0$) bilden mit gewöhnlicher paarweiser Addition und Multiplikation einen kommutativen Ring mit Eins
- *Grad* des Polynoms: Das höchste $a_n\neq0$
	→ Der Grad der Nullpolynome ist $-\infty$
