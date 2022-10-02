---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases: Zeithierarchiesatz
date: 2022-08-17
mod-date: 2022-08-21
linter-yaml-title-alias: Zeithierarchiesatz
---

# Zeithierarchiesatz
-> [[../Hierarchiesätze|Hierarchiesätze]]

## Definition: #fc
- Seien $t_1,t_2$ Funktionen mit $\mathbb{N}\rightarrow\mathbb{N}$ mit $t_1\log t_1\notin\Omega(t_2)\wedge t_2\in\Omega(n\log n)\wedge t_2$ [[Zeitklassen/Zeitkonstruierbarkeit|zeitkonstruierbar]], dann giltt
$$DTIME(t_2)\setminus DTIME(t_1)\neq\emptyset$$
	-> $t_1\log(t_1)\notin\Omega(t_2)$ und $t_2\log(t_2)\notin\Omega(t_1)$ ist auch möglich
	-> Die notwendige Konstrquierbarkeit ist auf den [[../Lückensatz von Borodin|Lückensatz Von Borodin]] zurückzuführen
- Verwendet [[Satz von Hennie und Stearns|Satz von Hennie und Stearns]] (woher der Faktor $n\log n$ rührt)
- Folgerung: $DTIME(\mathcal{O}(n))\subsetneq DTIME(n^2)\subsetneq DTIME(2^n)\subsetneq DTIME(n\log n\cdot2^n)$
^1660502846790
