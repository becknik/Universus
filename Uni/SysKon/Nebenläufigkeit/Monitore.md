---
tags: uni practical-cs syskon parallel sync
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Monitore
linter-yaml-title-alias: Monitore
date-of-creation: 2022-12-03
mod-date: 2023-01-04
---

# Monitore

## Funktionsweise #fc
- Manipulation der gemeinsamen Daten (=des Zustands) des *Monitor-Objekts* *ausschließlich* über Methodenaufrufe
	→ [[OOP]]-Ansatz
	→ Nur ein Thread kann zu einem Zeitpunkt eine Methode des Monitor-Objekts aufrufen
- Weitere Threads werden [[../Korrektheitskriterien|fair]] in einer [[../../DSA/Datenstrukturen/Queue|Queue]] blockiert
^1670108796413
