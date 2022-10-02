---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases: Translationssatz für Platzklassen
date: 2022-08-18
mod-date: 2022-08-19
linter-yaml-title-alias: Translationssatz für Platzklassen
---

# Translationssatz für Platzklassen
-> [[Translationstechnik|Translationstechnik]]

## Definition: #fc
- Seien $g,f$ zwei Funktionen, $g\in\Omega(\log)\wedge\forall n:n\leq f(n)$
- Sei $f(n)$ für unär kodierte Zahlen $n~\in\mathcal{O}(g\circ f)$, dann gilt
1. $Pad_f(L)\in DSPACE(\mathcal{O}(g))\Leftrightarrow L\in DSPACE(\mathcal{O}(g\circ f))$
2. $Pad_f(L)\in NSPACE(\mathcal{O}(g))\Leftrightarrow L\in NSPACE(\mathcal{O}(g\circ f))$
-> Mit jedem Vor- und Zurückspringen zwischen $Pad_(L)$ und $L$ vergrößert sich die Konstante der [[../../../DSA/O-Notation|O-Notation]]
^1660860179900
