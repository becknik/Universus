---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Modifiziertes Postsches Korrespondenzproblem
  - MPCP
date-of-creation: 2022-08-09
mod-date: 2022-08-09
linter-yaml-title-alias: Modifiziertes Postsches Korrespondenzproblem
---

# Modifiziertes Postsches Korrespondenzproblem

## Definition:
- Definiert wie das [[Postsches Korrespodenzproblem|PCP]], nur dass die Lösung mit $i_1 = 1$ beginnen muss
	→ MPCP ist unentscheidbar

## Eigenschaften:
- Das [[../../Entscheidbarkeit/Halteprobleme/Allgemeines Halteproblem|Allgemeines Halteproblem]] $H \leq$ MPCP
	→ Simulation über eine TM
- $MPCP \leq PCP$ → $PCP$ und $MPCP$ sind unentscheidbar
→ $K$ (=$MPCP$-Instanz) hat Lösung als $MPCP$ $\Leftrightarrow f(K)$ (=$PCP$-Instanz) hat Lösung als $PCP$
- Für $|\Sigma| \geq 2$ ist $PCP_\Sigma$ unentscheidbar
