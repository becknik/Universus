---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Matrizen
  - Matrix
  - Spaltenvektoren
  - Matrixmultiplikation
  - Matrizenmultiplikation
linter-yaml-title-alias: Matrizen
date-of-creation: 2022-10-31
mod-date: 2022-12-04
---

# Matrizen

## Definition #fc
- Eine $n\times m$-Matrix ein rechteckiges Schema mit Einträgen aus einem [[Ringe|Ring]] $R$
$$\begin{pmatrix}a_{11} & \cdots & a_{1m}\\\vdots & \ddots & \vdots\\a_{n1} & \cdots & a_{nm}\end{pmatrix}$$
- Die Elemente der Matrix werden mit $a_{i\leq n~j\leq m}\in R$ referenziert
	→ $i:$ Zeilenindex, $j:$ Spaltenindex
- Die Menge der $n\times m$-Matrizen in $R$ wird $M_{n,m}(R)$ bezeichnet
^1667232770811

### Spezielle Matrizen #fc
- Die *Einheitsmatrix*: $$\begin{pmatrix}1 & 0 & \cdots & 0 \\ 0 & 1 & \ddots & \vdots \\ \vdots & \ddots & \ddots & 0 \\ 0 & \cdots & 0 & 1\end{pmatrix}$$
	→ *Konecker-Symbol*: $E_n=\left(\delta_{ij}\begin{cases}1, & \text{falls }i=j\\0, & \text{falls }i\neq j\end{cases}~\right)$
^1667232770821

## Produkt #fc
- Für zwei Matrizen $A,B$ mit $A_{\ell,m}(R),B_{m,n}(R)$ auf dem [[Ringe|Ring]] $R$ ist der Eintrag $a_{ij}$ des *Matrixprodukts* $A\times b\in R^{\ell\times n}$ gegeben durch: $$(A\cdot B)_{ij}\quad:=\quad\sum_{k=1}^ma_{ik}b_{kj}\quad\text{für }1\leqslant i\leqslant\ell\text{ und }1\leqslant j\leqslant n$$
	→ Das Matrixprodukt ist also eine [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]] $M_{\ell,m}(R)\times M_{m,n}(R)\rightarrow M_{\ell, m}(R)$
^1667232770823

### Eigenschaften #fc
- Anzahl der notwendigen *skalaren Multiplikationen* von zwei Matrizen $M_1\in M_{m,n}(R)$ und $M_2\in M_{n,p}:m\cdot n\cdot p$
- Die Matrixmultiplikation ist nicht kommutativ
^1670180674557

## Addition
- Eine [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]] $M_{\ell,m}(R)\times M_{\ell,m}(R)\rightarrow M_{\ell,m}(R)$

## Spaltenvektoren #fc
→ [[../3. Vektorräume/Vektorräume|Vektorräume]]
- Notation von *Spaltenvektoren*: $$K^n:=\{\begin{pmatrix}x_1\\\vdots\\x_n\end{pmatrix}\mid x_1,\dots,x_n\in K\}$$
^1670180658268

## Eigenschaften #fc
- Die Menge der Matrizen $M\in R^{m\times n}$ mit Einträgen aus dem [[Ringe|Ring]] $R$ bildet mit der *Nullmatrix* und *komponentenweisen Addition* eine [[Gruppen|abelschen Gruppe]]
- Die Menge der $M_n(R)$-Matrizen wird mit *Multiplikation* und *Addition* und der *Einheitsmatrix* $E\in R^{n\times n}$ zu einem [[Ringe|unären Ring]]
- $M_n(R)$ besitzt *Nullteiler*, sobald $n\geq2$ gilt
	→ *Nullteiler*: $\exists a,b\in M_n(R),a,b\neq M_0:ab=0$
^1667232770825
