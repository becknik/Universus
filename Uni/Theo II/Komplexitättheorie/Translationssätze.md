---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Translationssätze
  - Translationssatz für Zeitklassen
  - Translationssatz für Platzklassen
linter-yaml-title-alias: Translationssätze
date-of-creation: 2022-10-24
mod-date: 2022-10-24
---

# Translationssätze

## Platz

### Definition: #fc
- Seien $g,f$ Funktionen
- Sei $g\in\Omega(\log)\wedge\forall n:n\leq f(n)$
- Sei $f(n)$ für unär kodierte Zahlen $n~\in\mathcal{O}(g\circ f)$, dann gilt
	1. $Pad_f(L)\in DSPACE(\mathcal{O}(g))\Leftrightarrow L\in DSPACE(\mathcal{O}(g\circ f))$
	2. $Pad_f(L)\in NSPACE(\mathcal{O}(g))\Leftrightarrow L\in NSPACE(\mathcal{O}(g\circ f))$
- *Aussage*: Mit jedem Vor- und Zurückspringen zwischen $Pad_(L)$ und $L$ vergrößert sich die Konstante der [[../../../DSA/O-Notation|O-Notation]]
^1660860179900

## Zeit

### Definition #fc
- Seien $g,f$ [[Konstruierbarkeit|zeitkonstruierbare]] Funktionen, $\forall n: n\leq g(n)\wedge n\leq f(n)$ sowie $L\subseteq\Sigma^{Stern},$ dann gilt:
	1. $Pad_f(L)\in DTIME(\mathcal{O}(g))\Leftrightarrow L\in DTIME(\mathcal{O}(g\circ f))$
	2. $Pad_f(L)\in NTIME(\mathcal{O}(g))\Leftrightarrow L\in NTIME(\mathcal{O}(g\circ f))$
- *Aussage*: Mit jedem Vor- und Zurückspringen zwischen $Pad_(L)$ und $L$ vergrößert sich die Konstante der [[../../../DSA/O-Notation|O-Notation]]
^1660502907005
