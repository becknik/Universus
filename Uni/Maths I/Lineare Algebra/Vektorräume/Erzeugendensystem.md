---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Erzeugendensystem
  - Basis
  - Standardbasis
  - kanonische Basis
linter-yaml-title-alias: Erzeugendensystem
date-of-creation: 2022-12-04
mod-date: 2022-12-04
---

# Erzeugendensystem

## Definition #fc
- Sei $V$ ein [[Vektorräume|Vektorraum]], dann wird $E\subseteq V$ mit $\text{span}(E)=V$ ([[Spann]]) *Erezeugendensystem* von $V$ genannt
^1670181684376

### Basis: #fc
- Eine *Basis* $B$ eines [[Vektorräume|Vektorraums]] $V's$ ist ein *[[Lineare Unabhängigkeit|linear unabhängiges]] Erzeugendensystem*
^1670181684379

### Äquivalenzen: #fc
1. $B\subseteq V$ ist eine *Basis* von $V$
2. $B$ ist ein *minimales Erzeugendensystem* von $V$
	 → $\forall v\in B:\quad B\setminus\{v\}$ ist kein Erzeugendensystem von $V$ mehr
3. $B$ ist eine *maximal [[Lineare Unabhängigkeit|linear unabhängige]]* Teilmenge von $V$
	 → $B$ ist *linear unabhängig* & $\forall v\in V\setminus B:\quad B\cup\{v\}$ ist *nicht* linear unabhängig
^1670181684382

## Standardbasis/ Kanonische Basis: #fc
- Die *Standardbasis/ kanonische Basis* von $K^n$ besteht aus der Menge von Elementen $e_1,\dots,e_n\in K^n$ (= [[../Gruppen-Ringe-Körper/Matrizen|Spaltenvektor]]):$$e_1=\begin{pmatrix}1\\0\\0\\\vdots\\0\end{pmatrix},e_2=\begin{pmatrix}0\\1\\0\\\vdots\\0\end{pmatrix},\dots,e_n=\begin{pmatrix}0\\0\\0\\\vdots\\1\end{pmatrix}$$
	→ Jeder Vektor $v\in K^n$ lässt sich als [[Linearkombinationen]] $$e_1=\begin{pmatrix}\lambda_1\\\vdots\\\lambda_n\end{pmatrix}=\lambda_1e_1+\dots+\lambda_ne_n$$ darstellen
^1670181183885

## Lemmata

### Basisergänzungssatz: #fc
- Sei $V$ ein [[Vektorräume|Vektorraum]] und $E=\{w_1,\dots,w_m\},E<\infty$ ein [[Erzeugendensystem]] von $V$
- Sei $B\subseteq V$ [[Lineare Unabhängigkeit|linear unabhängig]]
- Dann gibt es Vektoren $v_1,\dots,v_k\in E,$ so dass $B\cup\{v_1,\dots,v_k\}$ eine [[Erzeugendensystem|Basis]] von $V$ ist
^1670182886177

### Austauschlemma: #fc
- Seien $A=\{v_1,\dots,v_n\}$ und $B=\{w_1,\dots,w_n\}$ [[Erzeugendensystem|Basen]] des [[Vektorräume|Vektorraums]] $V$
- Sei $i\in\{1,\dots,n\}$
- Es gilt: $\exists j\in\{1,\dots,n\},$ so dass auch $${v_1,\dots,v_{i−1},w_j,v_{i+1},\dots,v_n}$$ eine *Basis* von $V$ darstellt
^1670182886180

### Hilfssatz 3.6.3
- Je zwei endliche Basen eines Vektorraums bestehen aus gleich vielen Elementen

### Satz 3.6.4: Allgemeinaussagen über Basen #fc
- Sei $V$ ein [[Vektorräume|Vektorraum]], der eine [[Erzeugendensystem|Basis]] aus $n$ Elementen besitzt, dann gilt:
	1. Jedes $A\subseteq V,|A|\geqslant n+1$ ist [[Lineare Unabhängigkeit|linear abhängig]]
	2. Jedes [[Erzeugendensystem]] von $V$ enthält mindestens $n$ Elemente
	3. Jede Basis von $V$ besteht aus $n$ Elementen
→ Folgerung: [[Untervektorräume]] von [[Dimensionen|endlich-dimensionalen]] [[Vektorräume|Vektorräumen]] sind selbst wieder *endlich-dimensional*
^1670184569001
