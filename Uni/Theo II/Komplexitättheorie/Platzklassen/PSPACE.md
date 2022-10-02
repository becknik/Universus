---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases:
  - PSPACE
  - IP
linter-yaml-title-alias: PSPACE
date: 2022-08-11
mod-date: 2022-09-10
---

# PSPACE

## Definition:
$$\text{IP}=\text{PSPACE}=\bigcup_{k\geq1}\text{DSPACE}(n^k)=\bigcup_{k\geq1}\text{NSPACE}(n^k)$$

## Eigenschaften: #fc
- [[NL]] $\neq PSPACE$
- [[Satz von Savitch]]: $NSPACE(n^k)\subseteq DSPACE(n^{2k})$
	-> Definition über $\text{DSPACE}$ und $\text{NSPACE}$
- [[../Hierarchiesätze|Hierarchiesätze]]: $\text{DSPACE}(n^k)\subsetneq\text{DSPACE}(2^n)=\text{EXPSPACE}$
- Der Verdacht besteht, dass Probleme $\in\text{PSPACE}$ nicht lösbar sind
	-> Ähnlich so wie bei [[../Zeitklassen/NP|NP]], [[../Zeitklassen/EXPTIME|EXPTIME]] oder [[../../Entscheidbarkeit/Rekursiv Aufzählbar|RE]]
^1660502953305

## Beispiele: #fc
- Das Quantifizierbare Boolesche Formeln [[../Probleme/Quantifizierte Boolesche Formeln|QBF]] ist *PSPACE-vollständig*
- Mathematische Spiele: "Existiert ein Zug für alle anderen Züge?" sind auch *PSPACE-vollständig*
- Die *Universalität von [[NFA]]*: $L(\text{NFA } A)=\Sigma^{Stern}?$ ist PSPACE-volständig[^1]
	-> [[NL]] $\subsetneq$ [[PSPACE]], da das Entscheidungsproblem zur Universalität von [[../../../Theo I/3. Typ - REG/Deterministischer Endlicher Automat|DFA]] $\in\text{NL}$ liegt
^1660856844947

[^1]:[stackovercoder](https://stackovercoder.com.de/cs/70129/what-is-the-complexity-for-the-universality-problem-for-a-nfa-with-all-states-ac)
