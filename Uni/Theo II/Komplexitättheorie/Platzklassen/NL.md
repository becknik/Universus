---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: NL
linter-yaml-title-alias: NL
date-of-creation: 2022-08-11
mod-date: 2022-10-24
---

# NL

## Definition:
$$NL = NSPACE(\log n)=NSPACE(\mathcal{O}(\log n))$$
- [[../Translationssätze|Translationssatz für Platzklassen]]: $DSPACE(n)\subsetneq NSPACE(n)\Rightarrow$ [[L|L]] $\subsetneq NL$

## Beispiele #fc
- *Universalität von [[../../../Theo I/3. Typ - REG/Deterministischer Endlicher Automat|DFAs]]**
	→ *Gegeben*: DFA $A$, Frage: $T(A)=\Sigma^{Stern}?$
	→ $NL\subsetneq PSPACE$, da das Problem für NFAs [[PSPACE]]-vollständig ist und die Probleme so weit auseinander sind
^1660858067801

### NL-Vollständigkeit: #fc
- [[../Probleme/Grapherreichbarkeitsproblem|GAP/ ST-connectivity]] ist $\leq_{\log}$-vollständig für $\text{NL}$
- 2-[[../Probleme/Satisfiability|SAT]] ist $\leq_{\log}$-vollständig
	→ $GAP\leq_{\log}\text{2-NSAT}$
	→ Kolar [[Satz von Immerman–Szelepcsényi|Satz von Immerman–Szelepcsényi]]: $2SAT$ ist NL-vollständig $\Leftrightarrow 2NSAT$ (V. 39.3)
- Das [[../../../Theo I/Wortproblem|Wortproblem]] für [[../../../Theo I/3. Typ - REG/Nichtdeterministischer Endlicher Automat|NFAs]] ist NL-vollständig
^1660943198010
