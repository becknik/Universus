---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: false
aliases:
  - Gödelisierung
  - Gödelindex
linter-yaml-title-alias: Gödelisierung
date-of-creation: 2022-07-03
mod-date: 2022-10-20
---

# Gödelisierung

## Definition:
- Eine Kodierung, bei der $\forall w \in \{0,1\}^{Stern}$ auf eine eindeutige, [[Berechenbarkeit|berechenbarer]] Weise einer [[../../Theo I/Turingmaschinen|TM]] $M_w$ zugeordnet werden
	→ Nicht immer gilt $w = w'$, wohl aber $M_w = M_{w'}$

## Herleitung:
- Sei $M = (Z, \Sigma, \Gamma, \delta, z_0, e, \square)$ eine [[../../Theo I/Turingmaschinen|TM]].
- $M$ lässt sich in einer *Meta-Sprache* als endliche Zeichenkette (z.B. in [[../../Ro I/Zahlen & Kodierung/ASCII|ASCII]]) aufschreiben
- Definiere die *injektive Funktion* $G: M\rightarrow\{1,0\}$
	→ $G(M)$ ist nicht *surjektiv*
- Für Surjektivität: Sei $M_0$ eine feste, triviale TM, sodass $\forall M, G(M) \neq w: G(M) =$ Kodierung für $M_0$
