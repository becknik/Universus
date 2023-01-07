---
tags: uni theoretical-cs
cards-deck: Uni::Courses::Theo-I
completed: true
aliases: Längenlexikographische Ordnung
linter-yaml-title-alias: Längenlexikographische Ordnung
date-of-creation: 2022-09-03
mod-date: 2022-10-02
---

# Längenlexikographische Ordnung

## Definition:[^1] #fc
- Sei ein *endlichen Alphabet* $\Sigma=\{a_1,\dots,a_n\}$ (mit einer festen Nummerierung, wie beim lateinischen Alphabet) gegeben
- $\Sigma^{Stern}$ lässt sich nach einer festen Ordnung auflisten, und zwar…
1. der Länge nach wobei es $\forall i:|\Sigma^i|<\infty$ gilt, da $|\Sigma|^l<\infty$
2. lexikographisch innerhalb der Wörter gleicher Länge durch $$b_1b_2\dots b_n~<~c_1c_2\dots c_n\quad\Leftrightarrow\quad b_1<c_1\vee(b_1=c_1\wedge b_2<c_2)\vee(b_1=c_1\wedge b_2=c_2\wedge b_3<c_3)\vee\dots$$
	→ Eine Menge $A^{Stern}$ mit *lexikographischer Ordnung* ist **abzählbar**
^1664736161962

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021.
