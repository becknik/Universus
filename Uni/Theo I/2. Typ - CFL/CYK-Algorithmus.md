---
tags: uni theo-1 theoretical-cs algorithm chomsky
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - CYK-Algorithmus
  - CYK
linter-yaml-title-alias: CYK-Algorithmus
date-of-creation: 2022-09-21
mod-date: 2022-09-25
---

# CYK-Algorithmus

## Funktionsweise: #fc
- Gegeben: Eine Grammatik in [[Chomsky-Normalform|CNF]] $G$ und ein Wort $w\in\Sigma^{Stern}$
	→ Entscheidbar für $|w|\geq2$
- Gesucht: Eine *effiziente* ($\in\mathbfcal{O}(n^3)$; nicht exponentielle) Lösung des [[../Wortproblem|Wortproblems]] für [[../Typ-2|CFL-Sprachen]]
1. Erstelle eine obere linke Dreiecksmatrix $M_{|w|+1}$ mit $M_{1\leq i\leq|w|,0}=i$ und $M_{0,1\leq i\leq|w|}=w[i-1]$
	→ In Matrix-Schreibweise ist das Verfahren (wieder) in der Praxis leichter anzuwenden, anschaulicher wird auf V.15 F.28.1 dargestellt
2. Berechne Spalte für Spalte $T\subseteq V$ mit $$A\in T_{i,j}\quad\Leftrightarrow\quad A\Rightarrow^{Stern}w_iw_{i+1}\dots w_{i+j-1}$$
^1664631112960

## Eigenschaften: #fc
- Der Algorithmus ist nach den Erfindern *Cocke, Younger und Kasami* benannt
- Er benutzt das *Algorithmenmuster* der [[../../DSA/Algorithmen/Muster/Dynamische Programmierung|Dynamische Programmierung]]
- Der Algorithmus funktioniert in kubischer Zeit
^1664633583621
