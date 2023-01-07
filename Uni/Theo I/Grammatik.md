---
tags: uni theo-1 theoretical-cs formal-languages
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Grammatik
  - formale Grammatik
linter-yaml-title-alias: Grammatik
date-of-creation: 2022-09-13
mod-date: 2022-09-23
---

# Grammatik

## Definition: #fc
- Eine Grammatik wird formal durch das Quadrupel $$G=(V,\Sigma,P,S)$$ beschrieben, welches mit Hilfe der *Übergangsrelation* eine [[Formale Sprachen|formale Sprache]] beschreibt
- $V:$ Die endliche, nicht-leere *Variablenmenge*
- $\Sigma:$ Das endliche, nicht-leere *Alphabet*
	→ $V\cap\Sigma=\emptyset$
- Die *Regelmenge*/*Produktion* $P\subseteq(V\cup\Sigma)^+\times(V\cup\Sigma)^{Stern},~P<\infty$
- $s:$ Das *Startsymbol* $\in V$
^1664630614509

## Fachtermini: #fc
- Satzformen: Elemente $\in(V\cup\Sigma)^{Stern}$
- *Übergangsrelation* $\Rightarrow_G$: Seien $w_1,w_2\in(V\cup\Sigma)^{Stern}$ und $(v,u)\in P$ folgt: $$w_1uw_2\Rightarrow_Gw_1vw_2$$
	→ $\Rightarrow_G^{Stern}:$ Die *reflexive transitive Hülle* von $\Rightarrow_G$
^1664630614517
