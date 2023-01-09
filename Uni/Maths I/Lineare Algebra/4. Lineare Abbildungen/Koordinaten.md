---
tags: uni maths maths-1 matrix
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Koordinaten
  - Koordinatenfunktion
linter-yaml-title-alias: Koordinaten
date-of-creation: 2023-01-08
mod-date: 2023-01-09
---

# Koordinaten

## Definition #fc
- Sei $V$ ein [[../3. Vektorräume/Vektorräume#Definition fc|Vektorraum]] mit der [[../3. Vektorräume/Erzeugendensysteme#Basis fc|Basis]] $B=(v_1,\dots,v_n),$ dann hat jedes $v'\in V$ eine eindeutige Darstellung als [[../3. Vektorräume/Linearkombinationen#Definition fc|Linearkombination]] der Elemente der Basis: $$v'=\lambda_1v_1+\dots+\lambda_n v_n$$
- Das Tupel $(\lambda_1,\dots,\lambda_n),\lambda_i\in K$ wird als *Koordinaten* des Vektors bezüglich $B$ bezeichnet
^1673212646887

## Koordinatenfunktion

### Definition #fc
- Die Abbildung $$\Phi_B\rightarrow K^n,\lambda_1v_1+\dots+\lambda_nv_n\mapsto\begin{pmatrix}\lambda_1\\\vdots\\\lambda_n\end{pmatrix},$$ die zu jedem Vektor $v\in V$ eine Koordinaten bezüglich der [[../3. Vektorräume/Erzeugendensysteme#Basis fc|Basis]] $B$ zuordnet heißt *Koordinatenabbildung*
	→ $\Phi_B$ ist ein [[Lineare Abbildungen#Typen von Lineare Abbildungen Definition fc Linearen / ../3. Vektorräume/Vektorräume Definition fc Vektorraum - *Morphismen (6) fc|Vektorraumisomorphismus]]
	→ Wählt man $B$ als die [[../3. Vektorräume/Erzeugendensysteme#Standard-/ Kanonische Basis fc|Standard-/ kanonische Basis]] $e_1,\dots,e_n$ von $K^n,$ so ist $\Phi_B=id_{K^n}$
^1673215016364
