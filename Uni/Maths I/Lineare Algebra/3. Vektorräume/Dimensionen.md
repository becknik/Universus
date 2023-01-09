---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Dimensionen
  - Dimension
  - Monom
linter-yaml-title-alias: Dimensionen
date-of-creation: 2022-12-04
mod-date: 2023-01-08
---

# Dimensionen

## Definition #fc
- Besitzt ein [[Vektorräume|Vektorraum]] $V$ ein [[Erzeugendensysteme|Basis]] $B,|B|<\infty,$ dann wird $|B|$ als Dimension $\text{dim}(V)$ des Vektorraums bezeichnet
	→ Wenn der Vektorraum keine Basis $B<\infty$ besitzt, gilt $\text{dim}(V)=\infty$
	→ Aufgrund der [[Erzeugendensysteme|Standardbasis/ kanonischen Basis]] $e_1,\dots,e_n:\quad\text{dim}(K^n)=n$
^1670184241827

## Formel für [[Untervektorräume]] #fc
- Sei $V$ ein [[Vektorräume|Vektorraum]], $U_1,U_2$ Untervektorräume von $V,$ dann gilt $$\text{dim}(U_1+U_2)=\text{dim}(U_1)+\text{dim}(U_2)+\text{dim}(U_1\cap U_2)$$
^1670184933328

## Hilfssatz 3.6.5
- Sei $V$ ein *endlich-$n$-dimensionaler* [[Vektorräume|Vektorraum]], dann hat jeder [[Untervektorräume|Untervektorraum]] $U$ von $V$ mit $U\neq V$ eine *echt kleinere Dimension* als $V$
- Außerdem: Jede [[Lineare Unabhängigkeit|linear unabhängige]] Teilmenge von $V$ mit $n$ Elementen ist eine [[Erzeugendensysteme|Basis]] von $V$

## Beispiel

### Menge der reellen Polynome #fc
$$\mathbb{R}\to\mathbb{R},~t\mapsto a_nt^n+a_{n-1}t^{n-1}+\dots+a_1t+a_0$$
- Ein *unendlich-dimensionaler* [[Vektorräume|Vektorraum]]:
- Die [[Monome]] $\{t\mapsto t^k\mid k\in\mathbb{N}_0\}$ bilden eine [[Lineare Unabhängigkeit|linear unabhängige]] Teilmenge
	→ Die einzige [[Linearkombinationen|Linearkombination]] von *Monomen*, die die 0-Funktion ergeben, ist die triviale
	→ Mit dem [[Erzeugendensysteme|Satz 3.6.4: Allgemeinaussagen über Basen]] folgt daraus, dass es in diesem Vektorraum keine endlichen Basen geben kann
	→ Es folgt, dass $\mathbb{R}\rightarrow\mathbb{R}$ *unendlich-dimensional* ist
 ^1670184254979
