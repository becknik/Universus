---
tags: uni theo-1 theoretical-cs
cards-deck: Uni::Courses::Theo-I
completed: true
aliases: Homomorphismus
linter-yaml-title-alias: Homomorphismus
date-of-creation: 2022-09-25
mod-date: 2022-09-25
---

# Homomorphismus

## Definition: #fc
- Gegeben seinen die [[../Monoid|Monoide]] $(M_1,\circ_1,\varepsilon_1),(M_2,\circ_2)$
- Die Funktion $h:M_1\rightarrow M_2$ ist genau dann ein Homomorphismus, wenn folgende Bedingungen erfüllt sind:
	- $\forall x,y\in M_1:h(x\circ_1 y)=h(x)\circ_2 h(y)$
	- $h(\varepsilon_1)=\varepsilon_2$ für die Neutralen Elemente aus $M_1,M_2$
^1664736223337
