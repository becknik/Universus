---
tags: uni theo-2 theoretical-cs complexity solvability
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: NP-Vollständigkeit
linter-yaml-title-alias: NP-Vollständigkeit
date-of-creation: 2022-08-11
mod-date: 2022-10-24
---

# NP-Vollständigkeit
→ [[NP|NP]]

## Definition: #fc
- Eine Sprache $A$ heißt NP-vollständig, falls sie [[NP/NP-Härte|NP-hart]] ist und $A \in$ [[NP|NP]] gilt
$$A\in NP\wedge \forall L\in NP: L\leq_pA$$
^1666643804965

## Eigenschaften: #fc
- Die schwierigsten Probleme in [[NP|NP]]
- $L\in$ NP-vollständig $\Rightarrow$ Effizienter Algorithmus (=in Polynomialzeit lösbar) ist (wahrscheinlich) unmöglich
- Falls $\exists A\in NP$-vollständig mit $A\in\text{P}:\text{P}=\text{NP}$ oder $A\notin\text{P}:\text{P}\neq\text{NP}$
^1660503074803
