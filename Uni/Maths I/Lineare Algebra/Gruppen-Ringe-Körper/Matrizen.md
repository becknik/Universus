---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
complete: true
aliases: Matrizen
linter-yaml-title-alias: Matrizen
date: 2022-10-31
mod-date: 2022-10-31
---

# Matrizen

## Definition #fc
- Eine $n\times m$-Matrix ein rechteckiges Schema mit Einträgen aus einem [[Ringe|Ring]] $R$
$$\begin{pmatrix}a_{11} & \cdots & a_{1m}\\\vdots & \ddots & \vdots\\a_{n1} & \cdots & a_{nm}\end{pmatrix}$$
- Die Elemente der Matrix werden mit $a_{i\leq n~j\leq m}\in R$ referenziert
	-> $i:$ Zeilenindex, $j:$ Spaltenindex
- Die Menge der $n\times m$-Matrizen in $R$ wird $M_{n,m}(R)$ bezeichnet
^1667232770811

### Spezielle Matrizen: #fc
- Die *Einheitsmatrix*: $$\begin{pmatrix}1 & 0 & \cdots & 0 \\ 0 & 1 & \ddots & \vdots \\ \vdots & \ddots & \ddots & 0 \\ 0 & \cdots & 0 & 1\end{pmatrix}\quad\Leftrightarrow\quad E_n=\left(\delta_{ij}\begin{cases}1, & \text{falls }i=j\\0, & \text{falls }i\neq j\end{cases}~\right)$$
	-> *Konecker-Symbol*
^1667232770821

## Produkt #fc
- Für zwei Matrizen $A,B$ mit $A_{n,m}(R),B_{m,k}(R)$ ist der Eintrag $a_{ij}$ des Matrizenprodukts $C_{n,k}(R)$ durch $$\sum_{k=1}^na_{ik}b_{jk}$$ gegeben
- Anzahl der skalaren Multiplikationen für $M_1\in M_{l,m}(R),M_2\in M_{m,n}:l\cdot m\cdot n$
^1667232770823

## Eigenschaften: #fc
- Die menge der $M_{n,m}$-Matrizen mit Einträgen aus dem [[Ringe|Ring]] $R$ wird mit der *Nullmatrix* und der *komponentenweisen Addition* zu einer [[Gruppen|abelschen Gruppe]]
	-> Assoziativität
- Die Menge der $M_n(R)$-Matrizen wird mit *Multiplikation* und *Addition* und der $n\times n$-*Einheitsmatrix* zu einem [[Ringe|unären Ring]]
	-> Assoziativität & Distributivität
- $M_n(R)$ besitzt *Nullteiler*, sobald $n\geq2$
	-> Nullteiler: $\exists a,b\in M_n(R),a,b\neq M_0:ab=0$
^1667232770825
