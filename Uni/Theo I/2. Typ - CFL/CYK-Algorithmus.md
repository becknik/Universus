---
tags: uni theo-1 theoretical-cs algorithm
cards-deck: Uni::Courses::Theo-I
complete: false
aliases:
  - CYK-Algorithmus
  - CYK
linter-yaml-title-alias: CYK-Algorithmus
date: 2022-09-21
mod-date: 2022-09-23
---

# CYK-Algorithmus

## Funktionsweise:
- Gegeben: Eine Grammatik in [[Chomsky-Normalform|CNF]] $G$ und ein Wort $w\in\Sigma^*$
	-> Entscheidbar für $|w|\geq2$
- Gesucht: Eine *effiziente* ($\in\mathbfcal{O}(n^3)$; nicht exponentielle) Lösung des [[../Wortproblem|Wortproblems]] für [[../Typ-2|CFL-Sprachen]]
1. Erstelle eine obere linke Dreiecksmatrix $M_{|w|+1}$ mit $M_{0,1\leq i\leq|w|}=w[i-1]$ und $M_{1\leq i\leq|w|,0}=i$
	-> In Matrix-Schreibweise ist das Verfahren (wieder) in der Praxis leichter anzuwenden
2. Berechne Spalte für Spalte $T\subseteq V$ mit $$A\in T_{i,j}\quad\Leftrightarrow\quad A\Rightarrow^*w_iw_{i+1}\dots w_{i+j-1}$$

## Eigenschaften:
- Der Algorithmus ist nach den Erfindern *Cocke, Younger und Kasami* benannt
- Er benutzt das *Algorithmenmuster* der [[../../DSA/Algorithmen/Muster/Dynamische Programmierung|Dynamische Programmierung]]
- Der Algorithmus funktioniert in kubischer Zeit
