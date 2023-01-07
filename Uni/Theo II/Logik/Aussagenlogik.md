---
tags: uni theo-2 theoretical-cs logic 
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Aussagenlogik
  - Formel
date-of-creation: 2022-08-05
mod-date: 2022-08-11
linter-yaml-title-alias: Aussagenlogik
---

# Aussagenlogik
→ [[Ersetzbarkeitstheorem|Ersetzbarkeitstheorem]]

## Syntaktische Definition: #fc
- Atomare Formeln: $A_i, i = 1,2,3,\dots$
- Die *Disjunktion* ($\vee$) und *Konjunktion* ($\wedge$) von zwei Formeln sind auch Formeln
- Die *Negation* ($\neg$) einer Formel ist auch eine Formel
→ Jede Formel lässt sich ein [[../../DSA/Bäume|Baum]] umformen:
	- $A_i:$ Blattknoten
	- $\neg B: \neg$ ist der Elternknoten von $B$
	- $B \wedge B': \wedge$ ist der Elternknoten von $B$ und $B'$
^1661245593161

## Abkürzungen: #fc
- $F_1 \rightarrow F_2 \equiv (\neg F_1 \vee F_2)$
- $F_1 \leftrightarrow F_2 \equiv ((\neg F_1 \wedge \neg F_2) \vee (F_1 \wedge F_2))$
^1661245593169

## Äquivalenzen: #fc
- *Kommutativität* (="Vertauschungsgesetz")
- *Assoziativität* (="Verknüpfungsgesetz")
- *Distributivität* (="Verteilungsgestz")
- *Idempotenz*: $F \equiv (F \wedge F) \equiv (F \vee F)$
- *Absoption*: $(F \wedge (F \vee G)) \equiv F \equiv (F \vee (F \wedge G))$
- *deMorgan*: $\neg(F \wedge G) \equiv (\neg F \vee \neg G) \quad \neg(F \vee G) \equiv (\neg F \wedge \neg G)$
- $F$ ist eine *Tautologie*: $(F \vee G) \equiv F \quad (F \wedge G) \equiv G$
- $F$ ist *unerfüllbar*: $(F \vee G) \equiv G \quad (F \wedge G) \equiv F$
^1661245593171

## Eigenschaften:
- Kann $\forall, \exists$ oder Relationen nicht ausdrücken
	→ Die [[Prädikatenlogik]] kann das hingegen