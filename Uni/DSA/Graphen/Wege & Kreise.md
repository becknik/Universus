---
tags: uni dsa practical-cs problem graph
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Wege & Kreise
  - Eulerscher Weg
  - Eulerscher Kreis
  - Hamiltonscher Weg
  - Hamiltonscher Kreis
linter-yaml-title-alias: Wege & Kreise
date-of-creation: 2022-07-23
mod-date: 2022-09-10
---

# Wege & Kreise

## Königsberger Brückenproblem: #fc
![|250](https://upload.wikimedia.org/wikipedia/commons/5/5d/Konigsberg_bridges.png)
- Ist es möglich einen Rundgang durch Königsberg zu machen und jede der 7 Brücken genau einmal zu besuchen?
	→ Der Königsberger Brückengraph ist nicht Euler'sch
<sub>[Pictures Source](https://upload.wikimedia.org/wikipedia/commons/5/5d/Konigsberg_bridges.png)</sub>
^1653921006325

## Euler: #fc
- **Euler'scher Weg**: Jede *Kante* des Graphen kommt *genau einmal* in einem Pfad $u_0, u_1, …, u_k$ vor
	→ Falls genau *2 Knoten* in einem [[Ungerichtete Graphen|ungerichteten Graphen]] einen *ungeraden Grad* haben, so hat der Graph nur einen Euler'schen Weg
- **Euler'scher Kreis**: Ein Euler'scher Weg, bei dem $u_k = u_0$ ist
	→ Satz: Ein [[Ungerichtete Graphen|ungerichteter Graph]] besitzt einen Euler'schen Kreis, wenn *alle* seine Knoten einen *geraden Grad* aufweisen
^1658939262955

## Hamilton: #fc
- **Hamilton'scher Weg**: Im Pfad $u_1, u_1, …, u_n$ kommt jeder Knoten genau einmal vor
- **Hamilton'scher Kreis**: Ein Hamilton'scher Weg, bei dem sich der Startknoten mit dem Endknoten verbinden lässt
	→ Das Finden eines Hamilton'schen Kreises ist ein [[../../../Theo II/Komplexitättheorie/Zeitklassen/NP|NP-vollständiges]] Problem
	→ Gesucht: Die Permutation $\pi$ der Knotenindizes $(v_{\pi(1)},v_{\pi(2)},\dots,v_{\pi(n)})$, so dass für $i=1,\dots,n-1:(v_{\pi(i)},v_{\pi(i+1)})\in E \wedge(v_{\pi(n)},v_{\pi(1)})\in E$
^1658939262959
