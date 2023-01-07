---
tags: uni dsa practical-cs hash trait
cards-deck: Uni::Courses::DSA
completed: true
aliases: Offenes Hashing
linter-yaml-title-alias: Offenes Hashing
date-of-creation: 2022-07-26
mod-date: 2022-09-06
---

# Offenes Hashing
→ [[../Hashfunktionen|Hashfunktionen]]

## Eigenschaften: #fc
 - *Chaining*: Bei einer *Kollision* werden die Werte in der Tabelle *hintereinander gehängt*
	 → Laufzeitkomplexität kann im Extremfall ohne den Einsatz von [[../Bäume/Suchbaum|Suchbäumen]] $\in O(n)$ liegen
- Für den maximalen Auslastungsgrad $\lambda$ sollte gelten: $\lambda = \frac{k}{p}\leq 0.8$, wobei $k$ der Anzahl der gespeicherten Elemente entspricht
	→ Falls $0.8$ überschritten und kein *Rehashing* durchgeführt wird, kommt es aufgrund von vermehrten Kollisionen zu einer dramatischen Verschlechterung der Laufzeit
	→ $\lambda>1$ ist bei einer durchschnittlichen Listenlänge von $\lambda$ möglich
^1658939286256
