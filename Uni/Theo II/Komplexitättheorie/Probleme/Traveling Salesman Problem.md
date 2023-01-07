---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Traveling Salesman Problem
  - TSP
date-of-creation: 2022-07-10
mod-date: 2022-08-12
linter-yaml-title-alias: Traveling Salesman Problem
---

# Traveling Salesman Problem

## Definition:
- *Gegeben*: Ein [[../../../DSA/Graphen/Gewichteter Graph|gewichteter Graph]] $G=(V,E,\gamma)$
- *Gesucht*: *Rundwege* $W = \{x_0,x_1,\dots,x_n\}$ mit $x_i \in V$$x_0 = x_{|V|},$$\forall i,j, 1 \leq i<j\leq n:x_i \neq x_j$
	→ Die Kosten $\gamma(W) = \sum_{i=1}^n \gamma(x_{i-1},x_i)$ sollen möglichst gering sein
	→ [[../../../DSA/Graphen/Wege & Kreise|Eulerscher Kreis]] ???

## Beispiel für [[../../Problemklassen|Problemklassen]]:
1. Entscheidungsvariante: Existiert ein Rundweg $W$ mit $\gamma(W) \leq k$ im Graphen $G$?
	 → Ausgabe "existiert nicht" muss erzeugt werden können
2. Berechnungsvariante: Berechne einen Rundweg $W$ im Graphen $G$ mit $\gamma(W) \leq k$ (falls möglich)
	→ ""
3. Optimierungsvariante: Berechne den minimalen Rundweg $W$ in $G$
	 → Wenn 1. $\in P,$ dann auch 3. $\in P$

## Beweis Entscheidung $\in NP\Rightarrow$ Optimierung $\in NP$:
- Setzte $k_{max} := \sum_{e \in E} \gamma(e)$ als obere Schranke für die Länge jedes Rundweges
	→ Beantwortet die Entscheidungsvariante
- Setzt $k_{opt}\in\{0,\dots,k_{max}\}$ als die Länge des optimalen Rundwegs durch Anfragen an die Entscheidungsvariante über beispielsweise die binäre Suche
```
INPUT: G = (V, E, γ) mit E = {e_1, ..., e_n}, k_{opt}
	G_0 := G;
	FOR i := 1 TO m DO
		IF ∃ Rundweg W in G_{i−1} \setminus {e_i} mit \gamma(W) ≤ k_{opt} 
			THEN G_i := G_{i−1} \setminus {e_i}
			ELSE G_i := G_{i−1}
		ENDIF
	ENDFOR
OUTPUT: G_m
```
