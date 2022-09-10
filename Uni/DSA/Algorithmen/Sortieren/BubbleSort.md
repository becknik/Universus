---
tags: uni dsa practical-cs algorithm algorithm sort
cards-deck: Uni::Courses::DSA
complete: true
aliases: BubbleSort
linter-yaml-title-alias: BubbleSort
date: 2022-07-21
mod-date: 2022-09-02
---

# BubbleSort
![](https://corte.si/posts/code/visualisingsorting/bubble.png)

## Funktionsweise: #fc
- Sortieren durch Aufsteigen vom durchgetauschten, größten Element bis zum (gekürzten) Ende der Folge
	-> Metapher: Aufsteigende Blasen unterschiedlicher Größe, wobei kleinere Blasen die größeren anstoßen (und selbst stehen bleiben)
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
