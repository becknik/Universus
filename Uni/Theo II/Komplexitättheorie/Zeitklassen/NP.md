---
tags: uni theo-2 theoretical-cs abstraction complexity solvability
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: NP
linter-yaml-title-alias: NP
date-of-creation: 2022-07-09
mod-date: 2022-10-24
---

# NP

## Definition: #fc
→ [[NP/NP-Härte|NP-Härte]], [[NP/NP-Vollständigkeit|NP-Vollständigkeit]]
- Für jedes beliebige Polynom $p$ ist $\text{NP}$ definiert als $$NP = \bigcup_{\text{Polynom }p} NTIME(p)$$
	→ [[TIME|NTIME]]
- *Alternative Definition*: $\{A \mid\exists p,~\exists M \in$ [[../../../Theo I/Turingmaschinen|NTM]] $, ~T(M)=A \wedge \forall x: ntime_M(x) \leq p(|x|)\}$
^1660503052355

## Eigenschaften: #fc
- [[P-NP-Problem]]
- [[NP/Satz von Cook|Satz Von Cook]]: Sei $L \in\text{NP}$ beliebig $\Rightarrow L \in$ [[EXPTIME]]
	→ Laut [[NP/Satz von Cook|Cook]]: $\forall L\in\text{NP}:$ Es lässt sich eine Formel $F$ erstellen, die in $dtime(2^{c\cdot n})$ für ein geeignetes $c$ und polynomiell großen $n$ entschieden werden kann
- NP $\subseteq$ [[../../Berechenbarkeit/LOOP-berechenbar|LOOP-berechenbar]]
- Nachweis für die Zugehörigkeit in $\text{NP}$ funktioniert meistens über durch [[NP/Guess and Check|Guess And Check]]
- Klasse enthält viele für die Praxis wichtige Probleme
	→ Meistens haben sie eine exponentielle, seltenst eine sub-exponentielle ($\mathcal{O}(2^\sqrt{n}n)$) Laufzeit oder können erst gar nicht gelöst werden
^1660503052362

## Beispiele

### [[NP/NP-Vollständigkeit]]: #fc
→ Alle bekannten Probleme $\in\text{NP}$ sind auch unter [[../Logspace-Reduktion|Logspace-Reduktionen]] $\text{NP}$-vollständig
- [[../Probleme/Satisfiability|SAT]]
- [[../Probleme/3KNF-SAT|3KNF-SAT]] durch $\text{SAT}\leq_p\text{3KNF-SAT}$
- [[../Probleme/CLIQUE|CLIQUE]] durch $\text{SAT}\leq_p\text{CLIQUE}$
- [[../Probleme/FÄRBBARKEIT|FÄRBBARKEIT]]
- [[../Probleme/Traveling Salesman Problem|TSP]]
- [[../Probleme/Vertex Cover|Vertex Cover]]
- [[../../../DSA/Graphen/Wege & Kreise|Hamilton Kreis]], [[../../../DSA/Probleme/Rucksackproblem|Rucksackproblem]]
- Aus *Schöning's Buch*:
	- $\text{3-KNF-SAT}\leq_p\text{MENGENÜBERDECKUNG}$
	- $\text{KNOTENÜBERDECKUNG}$
	- $\text{PARTITION}$
	- $\text{BIN PACKING}$
^1660944596584
