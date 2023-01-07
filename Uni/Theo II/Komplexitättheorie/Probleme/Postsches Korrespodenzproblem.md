---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Postsches Korrespodenzproblem
  - PCP
linter-yaml-title-alias: Postsches Korrespodenzproblem
date-of-creation: 2022-07-03
mod-date: 2022-09-12
---

# Postsches Korrespodenzproblem

## Definition: #fc
- *Gegeben*: Eine endliche Folge von Paaren $(x_i, y_i), 1 \leq i \leq k$, wobei $x_i, y_i \in \Sigma \setminus \varepsilon$
	→ Zwei gleich lange Listen von Worten über einem endlichen Alphabet $A$ mit $\alpha=(\alpha_1,\alpha_2,\dots,\alpha_n)$ und $\beta=\beta_1,\beta_2,\dots,\beta_n$ mit $\alpha_i,\beta_i\in A^+\wedge n\geq1$
 - *Gesucht*: Eine Folge von Indizes $i_1, \dots, i_{1\leq n}, i_j \in \{1,\dots,k\}$, so dass $x_{i_1}\dots x_{i_n} = y_{i_1}\dots y_{i_n}$
^1664744027112

## Eigenschaften: #fc
- Das PCP ist nicht [[../../Entscheidbarkeit|entscheidbar]] für $2\leq|\Sigma|$
- Das PCP ist durch $\chi_{PCP}'$ [[Berechenbarkeit|semi-entscheidbar]]:
```
l := 1; found:=FALSE;
WHILE NOT found DO
	Prüfe alle Indexfolgen der Länge l, ob sie das gegebene PCP lösen.
	IF Lösung gefunden THEN found:=TRUE ENDIF;
	l := l + 1
ENDWHILE;
OUTPUT 1
```
→ Das PCP ist für Einzelfälle entscheidbar - das Problem, *im Allgemeinen* zu entscheiden, ob eine PCP-Instanz mit $|\Sigma|\geq2$ eine Lösung existiert, ist nicht entscheidbar
- Das PCP ist durch [[../../Entscheidbarkeit/Halteprobleme/Allgemeines Halteproblem|H]] $\leq$ [[Modifiziertes Postsches Korrespondenzproblem|MPCP]] $\leq$ PCP nicht entscheidbar
	→ Für $2\leq|\Sigma|$ ist $PCP_\Sigma$ nicht entscheidbar
^1664744034538
