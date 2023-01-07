---
tags: uni practical-cs syskon parallel correctness
cards-deck: Uni::Courses::SysKon
completed: false
aliases:
  - Model-Checking
  - PlusCal
linter-yaml-title-alias: Model-Checking
date-of-creation: 2022-12-03
mod-date: 2023-01-04
---

# Model-Checking

## Prinzip #fc
- Ein Modell des Programms muss erstellt werden, das die [[../Atomizität|Atomizität]] so genau wie möglich beschreiben soll
- [[../Korrektheitskriterien|Korrektheitskriterien]] müssen formuliert sein
- Der Rechner überprüft mit Hilfe des Modell-Checkers automatisch, ob die Eigenschaften erfüllt sind
	→ Der Model-Checker versucht durch das Aufzählen aller möglichen Zustände Gegenbeispiele zu liefern (was u.U. unendlich lange dauern kann)
	→ Wenn der Modell-Checker terminiert, sind die Eigenschaften erfüllt
^1673097622837

## Leslie Lamports Tools
- Tempral Logic of Actions *TLA+*: Modelliersprach für nebenläufige Systeme & zur Definition der Korrektheitseigenschaften
- PlusCal: Meta-Sprache (="Syntactic Sugar") zur Beschreibung von Algorithmen
	→ Wird nach TLA+ übersetzt
- TLC: Model-Checker

## Umsetzung
- Atomare Befehle ohne *globale Seiteneffekte* lassen sich zusammenfassen
	→ Entweder atomares Lesen oder Schreiben
- Variablen sollten nach oben beschränkt werden, sonst Laufzeit (?)
