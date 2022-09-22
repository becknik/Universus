---
tags: uni theo-1 theoretical-cs
cards-deck: Uni::Courses::Theo-I
complete: true
aliases:
  - Grammatik
  - formale Grammatik
linter-yaml-title-alias: Grammatik
date: 2022-09-13
mod-date: 2022-09-23
---

# Grammatik

## Definition:
- Eine Grammatik wird formal durch das Quadrupel $$G=(V,\Sigma,P,S)$$ beschrieben, welches mit Hilfe der *Übergangsrelation* eine [[Formale Sprache|formale Sprache]] beschreibt
- $V:$ Die endliche, nicht-leere *Variablenmenge*
- $\Sigma:$ Das endliche, nicht-leere *Alphabet*
	-> $V\cap\Sigma=\emptyset$
- Die *Regelmenge*/*Produktion* $P\subseteq(V\cup\Sigma)^+\times(V\cup\Sigma)^*,~P<\infty$
- $s:$ Das *Startsymbol* $\in V$

## Fachtermini:
- Satzformen: Elemente $\in(V\cup\Sigma)^*$
- *Übergangsrelation* $\Rightarrow_G$: Seien $w_1,w_2\in(V\cup\Sigma)^*$ und $(v,u)\in P$ folgt: $$w_1uw_2\Rightarrow_Gw_1vw_2$$
	-> $\Rightarrow_G^*:$ Die *reflexive transitive Hülle* von $\Rightarrow_G$
