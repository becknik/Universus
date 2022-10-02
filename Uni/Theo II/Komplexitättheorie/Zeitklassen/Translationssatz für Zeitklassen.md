---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases: Translationssatz für Zeitklassen
date: 2022-08-17
mod-date: 2022-08-18
linter-yaml-title-alias: Translationssatz für Zeitklassen
---

# Translationssatz für Zeitklassen

## Definition: #fc
- Seien $g,f$ zwei [[Zeitkonstruierbarkeit|zeitkonstruierbare]] Funktionen und $\forall n: n\leq g(n),f(n)$ sowie $L\subseteq\Sigma^{Stern},$ dann gilt
1. $Pad_f(L)\in DTIME(\mathcal{O}(g))\Leftrightarrow L\in DTIME(\mathcal{O}(g\circ f))$
2. $Pad_f(L)\in NTIME(\mathcal{O}(g))\Leftrightarrow L\in NTIME(\mathcal{O}(g\circ f))$
-> Mit jedem Vor- und Zurückspringen zwischen $Pad_(L)$ und $L$ vergrößert sich die Konstante der [[../../../DSA/O-Notation|O-Notation]]
^1660502907005
