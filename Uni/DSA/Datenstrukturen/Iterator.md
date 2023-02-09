---
tags: uni dsa practical-cs struct
cards-deck: Uni::Courses::DSA
completed: true
aliases: Iterator
linter-yaml-title-alias: Iterator
date-of-creation: 2022-07-21
mod-date: 2022-09-10
---

# Iterator

## Eigenschaften
- Ähnelt einem Cursor, der eine Datenstruktur durchwandert
→ Ähnelt dem Kopf einer [[../../Theo I/Turingmaschinen|Turingmaschine]]

## Spezifikation #fc
- `next()`
	→ *CPP*: *Gibt das aktuelle Element* zurück und setzt den Zeiger daraufhin auf das nächste Element
	→ [[../../../Informatik/Softwareentwicklung/ProgLangs/Java|Java]]: Verrückt die Referenz vom Head-Node aus startend auf das nächste Element und *gibt dann* dessen *Wert zurück*
- `begin()`/ `end()`
- `hasNext()`
- `remove()`
- *Erweiterte Spezifikation*:
	- *Wahlfreier Zugriff* über Indizes
	- *Manipulation* durch Einfügen und Löschen von Elementen
	- *Bidirektionale Iteration*
^1649785309471
