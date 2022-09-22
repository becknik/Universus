---
tags: uni theo-1 theoretical-cs automata theorem
cards-deck: Uni::Courses::Theo-I
complete: true
aliases: Satz von Rabin und Scott
linter-yaml-title-alias: Satz von Rabin und Scott
date: 2022-09-15
mod-date: 2022-09-16
---

# Satz von Rabin und Scott

## Aussage:
- Für jede Sprache $L\in\Sigma^*:$ Wenn einen [[Nichtdeterministischer Endlicher Automat|NFA]] $M$ mit $T(M)=L$ existiert, dann existiert auch ein [[Deterministischer Endlicher Automat|DFA]] $M'$ mit $T(M')=L$
	-> $\text{NFA}\subseteq\text{DFA}$
- Allerdings können die resultierenden DFAs eine deutlich höhere Zustandsmenge aufweisen als die äquivalenten NFAs (im Extrem: *Exponentielles Blow-Up*)
	-> [[Potenzmengenkonstruktion]]
