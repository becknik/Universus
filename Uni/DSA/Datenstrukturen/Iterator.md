---
tags: uni dsa practical-cs struct
cards-deck: Uni::Courses::DSA
status: unfinished
aliases: Iterator
linter-yaml-title-alias: Iterator
date: 2022-07-21
mod-date: 2022-09-08
---

# Iterator

## Eigenschaften:
- Ähnelt einem Cursor, der eine Datenstruktur durchwandert
-> Ähnelt dem Kopf einer [[../../Theo II/Turingmaschine|Turingmaschine]]

## Spezifikation: #fc
- `next()`
	-> *CPP*: *Gibt das aktuelle Element* zurück und setzt den Zeiger daraufhin auf das nächste Element
	-> [[../../../Privat/Programmiersprachen/Java|Java]]: Verrückt die Referenz vom Head-Node aus startend auf das nächste Element und *gibt dann* dessen *Wert zurück*
- `begin()`/ `end()`
- `hasNext()`
- `remove()`
- *Erweiterte Spezifikation*:
	- Wahlfreier Zugriff über Indizes
	- Manipulation durch Einfügen und Löschen von Elementen
	- Bidirektionale Iteration
^1649785309471
