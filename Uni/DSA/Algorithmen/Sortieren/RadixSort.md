---
tags: practical-cs algorithm sort
sources: Algorithmen und Datenstrukturen
cards-deck: Private::Books::Algorithmen und Datenstrukturen
completed: true
aliases: RadixSort
linter-yaml-title-alias: RadixSort
date-of-creation: 2022-07-23
mod-date: 2022-09-11
---

# RadixSort

## Eigenschaften: #fc
- Ist auch unter dem Namen "*DistributionSort*" bekannt
	→ lat. Radix = Wurzel bezeichnet die Basis Schwellenwertsystems (z.B. 10 für die Basis von $\mathbb{N}$)
- Ist auf einem Alphabet $\Sigma,|\Sigma|<\infty$ definiert
- Das Prinzip entspricht dem *Sortieren von nummerierten Lochkarten*, das bereits 1887 von Hollerith entwickelt wurde
- Es gibt viele Realisierungen ([[../../Sortierverfahren|in-situ]] oder [[../../Sortierverfahren|out-of-place]]) und Optimierungsvarianten für spezielle Datentypen
- Zeitkomplexität Bewegt Sich Zwischen O(n) Und O(n^2)
- Die Vergleiche im Mittel liegen bei Out-of-place Implementierung bei $l\cdot n$

## Funktionsweise: #fc
- *Vom LSB/MSB* her wird in jedem Durchlauf eine Stelle aller Elemente behandelt
- In einem Histogramm wird festgehalten, wie viele Elemente pro Alphabetszeichen vorhanden sind
	→ Eine Partitionierung der Elemente ist grundsätzlich auch möglich, allerdings nur unter Verwaltung zusätzlicher Listen
- Nach der Anzahl der Elemente pro Zeichen im Histogramm wird die neue Position der Schlüssel in der Folge bestimmt
	→ Die Elemente werden dementsprechend angeordnet
