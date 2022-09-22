---
tags: 
cards-deck: 
complete: true
aliases: Längenlexikographische Ordnung
linter-yaml-title-alias: Längenlexikographische Ordnung
date: 2022-09-03
mod-date: 2022-09-11
---

# Längenlexikographische Ordnung

## Definition:
- Sei ein *endlichen Alphabet* $\Sigma=\{a_1,\dots,a_n\}$ (mit einer festen Nummerierung, wie beim lateinischen Alphabet) gegeben
- $\Sigma^*$ lässt sich nach einer festen Ordnung auflisten, und zwar…
1. der Länge nach wobei es $\forall i:|\Sigma^i|<\infty$ gilt, da $|\Sigma|^l<\infty$
2. lexikographisch innerhalb der Wörter gleicher Länge durch $$b_1b_2\dots b_n~<~c_1c_2\dots c_n\quad\Leftrightarrow\quad b_1<c_1\vee(b_1=c_1\wedge b_2<c_2)\vee(b_1=c_1\wedge b_2=c_2\wedge b_3<c_3)\vee\dots$$
	-> Eine Menge $A^*$ mit *lexikographischer Ordnung* ist **abzählbar**
