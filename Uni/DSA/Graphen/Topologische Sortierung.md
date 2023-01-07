---
tags: uni dsa practical-cs graph sort
cards-deck: Uni::Courses::DSA
completed: true
aliases: Topologische Sortierung
linter-yaml-title-alias: Topologische Sortierung
date-of-creation: 2022-07-25
mod-date: 2022-09-10
---

# Topologische Sortierung

## Prinzip: #fc
- Die Reihenfolge der Knoten eines [[Gerichteter Azyklischer Graph|gerichteter azyklischen Graphen]], so dass jeder Knoten nach seinem Vorgängern kommt und es keine Zyklen gibt
- Die Folge wird zum Beispiel durch die [[Algorithmen/Tiefensuche|DFS]] ermittelt
	→ Im Grunde genommen werden die Knoten beim Setzten des Schwarz-Wertes in eine Liste eingefügt
- Entspricht einer Sortierung nach paarweisen Beziehungen, nicht nach totaler Ordnung
^1653939412571
