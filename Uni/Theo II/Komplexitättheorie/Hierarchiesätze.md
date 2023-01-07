---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Hierarchiesätze
  - Zeithierarchiesatz
  - Platzhierarchiesatz
linter-yaml-title-alias: Hierarchiesätze
date-of-creation: 2022-08-12
mod-date: 2022-10-24
---

# Hierarchiesätze

## Aussage: #fc
- Allgemein: "*Mehr kann mehr*"
- Existieren es jeweils auch im Nichtdeterminismus
	→ Bei $NTIME$ lassen sich die Forderungen allerdings weiter aufweichen
^1660502846781

## Platz

### Definition: #fc
- Seien $s_1,s_2$ Funktionen mit $\mathbb{N}\rightarrow\mathbb{N}$ und $s_1\notin\Omega(s_2)\wedge s_2\in\Omega(\log(n))\wedge s_2$ ist [[Konstruierbarkeit|platzkonstruierbar]], dann gilt:
$$DSPACE(s_2)\setminus DSPACE(s_1)\neq\emptyset$$
- $\exists$Fälle, in denen $s_1\notin\Omega(s_2)$ (=$s_1$ aber nicht zwingend die kleinere Funktion sein muss) und $s_2\notin\Omega(s_1)$ gilt: $s_1\in \mathcal{o}(s_2)\Rightarrow s_1\notin\Omega(s_2)$
	→ [[../../Theo-III/Landau-Notationen|Landau-Notationen]]
- Der [[Lückensatz von Borodin]] macht die Konstruierbarkeit notwendig
^1660733029827

### Folgerungen: #fc
- $DSPACE(\log)\subsetneq DSPACE(\log^2)\subsetneq\dots$ oder auch $DSPACE(n^{100})\subsetneq$ [[Komplexitättheorie/Platzklassen/PSPACE|PSPACE]]
- $DSPACE(n^k)\subsetneq DSPACE(2^n)$
- [[Komplexitättheorie/Platzklassen/NL|NL]] $\subsetneq DSPACE(\log^k n)$ ([[Komplexitättheorie/Platzklassen/Satz von Savitch|Satz von Savitch]]) $\subsetneq DSPACE(n)\subsetneq$ [[Komplexitättheorie/Platzklassen/PSPACE|PSPACE]]
^1660733029838

### Weiteres:
- Ohne Einschränkungen sei $2\log_2(n)<s_2(n)$
- Beispiel: $NSPACE\subseteq DSPACE(n^2)\subsetneq DSPACE(n^2\log n)\subseteq NSPACE(n^2\log n)$

## Zeit

### Definition: #fc
- Seien $t_1,t_2$ Funktionen mit $\mathbb{N}\rightarrow\mathbb{N}$ und $t_1\log(t_1)\notin\Omega(t_2)\wedge t_2\in\Omega(n\log(n))\wedge t_2$ ist [[Konstruierbarkeit|zeitkonstruierbar]], dann gilt:
$$DTIME(t_2)\setminus DTIME(t_1)\neq\emptyset$$
- $t_1\log(t_1)\notin\Omega(t_2)$ und $t_2\log(t_2)\notin\Omega(t_1)$ ist auch möglich
- Der [[Lückensatz von Borodin]] macht die Konstruierbarkeit notwendig
^1660502846790

### Weiteres:
- Verwendet [[Satz von Hennie und Stearns|Satz von Hennie und Stearns]] Anwendung

### Beispiel:
- $DTIME(\mathcal{O}(n))\subsetneq DTIME(n^2)\subsetneq DTIME(2^n)\subsetneq DTIME(n\log n\cdot2^n)$
