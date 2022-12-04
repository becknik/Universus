---
tags: uni practical-cs syskon parallel correctness
cards-deck: Uni::Courses::SysKon
complete: false
aliases:
  - Model-Checking
  - PlusCal
linter-yaml-title-alias: Model-Checking
date: 2022-12-03
mod-date: 2022-12-05
---

# Model-Checking

## Prinzip: #fc
- Erstelle ein Modell des Algorithmus
- Definiere die [[../Korrektheitskriterien|Korrektheitskriterien]]
- Lasse den Rechner automatisch überprüfen, ob die Eigenschaften erfüllt sind
	-> Model-Checker kann durch Aufzählung der Zustände Gegenbeispiele liefern
	-> Checker kann auch nie unendlich lange rechnen
^1670089450391

## Funktionsweise:
- Atomare Befehle ohne *globale Seiteneffekte* lassen sich zusammenfassen
	-> Entweder atomares Lesen oder Schreiben

## Achtung:
- Variablen sollten nach oben beschränkt werden, sonst Laufzeit (?)

## PlusCal

### Notation:
- $\square P:$ $P$ gilt immer
- $\square\textasciitilde P:$ $P$ gilt niemals
- $\diamond P:$ $P$ ?
