---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases: NP-Vollständigkeit
date: 2022-08-11
mod-date: 2022-08-20
linter-yaml-title-alias: NP-Vollständigkeit
---

# NP-Vollständigkeit
-> [[NP|NP]]

## Definition:
- Eine Sprache $A$ heißt NP-vollständig, falls sie [[NP/NP-Härte|NP-hart]] ist und $A \in$ [[NP|NP]] gilt
$$A\in NP\wedge \forall L\in NP: L\leq_pA$$

## Eigenschaften: #fc
- NP $\subseteq$ [[../../../Berechenbarkeit/LOOP-berechenbar|LOOP-berechenbar]]
- NP-vollständige Probleme sind die schwierigsten Probleme in [[NP|NP]]
- Nachweis für die Zugehörigkeit in NP funktioniert meistens über durch [[NP/Guess and Check|Guess And Check]]
- $L\in$ NP-vollständig $\Rightarrow$ Effizienter Algorithmus (=in Polynomialzeit lösbar) ist (wahrscheinlich) unmöglich
- Falls $\exists A\in NP$-vollständig mit $A \in/\notin P:P =/\neq NP$
^1660503074803
