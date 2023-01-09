---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Darstellende |Matrizen
  - darstellende Matrizen
  - darstellende Matrix
linter-yaml-title-alias: Darstellende |Matrizen
date-of-creation: 2023-01-08
mod-date: 2023-01-09
---

# Darstellende [[../2. Gruppen-Ringe-Körper/Matrizen|Matrizen]]
- Merkregel ::: "Die Spalten der (darstellbaren) Matrix stellen die Bilder der Basisvektoren dar." ^1673215063239

## Definition #fc
- Seien $V,W$ [[../3. Vektorräume/Vektorräume#Definition fc|Vektorräume]] über $K$ und sei $(v_1,\dots,v_n)$ eine [[../3. Vektorräume/Erzeugendensysteme#Definition fc|Basis]] von $V, (w_1,\dots,w_m)$ eine Basis von $W$
- Sei $f:V\to W$ eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]]
- Die *(darstellbare) Matrix* $A\in M_{m,n}$ bezüglich der Basen $(v_1,\dots,v_n)$ und $(w_1,\dots,w_m)$ sei gegeben durch folgende Definition:
	- Definiere die $j$-te Spalte $(0\leq j\leq m)$ der [[../2. Gruppen-Ringe-Körper/Matrizen#Definition fc|Matrix]] $A\in M_{m,n}(K)$ jeweils als $f(v_j)$ mit $v_j$ als $j$-te Basisvektors in den [[Koordinaten]] bezüglich $(w_1,\dots,w_m)$
^1673217846905

## Beispiele #fc
- Sei $A\in M_{m,n}(K),f:K^n\to K^m,\quad x\mapsto Ax$ als die [[../2. Gruppen-Ringe-Körper/Matrizen#Produkt fc|Matrixmultiplikation]] definiert: \$$$\begin{pmatrix}x_1\\\vdots\\x_m\end{pmatrix}\mapsto\begin{pmatrix}a_{11}&\cdots&a_{1n}\\\vdots&\ddots&\vdots\\a_{m1}&\cdots&a_{mn}\end{pmatrix}\cdot\begin{pmatrix}x_1\\\vdots\\x_m\end{pmatrix}$$
	→ Der [[Kern#Definition fc|Kern]] dieser Abbildung entspricht der *Lösungsmenge* eines [[../5. Lineare Gleichungssysteme/Lineare Gleichungssysteme|homogenen linearen Gleichungssystems]]
- Sei $V$ der $\mathbb{R}$-[[../3. Vektorräume/Vektorräume#Definition fc|Vektorraum]] der reellen Polynome des Grades $\leq2,$ die Basis $B$ durch die [[../3. Vektorräume/Monome|Monome]] $$t\mapsto1,\quad t\mapsto t,\quad t\mapsto t^2$$
	→ Man betrachte den [[#Typen von Lineare Abbildungen Definition fc Linearen / ../3. Vektorräume/Vektorräume Definition fc Vektorraum - *Morphismen (6) fc|Endomorphismus]] $\varphi:V\to V,f\mapsto f'$ die Ableitung von $f,$ aus der sich die *darstellende Matrix* $$\begin{pmatrix}0&1&0\\0&0&2\\0&0&0\end{pmatrix}$$ bezüglich der Basis $B$ ergibt
^1673217846909
