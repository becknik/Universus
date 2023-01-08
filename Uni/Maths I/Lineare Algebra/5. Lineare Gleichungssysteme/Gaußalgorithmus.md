---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases: Gaußalgorithmus
linter-yaml-title-alias: Gaußalgorithmus
date-of-creation: 2023-01-09
mod-date: 2023-01-09
---

# Gaußalgorithmus

## Elementare Zeilenumformungen
- Die folgenden *elementaren Zeilenumformungen* sind Äquivalenzumformungen auf einer [[../2. Gruppen-Ringe-Körper/Matrizen#Definition fc|Matrix]] $A\in M_{m,n}(K):$
1. Vertauschen von zwei Zeilen
2. Die Skalarmultiplikation mit Skalaren $\neq0$
3. Das Addieren des $\lambda$-fachen einer Zeile auf eine Andere

## Zeilenstufenform #fc
- Eine [[../2. Gruppen-Ringe-Körper/Matrizen#Definition fc|Matrix]] $A\in M_{m,n}(K)$ ist in *Zeilenstufenform*, wenn für eine aufsteigende Folge von Indizes $1\leq j_1<j_2<j_r\leq n$ das Folgende gilt:
	- Sei $P:=\{a_{ij_i}\mid1\leq i\leq r\}$ die Menge der *Pivotelemente*
	1. Für $\forall a\in P:a\neq0$
	2. Für $k=1,\dots,r$ sind jeweils alle Einträge $a_{ij}$ mit $i\geq k$ und $j\leq kj-1$ gleich $0$
	3. Die untersten $m-r$ Zeilen sind Nullzeilen
^1673222028405
> Schaubild texen #TODO

