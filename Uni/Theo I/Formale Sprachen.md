---
tags: uni theo-1 theoretical-cs abstraction formal-languages
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Formale Sprachen
  - Sprache
linter-yaml-title-alias: Formale Sprachen
date-of-creation: 2022-09-13
mod-date: 2022-10-02
---

# Formale Sprachen
![[_Figures/Chomsky-Hiarchie-Spachen-Überblick.png|400]]
[CC Carlos Camino, SS2020, source:](https://fmi.uni-stuttgart.de/files/ti/teaching/s20/ti2/erg/z06.pdf)

## Definition: #fc
- Unter zur Hilfenahme einer [[Grammatik|Grammatik]] $G$ gilt: $$L(G)=\{w\in\Sigma^{Stern}\mid S\Rightarrow^{Stern}_Gw\}$$
- Eine Teilmenge des [[Monoid|freien Monoids]] über $\Sigma$
	→ Es gibt überabzählbar viele Sprachen über $\Sigma$
^1664632450791

## Eigenschaften: #fc
- Für eine *formale Sprache* $L\subseteq\Sigma^{Stern}:L$ ist vom [[Chomsky-Hierarchie|Typ]] $i\in\{0,1,2,3\},$ falls $\exists$ eine [[Grammatik|Grammatik]] $G$ mit $L=L(G)$
- Formale Sprachen entsprechen [[../../Theo II/Problemklassen|Entscheidungsproblemen]]
	→ z.B. Gibt es einen Graphen der Länge 5 $\Leftrightarrow$ $\{L\mid L$ beschreibt Graphen mit einem Weg der Länge 5$\}$
^1664630626121
