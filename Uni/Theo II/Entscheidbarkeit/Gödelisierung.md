---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: false
aliases:
  - Gödelisierung
  - Gödelindex
date: 2022-07-03
mod-date: 2022-08-09
linter-yaml-title-alias: Gödelisierung
---

# Gödelisierung

## Definition:
- Eine Kodierung, bei der $\forall w \in \{0,1\}^{Stern}$ auf eine eindeutige, [[Berechenbarkeit|berechenbarer]] Weise einer [[../../Theo I/Turingmaschinen|TM]] $M_w$ zugeordnet werden
	-> Nicht immer gilt $w = w'$, wohl aber $M_w = M_{w'}$

## Herleitung:
- Sei $M = (Z, \Sigma, \Gamma, \delta, z_0, e, \square)$ eine [[../../Theo I/Turingmaschinen|TM]].
- $M$ lässt sich in einer *Meta-Sprache* als endliche Zeichenkette (z.B. in [[../../Ro I/Zahlen & Kodierung/ASCII|ASCII]]) aufschreiben
- Definiere die [[../../Maths/Injektive Funktion|injektive Funktion]] $G: M\rightarrow\{1,0\}$
	-> $G(M)$ ist nicht [[../../Maths/Surjektive Funktion|surjektiv]]
- Für Surjektivität: Sei $M_0$ eine feste, triviale TM, sodass $\forall M, G(M) \neq w: G(M) =$ Kodierung für $M_0$
