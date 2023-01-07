---
tags: uni dsa practical-cs graph abstraction
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Graphen
  - doppelpunktfrei
  - Teilgraph
  - Entry Point
  - Grad
  - Zyklus
  - Pfad
linter-yaml-title-alias: Graphen
date-of-creation: 2022-07-23
mod-date: 2022-09-10
---

# Graphen
→ [[Algorithmen auf Graphen|Algorithmen auf Graphen]]
→ [[Datenstrukturen für Graphen|Datenstrukturen für Graphen]]

## Varianten:
- [[Graphen/Ungerichtete Graphen|Ungerichteter Graph]]
- [[Graphen/Gerichtete Graphen|Gerichteter Graph]]
- [[Graphen/Gewichteter Graph|Gewichteter Graph]]
- [[Graphen/Gerichteter Azyklischer Graph|Gerichteter Azyklischer Graph]]
- [[Graphen/Multigraph|Multigraph]]
- [[Graphen/Hypergraph|Hypergraph]]
- [[Graphen/Planarer Graph|Planarer Graph]]
- [[Graphen/Bipartite Graphen|Bipartiter Graph]]

## Fachbegriffe: #fc
- *Doppelpunktfrei*: Für einen Pfad $v_0, v_1, \dots, v_n$ gilt $\forall i,j \in \mathbb{N}, 0 \leq i,j \leq n, i \neq j: v_i \neq v_j$
	→ Kein Knoten kommt doppelt im Pfad vor
- [[Graphen/Zusammenhangskomponenten|Zusammenhangskomponenten]]
- *Teilgraph*: Ein Teilgraph $G_{sub}$ eines Graphen $G$ enthält eine Teilmenge der Knoten $V_{sub}$ und Kanten $E_{sub}$
	→ $G_{sub}$ muss ein gültiger Graph sein und $E_{sub}= \bigcup_{e \in E} e=(v_o, v_d): v_o, v_d \in V_{sub}$
- *Entry Point*: Erlauben den Zugriff auf alle Knoten im Graphen durch direkte oder indirekte Erreichbarkeit
^1653920241755

### (Ausgangs-/Eingangs-)Grad: #fc
→ Wird auch *Valenz* genannt
- *Quelle*: Ein Knoten mit dem Eingangsgrad 0
- *Senke*: Ein Knoten mit dem Ausgangsgrad 0
^1653920279100

### Pfad: #fc
- $(v_1,v_2,\dots,v_r)$ mit $r \geq 1 \wedge \forall i \in \{1,2,\dots,r-1\}: v_i,v_{i+1} \in E$
	→ $v_r$ ist von $v_1$ aus *erreichbar* und die beiden Knoten sind *verbunden*
	→ Wäre $v_1 = v_r$, wäre der Pfad *geschlossen*
^1653670020191

### Zyklus: #fc
- Ein geschlossener Pfad $v_i,\dots,v_n,v_i$, mit $\forall i\leq n-1:(v_i,v_{i+1})\in E\wedge(v_n,v_1)\in E,$ der *doppelpunktfrei* ist
	→ *Trivialzyklen* (=Zyklen mit weniger als 3 Knoten) sind ausgeschlossen
^1654943217549

## Berechnung des Weges:
$$w(P)=\sum^{n-1}_{i=1}\gamma((v_ i,v_{i+1}))$$

## Vergleich zu [[Bäume|Bäumen]]: #fc
- Bei Bäumen steht oft die [[Suchverfahren|Suche]] im Vordergrund, bei Graphen eher die Traversierung
- Da es *keinen Wurzelknoten* gibt, muss der Startknoten bei Graphen ausgewählt werden
- Die *ausgehenden Kanten* werden anstelle von Kindknoten betrachtet
- Bereits besuchte Knoten müssen bei Graphen *markiert* werden, da sie zyklisch sein können
^1653919973449
