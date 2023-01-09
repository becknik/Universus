---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Gaußalgorithmus
  - Zeilenform
  - elementare Zeilenumformungen
linter-yaml-title-alias: Gaußalgorithmus
date-of-creation: 2023-01-09
mod-date: 2023-01-09
---

# Gaußalgorithmus

## Elementare Zeilenumformungen #fc
- Die folgenden *elementaren Zeilenumformungen* sind Äquivalenzumformungen auf einer [[../2. Gruppen-Ringe-Körper/Matrizen#Definition fc|Matrix]] $A\in M_{m,n}(K):$
1. Vertauschen von zwei Zeilen
2. Die Skalarmultiplikation mit Skalaren $\neq0$
3. Das Addieren des $\lambda$-fachen einer Zeile auf eine Andere
→ Lassen sich auch durch die Multiplikation *von links* mit den [[Inversen-Bildung#Elementarmatrizen (3) fc|Elementarmatrizen]] beschreiben
^1673223378081

## Zeilenstufenform

### Definition #fc
- Eine [[../2. Gruppen-Ringe-Körper/Matrizen#Definition fc|Matrix]] $A\in M_{m,n}(K)$ ist in *Zeilenstufenform*, wenn für eine aufsteigende Folge von Indizes $1\leq j_1<j_2<j_r\leq n$ mit $r\leq m$ folgendes gilt:
	- Sei $P:=\{a_{ij_i}\mid1\leq i\leq r\}$ die Menge der *Pivotelemente*
	1. Für $\forall a_{ij_i}\in P:a_{ij_i}\neq0$
	2. Für $k=1,\dots,r$ sind jeweils alle Einträge $a_{ij}$ mit $i\geq k$ und $j\leq k_j-1$ gleich $0$
	3. Die untersten $m-r$ Zeilen sind Nullzeilen
- Die resultierende Matrix in *Zeilenstufenform* hat also die Form
$$\begin{pmatrix}
0&\cdots&0&a_{1j}&\ast&&&\cdots&&&&\ast\\
0&\cdots&\cdots&\cdots&\cdots&0&a_{2j_2}&\ast&&\cdots&&\ast\\
&&&&&&\ddots&\ddots&\ddots&&&\vdots\\
0&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&0&a_{rj_r}&\ast&\cdots&\ast\\
0&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&0\\
\vdots&&&&&&&&&&&\vdots\\
0&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&0
\end{pmatrix}$$
→ Es muss gelten: $a_{1j_1},\dots,a_{rj_r}\neq0$
- *Bemerkung 1*: Beim *praktischen Rechnen* ist es oft vorteilhaft von dem Formalisums abzuweichen, indem am *zusätzliche [[#Elementare Zeilenumformungen fc|elementare Zeilenumformungen]]* wie beispielsweise Zeilenvertauschungen oder -Multiplikationen durchführt
- *Bemerkung 2*: Man kann bei dem [[Lineare Gleichungssysteme#Definition fc|LGS]] $Ax=b$ mit $b\in\{b_1,\dots,b_k\}$ auch die Matrix $\left(A|b_1|\dots|b_k\right)$ betrachten
^1673222028405

### Umformungsschritte #fc
1. Umordnen
	- Wähle die am weitesten links stehende Spalte, die nicht ausschließlich $0$en enthält als die $j$-te Spalte
	- Falls der erste Eintrag in $a_{1j}=0$ ist, wählt man den ersten Eintrag $i$ in $j$ mit $i\neq0$ und tauscht die $i$-te Zeile mit der $1.$
		→ Die Matrix ist nun in der Form $$\left(\begin{array}{ccccccc|c}0&\cdots&0&a_{1j}&\ast&\cdots&\ast&\ast\\0&\cdots&0&a_{2j}&\ast&\cdots&\ast&\ast\\\vdots&&\vdots&\vdots&\vdots&&\vdots&\vdots\\0&\cdots&0&a_{mj}&\ast&\cdots&\ast&\ast\end{array}\right),$$ wobei $\ast$ Werten $\in K$ entsprechen, die uns erstmal egal sind
2. Abziehen
	- $\forall i\in\{2\dots m\}$ wird das $-(\frac{a_{ij}}{a_{1j}})$-fache der $1.$ Spalte auf die $i.$ Spalte addiert
		→ Die Matrix ist nun in der Form $$\left(\begin{array}{ccccccc|c}0&\cdots&0&a_{1j}&\ast&\cdots&\ast&\ast\\0&\cdots&0&0&\ast&\cdots&\ast&\ast\\\vdots&&\vdots&\vdots&\vdots&&\vdots&\vdots\\0&\cdots&0&0&\ast&\cdots&\ast&\ast\end{array}\right)$$
3. Wiederholen
	- Die Schritte 1 & 2 werden auf den unteren $m-1$ Zeilen angewandt, bis die Ausgangsmatrix die folgende Gestalt aufweist:
$$\left(\begin{array}{cccccccccccc|c}
0&\cdots&0&a_{1j}&\ast&&&\cdots&&&&\ast&\ast\\
0&\cdots&\cdots&\cdots&\cdots&0&a_{2j_2}&\ast&&\cdots&&\ast&\ast\\
&&&&&&\ddots&\ddots&\ddots&&&\vdots&\vdots\\
0&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&0&a_{rj_r}&\ast&\cdots&\ast&\ast\\
0&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&0&\beta_{r+1}\\
\vdots&&&&&&&&&&&\vdots&\vdots\\
0&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&\cdots&0&\beta_m
\end{array}\right)$$
→ $\forall j_i,j_k\in\{j_1,\dots,j_r\}:\quad i<k\implies j_i$ liegt *mindestens* eine Spalte vor $j_k$
→ Die Matrix ist in [[#Zeilenstufenform#Definition fc|Zeilenstufenform]], wenn $\forall\beta\in\{\beta_{i}\mid r<i\leq m\}:\beta=0$
^1673270083825

### Hilfssatz 5.2.7
- Sein $A\in M_{mn}(K)$ in Zeilenstufenform, dann sind die [[Bezeichnungen für Matrizen|Zeilenvektoren]], die $\neq0$ sind, [[../3. Vektorräume/Lineare Unabhängigkeit#Definition fc|linear unabhängig]]

## Eigenschaften bezüglich des [[Bezeichnungen für Matrizen|Rangs]] (3) #fc
- Sei $A\in M_{m,n}(K)$
1. Die Anwendung des [[Gaußalgorithmus]] ändert nichts am [[Bezeichnungen für Matrizen|Kern]] oder dem [[Bezeichnungen für Matrizen|Rang]] der Matrix $A$
2. Der *Rang* von $A$ in Zeilenstufenform entspricht der Anzahl der Pivotelemente und somit der Anzahl der von $0$ verschiedenen Zeilen
3. Der [[Bezeichnungen für Matrizen|Zeilen- und Spaltenrang]] entsprechen dem Rang von $A$ #TODO
^1673275164414

## Weitere Anwendungen

### [[../3. Vektorräume/Spann#Definition fc|Aufspann]] des [[../3. Vektorräume/Untervektorräume#Definition fc|Zeilenuntervektorraums]]
- Sei $A\in M_{m,n}(K)$ und $B$ die [[../2. Gruppen-Ringe-Körper/Matrizen#Definition fc|Matrix]], die sich durch die Anwendung des [[Gaußalgorithmus]] aus $A$ ergibt
- Dann bilden die von $0$ verschiedenen [[Bezeichnungen für Matrizen|Zeilenvektoren]] von $B$ eine [[../3. Vektorräume/Erzeugendensysteme|Basis]] des von den *Zeilenvektoren* von $A$ aufgespannten [[../3. Vektorräume/Untervektorräume#Definition fc|Untervektorraums]] $K^n$

### Berechnung der [[../4. Lineare Abbildungen/Invertierbare Matrizen#Definition fc|Inversen]]
- Nach [[../4. Lineare Abbildungen/Lineare Abbildungen#Folgerung 4.2.5|Folgerung 4.2.5]] ist eine *quadratische* Matrix genau dann [[../4. Lineare Abbildungen/Invertierbare Matrizen|invertierbar]], wenn ihr [[Bezeichnungen für Matrizen|Kern]] trivial ist, also nur aus *Nullvektoren* besteht
	→ Dies ist genau dann der Fall, wenn die Anwendung des [[Gaußalgorithmus]]' keine Nullzeile liefert
