---
tags: uni theo-2 theoretical-cs complexity
cards-deck: Uni::Courses::Theo-II
completed: false
aliases: P
linter-yaml-title-alias: P
date-of-creation: 2022-07-09
mod-date: 2022-10-24
---

# P
> Skizze aus der Vorlesung einfügen

## Definition:
- Für jedes beliebige Polynom $p$ ist $\text{P}$ definiert als $$\text{P}:= \bigcup_{\text{Polynom }p} \text{DTIME}(p)$$
	→ [[TIME|DTIME]]
- *Alternativ*: $\text{P}=\{A\mid\exists$ Polynom $p$ und eine [[../../../Theo I/Turingmaschinen|TM]] $M$ mit $T(M)=A\wedge time_M(x)\leq p(|x|)\}$
- $\text{P}$ st *unabhängig* von dem *verwendeten [[../../Berechnungsmodelle|Algorithmen-Modell]]*, allerdings relativ zur [[Zeitkomplexität|Zeitkomplexität]]
	→ $\text{P}$ ist *robust*

## Eigenschaften: #fc
- $\text{P}\subseteq$ [[NP]]$~\cap~co\text{NP}$
	→ [[P-NP-Problem]]
- $\forall A\in\text{P}:$ Es existiert ein effizienter Algorithmus für $A$
- $\text{P}\subseteq$ [[../../Berechenbarkeit/LOOP-berechenbar|LOOP-berechenbar]]
- Alle Probleme in $\text{P}$ sind $\text{P}$-vollständig
- *Kollar* aus den [[../Translationssätze|Translationssätzen]]: $\text{DSPACE}(n)\neq\text{P}$
^1660503092481

## Kostenmaße: #fc
- Die Kosten sollen generell *fair* angesetzt werden:
	- *Uniformes Kostenmaß*: Dei Zeitkomplexität von Operationen werden uniform mit dem Kostenmaß 1 angegeben
		→ Gängig, wenn sich die verwendeten Operationen *nicht gravierend unterscheiden* und der *Wertebereich eingeschränkt* ist
		→ z.B. bei [[../../Berechenbarkeit/Modelle/WHILE|WHILE]]
	- *Logarithmisches Kostenmaß*: Abgeleitet von der Anzahl der Übertragenen Bits in Binärdarstellung
		→ Für *große Zahlenwerte* und *gravierende Unterschiede* zwischen Operanden
^1662809091425

## Beispiele

### Inklusion in $\text{P}\Rightarrow\text{P}$-Vollständigkeit: #fc
- [[../Probleme/3KNF-SAT|2KNF-SAT]]
- [[../Probleme/Grapherreichbarkeitsproblem|GAP]]
- *PRIMES*: Das binär-kodierte Primzahl-Problem
	→ Lösbar durch den *AKS-Test*
- Entscheidungsproblem: für *Leerheit [[../../../Theo I/Typ-2|kontextfreier Sprache]]* ist [[../Logspace-Reduktion|Logspsce-vollständig]] für $\text{P}$
	→ $L_{\text{CFE}}=\{w\mid w$ ist eine Kodierung einer Typ-2 Grammatik $G$ mit $L(G)=\emptyset\}$
- [[../Probleme/Circuit Value Problem|(modifizierte) Circuit Value Problem]] ist $\leq_{\log}-$vollständig für $\text{P}$
- Das [[../../../Theo I/Wortproblem|Wortproblem]] für [[CSL]] Sprachen ist $\text{P}$-vollständig[^1]
- Horn-SAT ist $\text{P}$-vollständig
- Die *LZW/ LZ78* Kompression ist $\text{P}$-vollständig
	→ *Gegeben*: Strings $t,s$; Wird $s$ durch Anwendung von LZ78 zu $t$?
^1660942356498

[^1]:[Wikipedia:P-Vollständigkeit](https://en.wikipedia.org/wiki/P-complete#P-complete_problems) (19.08.2022)
