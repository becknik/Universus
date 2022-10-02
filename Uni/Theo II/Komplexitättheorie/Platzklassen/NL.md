---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases: NL
date: 2022-08-11
mod-date: 2022-08-23
linter-yaml-title-alias: NL
---

# NL

## Definition:
$$NL = NSPACE(\log n)=NSPACE(\mathcal{O}(\log n))$$
- [[Translationssatz für Platzklassen|Translationssatz für Platzklassen]]: $DSPACE(n)\subsetneq NSPACE(n)\Rightarrow$ [[L|L]] $\subsetneq NL$

## Beispiele #fc
- Universalität von DFAs: Gegeben: DFA $A$, Frage: $L(A)=\Sigma^{Stern}?$
	-> Die Universalität von NFAs ist [[PSPACE]]-vollständig, also $NL\subsetneq PSPACE,$ da die Probleme so weit auseinander sind
^1660858067801

### NL-Vollständigkeit: #fc
- [[../Probleme/Grapherreichbarkeitsproblem|GAP]]/ST-connectivity ist $\leq_{\log}$-vollständig für NL
- $\text{2-SAT}$ ist $\leq_{\log}$-vollständig ($GAP \leq_{\log}\text{2-NSAT}$)
	-> $2SAT$ ist NL-vollständig $\Leftrightarrow 2NSAT$ ist NL-vollständig ([[Satz von Immerman–Szelepcsényi|Satz von Immerman–Szelepcsényi]]) (V39.3)
- Das Wortproblem für NFAs ist NL-vollständig
^1660943198010
