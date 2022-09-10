---
tags: uni dsa practical-cs algorithm algorithm sort
cards-deck: Uni::Courses::DSA
complete: true
aliases: BubbleSort
linter-yaml-title-alias: BubbleSort
date: 2022-07-21
mod-date: 2022-09-10
---

# BubbleSort
![](https://corte.si/posts/code/visualisingsorting/bubble.png)

## Funktionsweise: #fc
- Die Sortierung kommt durch das wiederholte Aufsteigen von Elementen bis zum Ende der betrachteten Folge zustande
- Dabei steigt immer das Element bis zum Ende der betrachteten Folge auf, welches das größte in dieser ist
- Um das größte Element zu ermitteln, wird immer das relativ größere für das nach oben durchtauschen ausgewählt
	-> Das kleinere Element wird bei der Erkennung eines größeren Elements liegen gelassen
	-> Metapher: Aufsteigende kleinere Blasen, die größeren anstoßen und dabei im Array stecken bleiben
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
