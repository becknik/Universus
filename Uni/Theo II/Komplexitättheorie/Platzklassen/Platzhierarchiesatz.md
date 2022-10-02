---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases: Platzhierarchiesatz
date: 2022-08-17
mod-date: 2022-08-20
linter-yaml-title-alias: Platzhierarchiesatz
---

# Platzhierarchiesatz
-> [[../Hierarchiesätze|Hierarchiesätze]]

## Definition: #fc
- Seien $s_1,s_2$ Funktionen mit $:\mathbb{N}\rightarrow\mathbb{N}$ und $s_1\notin\Omega(s_2)\wedge s_2\in\Omega(\log(n))\wedge s_2$ [[Platzklassen/Platzkonstruierbarkeit|platzkonstruierbar]], dann gilt:
$$DSPACE(s_2)\setminus DSPACE(s_1)\neq\emptyset$$
- $\exists$Fälle, in denen $s_1\notin\Omega(s_2)$ (=$s_1$ aber nicht zwingend die kleinere Funktion sein muss) und $s_2\notin\Omega(s_1)$ gilt: $s_1\in \mathcal{o}(s_2)\Rightarrow s_1\notin\Omega(s_2)$
	-> [[../../../DSA/Landau-Notationen|Landau-Notationen]]
- Der [[../Lückensatz von Borodin|Lückensatz Von Borodin]] macht die Konstruierbarkeit notwendig
- Ohne Einschränkungen sei $2\log_2(n)<s_2(n)$
- Beispiel: $NSPACE\subseteq DSPACE(n^2)\subsetneq DSPACE(n^2\log n)\subseteq NSPACE(n^2\log n)$
^1660733029827

## Folgerungen: #fc
- $DSPACE(\log)\subsetneq DSPACE(\log^2)\subsetneq\dots$ oder auch $DSPACE(n^{100})\subsetneq$ [[Komplexitättheorie/Platzklassen/PSPACE|PSPACE]]
- $DSPACE(n^k)\subsetneq DSPACE(2^n)$
- [[Komplexitättheorie/Platzklassen/NL|NL]] $\subsetneq DSPACE(\log^k n)$ ([[Komplexitättheorie/Platzklassen/Satz von Savitch|Satz Von Savitch]]) $\subsetneq DSPACE(n)\subsetneq$ [[Komplexitättheorie/Platzklassen/PSPACE|PSPACE]]
^1660733029838
