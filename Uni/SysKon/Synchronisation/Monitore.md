---
tags: uni practical-cs syskon parallel sync
cards-deck: Uni::Courses::SysKon
complete: true
aliases: Monitore
linter-yaml-title-alias: Monitore
date: 2022-12-03
mod-date: 2022-12-04
---

# Monitore

## Funktionsweise: #fc
- Die Manipulation der (gemeinsamen) Daten (und somit des Zustands) des Monitor-Objekts ist *ausschließlich* über Methodenaufrufe möglich
- Nur ein Thread kann zu einem Zeitpunkt eine Methode des Monitor-Objekts ausführen
	-> Weitere Threads werden [[../Korrektheitskriterien|fair]] in einer [[../../DSA/Datenstrukturen/Queue|Queue]] blockiert
^1670108796413
