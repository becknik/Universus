---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: false
aliases: P
linter-yaml-title-alias: P
date: 2022-07-09
mod-date: 2022-10-02
---

# P

## Definition:
- Für jedes beliebige Polynom $p$ ist $$\text{P}:= \bigcup_{\text{Polynom }p} \text{DTIME}(p)$$
- Alternativ: $\text{P}=\{A\mid\exists$ Polynom $p$ und eine [[../../../Theo I/Turingmaschinen|TM]] $M$ mit $T(M)=A\wedge time_M(x)\leq p(|x|)\}$
- $\text{P}$ st *unabhängig* von dem *verwendeten Algorithmen-Modell* (=$\text{P}$ ist *robust*), allerdings relativ zur [[Zeitkomplexität|Zeitkomplexität]]

## Eigenschaften: #fc
- $\text{P}\subseteq$ [[../../Berechenbarkeit/LOOP-berechenbar|LOOP-berechenbar]]
- $\forall A\in\text{P}~\exists$ effizienter Algorithmus
- $\text{P}\subseteq$ [[NP]]$~\cap~co\text{NP}$ (-> *P-NP-Problem*: $\text{NP}\subseteq\text{P}?$)
- Folgerung aus dem [[../Platzklassen/Translationssatz für Platzklassen|Translationssatz für Platz-]] und [[Translationssatz für Zeitklassen|Zeitklassen]]: $\text{DSPACE}(n)\neq\text{P}$
- Alle Probleme in $\text{P}$ sind $\text{P}$-vollständig
> Skizze aus der Vorlesung einfügen
^1660503092481

## Kostenmaße: #fc
- Die Kosten sollen *fair* angesetzt werden:
- *Uniformes Kostenmaß*: Dei Zeitkomplexität von Operationen werden uniform mit dem Kostenmaß 1 angegeben
	-> Gängig bei Programmen wie beispielsweise in [[../../Berechenbarkeit/Modelle/WHILE|WHILE]], also wenn sich die verwendeten *Operationen nicht gravierend unterscheiden* und der *Wertebereich eingeschränkt* ist
- *Logarithmisches Kostenmaß*: Abgeleitet von der Anzahl der Übertragenen Bits in Binärdarstellung
	-> Für Große Zahlenwerte und gravierende Unterschiede zwischen Operanden
^1662809091425

## Beispiele Für P-Vollständigkeit: #fc
-> Alle Probleme in $\text{P}$ sind $\text{P}$-vollständig
- [[../Probleme/3KNF-SAT|2KNF-SAT]] $\in\text{P}$
- *PRIMES*: Das (binär-kodierte) Primzahl-Problem $\in\text{P}$
	-> Lösbar durch den AKS-Test
- [[../Probleme/Grapherreichbarkeitsproblem|GAP]] $\in\text{P}$
- Das *Entscheidungsproblem für Leerheit kontextfreier Sprachen* ist für $\text{P}$ $\leq_{\log}$-vollständig
	-> $L_{\text{cfe}}=\{w\mid w$ ist eine Kodierung einer Typ-2 Grammatik $G$ mit $L(G)=\emptyset\}$
- [[../Probleme/Circuit Value Problem|Circuit Value Problem]] und MCP sind $\leq_{\log}-$vollständig für $\text{P}$
- Das Wortproblem für [[CSL]] Sprachen ist $\text{P}$-vollständig[^1]
- Horn-SAT ist $\text{P}$-vollständig
- Die LZW (LZ78) Kompression ist $\text{P}$-vollständig
^1660942356498

[^1]:[Wikipedia:P-Vollständigkeit](https://en.wikipedia.org/wiki/P-complete#P-complete_problems) (19.08.2022)
