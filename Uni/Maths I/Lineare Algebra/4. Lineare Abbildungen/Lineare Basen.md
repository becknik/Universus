---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Lineare Basen
  - Angeordnete Basis
linter-yaml-title-alias: Lineare Basen
date-of-creation: 2023-01-08
mod-date: 2023-01-09
---

# Lineare Basen

## Definition #fc
- Seien $V,W$ [[../3. Vektorräume/Vektorräume#Definition fc|Vektorräume]] und $f:V\to W$ eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]]
- Sei $B$ die [[../3. Vektorräume/Erzeugendensysteme#Definition fc|Basis]] von $V$
- Dann gilt: $f$ ist genau dann ein [[Lineare Abbildungen#Typen von Lineare Abbildungen Definition fc Linearen / ../3. Vektorräume/Vektorräume Definition fc Vektorraum - *Morphismen (6) fc|Vektorraum*iso*morphismus]] (= eine *bijektive lineare Abbildung*), wenn $f$ die *Basis* von $V$ auf die *Basis* von $W$ abbildet
^1673214625164

## Angeordnete Basis #fc
- Den [[../3. Vektorräume/Erzeugendensysteme#Basis fc|Basis]]-Vektoren wird eine Reihenfolge zugeordnet:
- Ist $\mathbf{t}=(v_1,\dots,v_n)\in V^n$ ein $n$-Tupel von Vektoren eines [[../3. Vektorräume/Vektorräume|Vektorraums]] $V$ der [[../3. Vektorräume/Dimensionen|Dimension]] $n,$ so dass die zu $\mathbf{t}$ zugehörige Teilmenge $\{v_1,\dots,v_n\}\in V^n$ eine *Basis* von $V$ ist, so nennt man das *Tupel* $\mathbf{t}=(v_1,\dots,v_n)$ eine *(angeordnete) Basis* von $V$
^1673214625172
> $t$ geht so schnell unter, deshalb habe ich mich für $\mathbf{t}$ entschieden

## Satz 4.2.2
- Angenommen $V,W$ sind zwei [[../3. Vektorräume/Vektorräume#Definition fc|Vektorräume]] und $f$ eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]]
1. Sei $E$ ein [[../3. Vektorräume/Erzeugendensysteme#Definition fc|Erzeugendensystem]] von $V,$ dann ist die Abbildung $f$ bereits durch durch Ihre Werte auf $v\in E$ eindeutig festgelegt
	→ Insbesondere gilt das für die [[../3. Vektorräume/Erzeugendensysteme#Basis fc|Basis]] von $V$
2. Umgekehrt: Sei $B$ eine *Basis* von $V$ und $f_0:B\to W$ eine [[../1. Logik-Mengenlehre-Relationen/Abbildungen#Definition fc|Abbildung]], so existiert eine eindeutig bestimmte *lineare Abbildung* $f:V\to W,$ so dass $\forall b\in B:f(b)=f_0(b)$
