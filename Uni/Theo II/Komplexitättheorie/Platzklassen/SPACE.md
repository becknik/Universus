---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - DSPACE
  - NSPACE
linter-yaml-title-alias: SPACE
date-of-creation: 2022-10-24
mod-date: 2022-10-24
---

# SPACE

## Definition

### Deterministisch:
$$DSPACE(\mathcal{O}(f))=\bigcup_{g\in\mathcal{O}(f)}DSPACE(g)=\bigcup_{c\in\mathbb{N}}DSAPCE(c\cdot f)$$

### Nichtdeterministisch:
$$NSPACE(\mathcal{O}(f))=\bigcup_{g\in\mathcal{O}(f)}NSPACE(g)=\bigcup_{c\in\mathbb{N}}NSPACE(c\cdot f)$$
→ [[Satz von Immerman–Szelepcsényi|Satz von Immerman–Szelepcsényi]]
