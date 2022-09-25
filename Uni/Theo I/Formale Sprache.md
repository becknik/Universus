---
tags: uni theo-1 theoretical-cs abstraction formal-languages
cards-deck: Uni::Courses::Theo-I
complete: true
aliases:
  - Formale Sprache
  - Sprache
linter-yaml-title-alias: Formale Sprache
date: 2022-09-13
mod-date: 2022-09-15
---

# Formale Sprache
![[_Figures/Chomsky-Hiarchie-Spachen-Überblick.png|400]]
[CC Carlos Camino, SS2020, source:](https://fmi.uni-stuttgart.de/files/ti/teaching/s20/ti2/erg/z06.pdf)

## Definition:
- Unter zur Hilfenahme einer [[Grammatik|Grammatik]] $G:$$$L(G)=\{w\in\Sigma^*\mid S\Rightarrow^*_Gw\}$$
- Eine Teilmenge des [[Monoid|freien Monoids]] über $\Sigma$
	-> Es gibt überabzählbar viele Sprachen über $\Sigma$

## Eigenschaften:
- Für eine *formale Sprache* $L\subseteq\Sigma^*:L$ ist vom [[Chomsky-Hierarchie|Typ]] $i\in\{0,1,2,3\},$ falls $\exists$ eine [[Grammatik|Grammatik]] $G$ mit $L=L(G)$
- Formale Sprachen entsprechen [[../../Theo II/Problemklassen|Entscheidungsproblemen]]
	-> z.B. Gibt es einen Graphen der Länge 5 $\Leftrightarrow$ $\{L\mid L$ beschreibt Graphen mit einem Weg der Länge 5$\}$
