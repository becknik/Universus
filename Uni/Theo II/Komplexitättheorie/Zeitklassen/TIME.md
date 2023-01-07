---
tags: uni theo-2 theoretical-cs complexity
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - DTIME
  - NTIME
linter-yaml-title-alias: TIME
date-of-creation: 2022-08-12
mod-date: 2022-10-24
---

# TIME

## Definition

### Deterministisch:
$$DTIME(\mathcal{O}(f))=\bigcup_{g\in\mathcal{O}(f)}DTIME(g)=\bigcup_{c\in\mathbb{N}}DTIME(c\cdot f)$$

### Nichtdeterministisch: #fc
$$NTIME(\mathcal{O}(f))=\bigcup_{g\in\mathcal{O}(f)}NTIME(g)=\bigcup_{c\in\mathbb{N}}NTIME(c\cdot f)$$
- Wenn die Eingabe $x$ von einer [[../../../Theo I/Turingmaschinen|NTM]] $M$ auf *mindestens einem Weg akzeptiert*, gibt $ntime_M(x)$ die *minimale Länge* aller akzeptierenden Pfade an
	→ Falls $M$ $x$ nicht akzeptiert gilt: $ntime_M(x) = 0$
^1666634833565
