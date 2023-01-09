---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Erzeugendensysteme
  - Basis
  - Standardbasis
  - kanonische Basis
linter-yaml-title-alias: Erzeugendensysteme
date-of-creation: 2022-12-04
mod-date: 2023-01-09
---

# Erzeugendensysteme

## Definition #fc
- Sei $(V,+)$ ein [[Vektorräume#Definition fc|Vektorraum]], dann wird $E\subseteq V$ mit $\text{span}(E)=V$ *Erezeugendensystem* von $V$ genannt
	→ Jeder *Vektorraum* besitzt eine Basis
> Siehe: [[Spann#Definition fc|Spann]]
^1670181684376

## Basis #fc
- Eine *Basis* $B$ eines [[Vektorräume#Definition fc|Vektorraums]] $V's$ ist ein *[[Lineare Unabhängigkeit#Definition fc|linear unabhängiges]] [[Erzeugendensysteme#Definition fc|Erzeugendensystem]]*
^1670181684379

## Äquivalenzen (3) #fc
1. $B\subseteq V$ ist eine *Basis* von $V$
2. $B$ ist ein *minimales Erzeugendensystem* von $V$
	→ $\forall v\in B:\quad B\setminus\{v\}$ ist kein Erzeugendensystem von $V$ mehr
3. $B$ ist eine *maximal [[Lineare Unabhängigkeit|linear unabhängige]]* Teilmenge von $V$
	→ $B$ ist *linear unabhängig* & $\forall v\in V\setminus B:\quad B\cup\{v\}$ ist *nicht* linear unabhängig
^1670181684382

## Standard-/ Kanonische Basis #fc
- Die *Standardbasis/ kanonische Basis* von $K^n$ besteht aus der Menge von Elementen $e_1,\dots,e_n\in K^n$ (= [[../2. Gruppen-Ringe-Körper/Matrizen|Spaltenvektor]]):$$e_1=\begin{pmatrix}1\\0\\0\\\vdots\\0\end{pmatrix},e_2=\begin{pmatrix}0\\1\\0\\\vdots\\0\end{pmatrix},\dots,e_n=\begin{pmatrix}0\\0\\0\\\vdots\\1\end{pmatrix}$$
	→ Jeder Vektor $v\in K^n$ lässt sich als [[Linearkombinationen]] $$v=\begin{pmatrix}\lambda_1\\\vdots\\\lambda_n\end{pmatrix}=\lambda_1e_1+\dots+\lambda_ne_n$$ darstellen
^1670181183885

## Lemmata

### Basisergänzungssatz #fc
- Sei $V$ ein [[Vektorräume|Vektorraum]] und $E=\{w_1,\dots,w_m\},|E|<\infty$ ein [[Erzeugendensysteme]] von $V$
- Sei $B\subseteq V$ [[Lineare Unabhängigkeit|linear unabhängig]]
- Dann gibt es Vektoren $v_1,\dots,v_k\in E,$ so dass $B\cup\{v_1,\dots,v_k\}$ eine [[Erzeugendensysteme|Basis]] von $V$ ist
^1670182886177

### Austauschlemma #fc
- Seien $A=\{v_1,\dots,v_n\}$ und $B=\{w_1,\dots,w_n\}$ [[Erzeugendensysteme|Basen]] des [[Vektorräume|Vektorraums]] $V$
- Wähle $i\in\{1,\dots,n\},$ dann gilt: $\exists j\in\{1,\dots,n\},$ so dass auch $${v_1,\dots,v_{i−1},w_j,v_{i+1},\dots,v_n}$$ eine *Basis* von $V$ darstellt
^1670182886180

### Hilfssatz 3.6.3
- Je zwei endliche [[#Basis fc|Basen]] eines [[Vektorräume#Definition fc|Vektorraums]] bestehen aus gleich vielen Elementen

### Satz 3.6.4: Allgemein-Aussagen über Basen #fc
- Sei $V$ ein [[Vektorräume|Vektorraum]], der eine [[Erzeugendensysteme|Basis]] aus $n$ Elementen besitzt, dann gilt:
	1. Jedes $A\subseteq V,|A|\geqslant n+1$ ist [[Lineare Unabhängigkeit|linear abhängig]]
	2. Jedes [[Erzeugendensysteme]] von $V$ enthält mindestens $n$ Elemente
	3. Jede Basis von $V$ besteht aus $n$ Elementen
→ Folgerung: [[Untervektorräume]] von [[Dimensionen|endlich-dimensionalen]] [[Vektorräume|Vektorräumen]] sind selbst wieder *endlich-dimensional*
^1670184569001
