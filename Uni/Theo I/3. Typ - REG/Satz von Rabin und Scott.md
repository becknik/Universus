---
tags: uni theo-1 theoretical-cs automata theorem
cards-deck: Uni::Courses::Theo-I
completed: true
aliases: Satz von Rabin und Scott
linter-yaml-title-alias: Satz von Rabin und Scott
date-of-creation: 2022-09-15
mod-date: 2022-09-16
---

# Satz von Rabin und Scott

## Aussage: #fc
- Für jede Sprache $L\in\Sigma^{Stern}:$ Wenn einen [[Nichtdeterministischer Endlicher Automat|NFA]] $M$ mit $T(M)=L$ existiert, dann existiert auch ein [[Deterministischer Endlicher Automat|DFA]] $M'$ mit $T(M')=L$
	→ $\text{NFA}\subseteq\text{DFA}$
- Allerdings können die resultierenden DFAs eine deutlich höhere Zustandsmenge aufweisen als die äquivalenten NFAs (im Extrem: *Exponentielles Blow-Up*)
	→ [[Potenzmengenkonstruktion]]
^1664631006685
