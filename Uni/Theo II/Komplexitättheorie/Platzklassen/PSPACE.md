---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - PSPACE
  - IP
linter-yaml-title-alias: PSPACE
date-of-creation: 2022-08-11
mod-date: 2022-10-24
---

# PSPACE

## Definition:
$$\text{PSPACE}=\bigcup_{k\geq1}\text{DSPACE}(n^k)=\bigcup_{k\geq1}\text{NSPACE}(n^k)=\text{IP}$$

## Eigenschaften: #fc
- [[NL]] $\neq\text{PSPACE}$
- [[Satz von Savitch]]: $NSPACE(n^k)\subseteq DSPACE(n^{2k})$
	→ Definition über $\text{DSPACE}$ und $\text{NSPACE}$
- [[../Hierarchiesätze|Hierarchiesätze]]: $\text{DSPACE}(n^k)\subsetneq\text{DSPACE}(2^n)=\text{EXPSPACE}$
^1660502953305

## Beispiele

### $\text{PSPACE}$-Vollständigkeit #fc
- [[../Probleme/Quantifizierte Boolesche Formeln|QBF]]
- Mathematische Spiele
	→ "Existiert ein Zug für alle anderen Züge?"
- Die *Universalität von [[../../../Theo I/3. Typ - REG/Nichtdeterministischer Endlicher Automat|NFAs]]*
	→ $L(\text{NFA } A)=\Sigma^{Stern}?$ ist PSPACE-volständig[^1]
	→ [[NL]] $\subsetneq$ [[PSPACE]], da das Entscheidungsproblem zur Universalität von DFA $\in\text{NL}$ liegt
^1660856844947

[^1]:[stackovercoder](https://stackovercoder.com.de/cs/70129/what-is-the-complexity-for-the-universality-problem-for-a-nfa-with-all-states-ac)
