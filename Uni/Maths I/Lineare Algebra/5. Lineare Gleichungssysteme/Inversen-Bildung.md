---
tags: uni maths maths-1 matrix
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Inversen-Bildung
  - Elementarmatrizen
  - Inverse
linter-yaml-title-alias: Inversen-Bildung
date-of-creation: 2023-01-09
mod-date: 2023-01-09
---

# Inversen-Bildung
→ [[../4. Lineare Abbildungen/Invertierbare Matrizen|Invertierbare Matrizen]]

## Elementarmatrizen #fc
- *Vertauschen*: Sei $E_{ij}$ für $1\leq i<j\leq n$ definiert als $E\in M_n(K)$ mit den vertauschten Zeilen $i$ und $j:$
$$E_{ij}:=\left(\begin{array}{ccc|c|ccc|c|ccc}
1\\
&\ddots\\
&&1\\\hline
&&&0&&&&1\\\hline
&&&&1\\
&&&&&\ddots\\
&&&&&&1\\\hline
&&&1&&&&0\\\hline
&&&&&&&&1\\
&&&&&&&&&\ddots\\
&&&&&&&&&&1
\end{array}\right)\begin{array}{}\}~i.\text{Zeile}\\\\\\\\\\\}~j.\text{Zeile}\end{array}$$
→ Es gilt: $E_{ij}^{-1}=E_{ij}$
- *Skalarmultiplikation*: Sei $E_i(\lambda)$ definiert für $\lambda\in K\setminus\{0\}$  als $E\in M_n(K)$ auf der $i$-ten Zeile mit $\lambda$ multipliziert:
$$E_i(\lambda):=\left(\begin{array}{ccc|c|ccc}
1\\
&\ddots\\
&&1\\\hline
&&&\lambda\\\hline
&&&&1\\
&&&&&\ddots\\
&&&&&&1\\
\end{array}\right)\}~i.\text{Zeile}$$
→ Es gilt: $E_i(\lambda)^{-1}=E_i(\lambda^{-1})$
- *Skalierung & Addition*: Sei $E_{ij}(\lambda)$ für $\lambda\in K$ und $i,j\in\{1,\dots,n\},1\leq i<j\leq n$ definiert als Einheitsmatrix $E\in M_n(K),$ bei der das $\lambda$-fache der $i$-ten Zeile zur $j$-ten Zeile addiert wurde:
$$E_{ij}:=\left(\begin{array}{ccc|c|ccc|c|ccc}
1\\
&\ddots\\
&&1\\\hline
&&&1&&&&0\\\hline
&&&&1\\
&&&&&\ddots\\
&&&&&&1\\\hline
&&&\lambda&&&&1\\\hline
&&&&&&&&1\\
&&&&&&&&&\ddots\\
&&&&&&&&&&1
\end{array}\right)\begin{array}{}\}~i.\text{Zeile}\\\\\\\\\\\}~j.\text{Zeile}\end{array}$$
	→ $E_{ij}(\lambda)$ lässt sich analog auch umgekehrt für $1\leq j<i\leq n$ definieren:
$$E_{ij}:=\left(\begin{array}{ccc|c|ccc|c|ccc}
1\\
&\ddots\\
&&1\\\hline
&&&1&&&&\lambda\\\hline
&&&&1\\
&&&&&\ddots\\
&&&&&&1\\\hline
&&&0&&&&1\\\hline
&&&&&&&&1\\
&&&&&&&&&\ddots\\
&&&&&&&&&&1
\end{array}\right)\begin{array}{}\}~j.\text{Zeile}\\\\\\\\\\\}~i.\text{Zeile}\end{array}$$
→ Es gilt: $E_{ij}(\lambda)^{-1}=E_{ij}(-\lambda)$
^1673297243022

### Hilfssatz 5.3.4
- Elementarmatrizen sind [[../4. Lineare Abbildungen/Invertierbare Matrizen#Definition fc|invertierbar]]
- Für eine beliebige [[../2. Gruppen-Ringe-Körper/Matrizen#Definition fc|Matrix]] $A\in M_{m,n}(K):$
	1. $A\cdot E_{ij}$ bewirkt eine Vertauschung der $i$-ten mit der $j$-ten Zeile von $A$
	2. $=A\cdot E_i(\lambda)$ bewirkt die Multiplikation der $i$-ten Zeile von $A$ mit $\lambda$
	3. $=A\cdot E_{ij}(\lambda)$ bewirkt die Addition des $\lambda$-fachen der $i$-ten Zeile zur $j$-ten Zeile
→ Das Multiplizieren einer Matrix $A$ *von links* mit den 3 [[#Elementarmatrizen (3) fc|Elementarmatrizen]] bewirkt dasselbe wie die [[Gaußalgorithmus#Elementare Zeilenumformungen fc|elementare Zeilenumformungen]]

## Funktionsweise #fc
- Seien $A\in M_n(K)$ und $E\in M_n(K)$ gegeben
- Wenn $A$ einen [[Bezeichnungen für Matrizen|Rang]] $\neq n$ hat, lässt sie sich nicht invertieren #TODO
- Lässt sich $\left(A\mid E\right)$ durch [[Gaußalgorithmus#Elementare Zeilenumformungen fc|elementare Zeilenumformungen]] auf die Form $\left(E\mid B\right)$ bringen, so ist $A$ [[../4. Lineare Abbildungen/Invertierbare Matrizen#Definition fc|invertierbar]] und $B$ das *Inverse* von $A$
^1673297243027
