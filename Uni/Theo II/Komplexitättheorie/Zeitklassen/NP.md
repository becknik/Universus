---
tags: uni theo-2 theoretical-cs abstraction complexity 
cards-deck: Uni::Courses::Theo-II
complete: true
aliases: NP
date: 2022-07-09
mod-date: 2022-08-20
linter-yaml-title-alias: NP
---

# NP
-> [[NP/NP-Härte|NP-Härte]], [[NP/NP-Vollständigkeit|NP-Vollständigkeit]]

## Definition: #fc
- Angenommen, die Eingabe $x$ wird von einer [[../../../Theo I/Turingmaschinen|TM]] $M$ auf *mindestens einem Weg akzeptiert*, dann gibt $mtime_M(x)$ die *minimale Länge* aller akzeptierenden Pfade an
	-> Falls $M$ $x$ nicht akzeptiert: $ntime_M(x) = 0$
- Für jedes beliebige Polynom $p$ ist
$$\displaylines{NP = \bigcup_{\text{Polynom }p} NTIME(p)\\ = \{A \mid\exists p,~\exists M \in NTM, ~T(M)=A \wedge \forall x: ntime_M(x) \leq p(|x|)\}}$$
-> [[../../../Theo I/Turingmaschinen|Nichtdeterministische Turingmaschine]]
^1660503052355

## Eigenschaften: #fc
- [[P|P]] $\subseteq NP$
	-> P-NP-Problem: $NP \subseteq P?$
	-> $NP=coNP$ könnte möglich sein
- Sei $L \in NP$ beliebig, dann können wir nur schließen, dass $L \in EXPTIME$ liegt
	-> Laut [[NP/Satz von Cook]] lässt sich für ein $NP$-Problem eine Formale $F$ erstellen, die dann in der Zeit $2^{c\cdot n}$ (für ein geeignetes $c$) entschieden werden kann, nur dass $n$ polynomiell groß ist.
- [[NP/Guess and Check|Guess And Check]]
- Die Klasse enthält enorm viele für die Praxis wichtige Probleme (z.B.)
	-> Meistens haben sie eine exponentielle, seltenst eine sub-exponentielle ($\mathcal{O}(2^\sqrt{n}n)$) Laufzeit, oder können erst gar nicht gelöst werden
^1660503052362

## Beispiele Für NP-Vollständigkeit: #fc
-> Alle bekannten NPC Probleme sind auch unter [[../Logspace-Reduktion|Logspace-Reduktionen]] vollständig
- [[../Probleme/Satisfiability|SAT]]
- [[../Probleme/3KNF-SAT|3KNF-SAT]] ($\text{SAT}\leq_p\text{3KNF-SAT}$)
- [[../Probleme/CLIQUE|CLIQUE]] ($\text{SAT}\leq_p\text{CLIQUE}$)
- [[../Probleme/FÄRBBARKEIT|FÄRBBARKEIT]]
- [[../Probleme/Traveling Salesman Problem|TSP]]
- [[../Probleme/Vertex Cover|Vertex Cover]]
- Aus *Datenstrukturen & Algorithmen*: [[../../../DSA/Graphen/Wege & Kreise|Hamilton Kreis]], [[../../../DSA/Probleme/Rucksackproblem|Rucksackproblem]]
- Aus *Schöning's Buch*: $\text{3-KNF-SAT}\leq_p\text{MENGENÜBERDECKUNG},\text{KNOTENÜBERDECKUNG},\text{PARTITION},\text{BIN PACKING}$
^1660944596584
