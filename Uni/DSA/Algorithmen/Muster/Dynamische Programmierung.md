---
tags: uni dsa practical-cs design-pattern
cards-deck: Uni::Courses::DSA
completed: true
aliases: Dynamische Programmierung
linter-yaml-title-alias: Dynamische Programmierung
date-of-creation: 2022-07-26
mod-date: 2022-09-08
---

# Dynamische Programmierung

## Prinzip: #fc
- Eine optimale Lösung für die kleineren Teilprobleme soll gefunden werden (Greedy), die zur Lösung größerer Teilprobleme und später *des Gesamtproblems* beitragen
	→ Ist nicht immer möglich
	→ Bei vielen disjunkten Teillösungen bringen die Gewinne nichts
	→ Die enstehende Tabelle kann sehr groß werden
- Die Lösung wird wiederum zur Lösung des nächstgrößeren Teilproblems verwendet
	→ Neuberechnung durch Rekursion (D&C, Backtracking) wird durch Zwischenspeicherung in einer Tabelle vermieden, wodurch Zeit gespart wird
^1658939018078

## Unterschiede zu anderen Mustern: #fc
→ Dynamische Programmierung = Greedy $\cup$ Rekursion (D&C) & Konfigurationsbaum (Backtracking)
- [[Divide And Conquer|D&C]]: Die Rekursion wird durch eine Iteration über abgespeicherte Teilergebnisse ersetzt
- D&C löst unabhängige Teilprobleme, die dynamische Programmierung hingegen Abhängige
 - [[Backtracking]]: Der Konfigurationsbaum wird "Bottom-Up" aufgebaut
- Viele [[Greedy]] sind eher auf das lokale Optimum aus
	→ Falls bei dynamischen Algorithmen ein komplettes Absuchen stattfindet: Das globale Optimum wird gefunden
^1658939018087

## Eigenschaften: #fc
- Vom Mathematiker *Richard Bellman* eingeführt
- Kann am besten auf Optimierungsprobleme angewandt werden, deren Lösung aus der Lösung von vielen gleichartigen Teilproblemen besteht
^1658939018090

## Anwendung:
- [[Levenshtein-Distanz|Levenshtein-Distanz]]
- [[CYK-Algorithmus]]
- Die garantiert optimale Lösung des [[../../Probleme/Rucksackproblem|Rucksackproblems]]

## Quelle:
- [Wikipedia](https://de.wikipedia.org/wiki/Dynamische_Programmierung) (26.07.2022)
