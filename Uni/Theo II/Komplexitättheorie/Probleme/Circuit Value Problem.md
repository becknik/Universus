---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Circuit Value Problem
  - CVP
date-of-creation: 2022-08-12
mod-date: 2022-08-18
linter-yaml-title-alias: Circuit Value Problem
---

# Circuit Value Problem

## Definition: #fc
- *Gegeben*: Ein boolescher Schaltkreis $C=(\{1,\dots,n\},E,s)$
	- Ein [[../../../DSA/Graphen/Gerichteter Azyklischer Graph|gerichteter azyklischer Graph]] $C$ mit den Kontenmarkierungen $s:\{1,\dots,n\}\rightarrow\{\neq,\wedge,\vee,T(RUE),F(ALSE)\}$
	- $V=\{1,\dots,n\},n=$ Output von $C$
	- $E\subseteq V\times V, \forall(i,j)\in E:i<j$
	- Sorte des Knotens $i:s(i)$
		- $s(i)\in\{\wedge,\vee\}\Rightarrow$ Eingangsgrad von $i$ ist 2
		- $s(i)=\neg\Rightarrow$ Eingangsgrad von $i$ ist 1
		- $s(i)\in\{T,F\}\Rightarrow$ Eingangsgrad von $i$ ist 0
	→ Jedem Knoten kann von hinten nach vorne ein boolescher Wert zugeordnet werden
- *Gesucht*: Ist der Output von $n$ der Wert T(RUE)
	→ CVP und MCVP (=ohne Negationen) sind $\leq_{\log}-$vollständig für [[../Zeitklassen/P|P]] (→ [[../Logspace-Reduktion|Logspace-Reduktion]])
^1660857829772

## Unterschied Zu Formeln:
- Jeder [[../../Logik/Aussagenlogik|Formel]] kann man einen Schaltkreis zuordnen
- Jeden Schaltkreis kann man in eine exponentielle Formel umwandeln
	→ Bei Schaltkreisen lassen sich Teilformeln ohne Aufblähung wiederverwenden
