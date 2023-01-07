---
tags: uni dsa practical-cs design-pattern
cards-deck: Uni::Courses::DSA
completed: true
aliases: Backtracking
linter-yaml-title-alias: Backtracking
date-of-creation: 2022-07-19
mod-date: 2022-09-13
---

# Backtracking

## Prinzip: #fc
- Alle infrage kommenden Lösungswege werden *systematisch abgesucht*, getestet und so zu einer Gesamtlösung ausgebaut
	→ "*Trail & Error*"
	→ Falls eine Lösung existiert, wird sie gefunden
- Falls ein Weg nicht zu einer Lösung führt, werden die letzten Schritte zurückgenommen und der nächste Weg ausprobiert
	→ Führt schrittweise zu einer global optimalen Gesamtlösung
```
Methode BACKTRACK (K: konfiguration)
…
if [K ist Lösung] then
	[gib K aus]
else
	for each [jede direkte Erweiterung K’ von K] do
		BACKTRACK(K’)
	od
fi
```
^1658308549431

## Voraussetzungen: #fc
- Sei $KF$ die Menge aller Konfigurationen $K$
- Sei $K_0$ die Anfangskonfiguration
- $\forall K_i \exists \text{ direkte Erweiterungen } K_{i,1},\dots,K_{i,n_i}$, für die jeweils [[../../../Theo II/Entscheidbarkeit|entscheidbar]] sind, ob sie eine Lösung ist
^1658308549442

## Optimierungen: #fc
Backtracking-Algorithmen werden meistens *rekursiv* implementiert
	→ Weisen meistens eine *exponentielle* Laufzeit auf
- Abbruch nach der ersten gefundenen Lösung (wie bei der [[../../Graphen/Algorithmen/Tiefensuche|Tiefensuche]])
- Vorgabe einer maximalen *Rukursionstiefe*
	→ Zum Beispiel die Stellungen der Spielfiguren auf dem Schachbrett bei einem Schachprogrammen
- *Branch-and-Bound*: Nur Zweige werden verfolgt, die eine Lösung versprechen oder die am besten bewertet sind
	→ Eine typische Variante für [[../../../Theo II/Problemklassen|Optimierungsfragen]]
→ Latentes Problem: Mehrfaches Berechnen von gleicher Teilbäume → [[Dynamische Programmierung|Dynamische Programmierung]]
^1658939009980

## Anwendung: #fc
- [[../../Graphen/Algorithmen/Tiefensuche|Tiefensuche]]
- Spielprogramme wie Schach oder Dame (z.B. [8-Damen-Problem](https://de.wikipedia.org/wiki/Damenproblem))
- [[../../../Theo II/Logik/Belegung|Erfüllbarkeit]] von logischen Aussagen [[../../../Theo II/Komplexitättheorie/Probleme/Satisfiability|SAT]]
- Planungs- und [[../../../Theo II/Problemklassen|Optimierungsprobleme]]:
	- Routenplanung
	- Verteilungsprobleme mit Nebenbedingungen (z.B. [[../../Probleme/Rucksackproblem|Rucksackproblem]])
	- Färben von Landkarten (oder [[../../../Theo II/Komplexitättheorie/Probleme/FÄRBBARKEIT|FÄRBBARKEIT]])
^1658939009985
