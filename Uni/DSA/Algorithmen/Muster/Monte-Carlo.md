---
tags: uni dsa practical-cs design-pattern
cards-deck: Uni::Courses::DSA
completed: true
aliases: Monte-Carlo
linter-yaml-title-alias: Monte-Carlo
date-of-creation: 2022-07-27
mod-date: 2022-09-05
---

# Monte-Carlo

## Prinzip: #fc
- Steht für *Mostly Correct*
- Berechnet mit der Wahrscheinlichkeit $p < 1$ das korrekte Ergebnis
	→ Die Korrektheit hängt von einer *Zufallskomponente* ab
- Macht sich eine randomisierte Abtastung zur Berechnung *numerischer Resultate* zunutzen
	→ "*Gesetz der großen Zahlen*": Konvergenz der relativen Häufigkeit zu Erwartungswert (?)
- Ist auf jeden Fall *effizient*
- Kann bei Entscheidungsproblemen zweiseitige Fehler aufweisen
^1658939028908

## Anwendung:
- [[../Miller-Rabin-Test|Miller-Rabin Primzahltest]]
- Numerische Integration: Liegt ein zufälliger Punkt im Quadrat $(-1,-1),(1,1)$?
