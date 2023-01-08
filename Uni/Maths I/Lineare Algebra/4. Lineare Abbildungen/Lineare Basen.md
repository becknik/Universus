---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Lineare Basen
  - Angeordnete Basis
linter-yaml-title-alias: Lineare Basen
date-of-creation: 2023-01-08
mod-date: 2023-01-08
---

# Lineare Basen

## Definition #fc
- Seien $V,W$ [[../3. Vektorräume/Vektorräume#Definition fc|Vektorräume]] und $f:V\to W$ eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]]
- Sei $B$ die [[../3. Vektorräume/Erzeugendensystem#Definition fc|Basis]] von $V$
- $f$ genau dann ein [[Lineare Abbildungen#Typen von Lineare Abbildungen Definition fc Linearen / ../3. Vektorräume/Vektorräume Definition fc Vektorraum - *Morphismen (6) fc|Vektorraum*iso*morphismus]] (= eine *bijektive lineare Abbildung*), wenn $f$ die Basis von $V$ auf die Basis von $W$ abbildet
^1673214625164

## Angeordnete Basis #fc #TODO
- Den [[../3. Vektorräume/Erzeugendensystem#Basis fc|Basis]]-Vektoren wird eine Reihenfolge zugeordnet:
- Ist $t=(v_1,\dots,v_n)\in V^n$ ein $n$-Tupel von Vektoren eines $n$-dimensionalen [[../3. Vektorräume/Vektorräume|Vektorraums]] $V$, so dass $\{v_1,\dots,v_n\}\subseteq(v_1,\dots,v_n)$ eine *Basis* ist, so nennt man $t$ eine *(angeordnete) Basis* von $V$
^1673214625172

## Satz 4.2.2
- Angenommen $V,W$ sind zwei [[../3. Vektorräume/Vektorräume#Definition fc|Vektorräume]] und $f$ eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]]
1. Sei $E$ ein [[../3. Vektorräume/Erzeugendensystem#Definition fc|Erzeugendensystem]] von $V,$ dann ist die Abbildung $f$ bereits durch durch Ihre Werte auf $v\in E$ eindeutig festgelegt
	→ Insbesondere gilt das für die [[../3. Vektorräume/Erzeugendensystem#Basis fc|Basis]] von $V$
2. Umgekehrt: Sei $B$ eine *Basis* von $V$ und $f_0:B\to W$ eine [[../1. Logik-Mengenlehre-Relationen/Abbildungen#Definition fc|Abbildung]], so existiert eine eindeutig bestimmte *lineare Abbildung* $f:V\to W,$ so dass $\forall b\in B:f(b)=f_0(b)$
