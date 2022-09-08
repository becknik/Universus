---
tags: uni dsa practical-cs problem graph
cards-deck: Uni::Courses::DSA
status: unfinished
aliases:
  - Wege & Kreise
  - Eulerscher Weg
  - Eulerscher Kreis
  - Hamiltonscher Weg
  - Hamiltonscher Kreis
linter-yaml-title-alias: Wege & Kreise
date: 2022-07-23
mod-date: 2022-09-01
---

# Wege & Kreise
![|250](https://upload.wikimedia.org/wikipedia/commons/5/5d/Konigsberg_bridges.png)

## Königsberger Brückenproblem: #fc
Ist es möglich einen Rundgang durch Königsberg zu machen und jede der 7 Brücken genau einmal zu besuchen?
	-> Der Königsberger Brückengraph ist nicht Euler'sch
^1653921006325

## Euler: #fc
- **Euler'scher Weg**: Jede *Kante* des Graphen kommt *genau einmal* in einem Pfad $u_0, u_1, …, u_k$ vor
	-> Falls genau *2 Knoten* in einem [[Ungerichteter Graph|ungerichteten Graphen]] einen *ungeraden Grad* haben, so hat der Graph nur einen Euler'schen Weg
- **Euler'scher Kreis**: Ein Euler'scher Weg, bei dem $u_k = u_0$ ist
	-> Satz: Ein [[Ungerichteter Graph|ungerichteter Graph]] besitzt einen Euler'schen Kreis, wenn *alle* seine Knoten einen *geraden Grad* aufweisen
^1658939262955

## Hamilton: #fc
- **Hamilton'scher Weg**: Im Pfad $u_1, u_1, …, u_n$ kommt jeder Knoten genau einmal vor
- **Hamilton'scher Kreis**: Ein Hamilton'scher Weg, bei dem sich der Startknoten mit dem Endknoten verbinden lässt
	-> Das Finden eines Hamilton'schen Kreises ist ein [[../../../Theo II/Komplexitättheorie/Zeitklassen/NP|NP-vollständiges]] Problem
	-> Gesucht: Die Permutation $\pi$ der Knotenindizes $(v_{\pi(1)},v_{\pi(2)},\dots,v_{\pi(n)})$, so dass für $i=1,\dots,n-1:(v_{\pi(i)},v_{\pi(i+1)})\in E \wedge(v_{\pi(n)},v_{\pi(1)})\in E$
^1658939262959