---
tags: uni dsa practical-cs algorithm algorithm sort
cards-deck: Uni::Courses::DSA
completed: true
aliases: BubbleSort
linter-yaml-title-alias: BubbleSort
date-of-creation: 2022-07-21
mod-date: 2022-09-11
---

# BubbleSort
![](https://corte.si/posts/code/visualisingsorting/bubble.png)

## Funktionsweise: #fc
- Die Sortierung kommt durch das wiederholte Aufsteigen vom größten Elementen der betrachteten Teilfolge bis zum Ende zustande
	→ Das größere Element wird dabei jeweils von einem *kleineren Element angestoßen*, welches dann *iterativ* immer weiter Richtung Ende der Folge getauscht wird
- Metapher: *Aufsteigende kleinere Blasen*, die größeren anstoßen und dabei selber im Array "stecken bleiben" und somit von den Größeren überholt werden
^1650720178867

## Algorithmus: #fc
```
Method: BubbleSort (F)
for i := 0 to n − 2 do
	if F[i ] > F [i + 1] then
		Vertausche Werte von F [i ] und F [i + 1]
until keine Vertauschung mehr aufgetreten
```
^1659134302257
