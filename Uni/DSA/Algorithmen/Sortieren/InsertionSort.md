---
tags: uni dsa practical-cs algorithm sort
cards-deck: Uni::Courses::DSA
complete: true
aliases: InsertionSort
linter-yaml-title-alias: InsertionSort
date: 2022-07-21
mod-date: 2022-09-07
---

# InsertionSort
![](https://corte.si/posts/code/visualisingsorting/listinsertion.png)

## Funktionsweise:
- Sortierung durch Einfügen von kleineren Elementen in den Folgen-Präfix

## Eigenschaften:
- Das momentan betrachtete Element ist immer zwischengespeichert
- Ist ein stabiles in-Situ Verfahren
- Menschen sortieren Spielkarten auf der Hand nach dem Prinzip von Insertion Sort[^1]

## Algorithmus: #fc
```
Method: InsertionSort (Folge F)
for i := 1..n−1 do
	current_element := F[i];
	current_index := i;
	inner_loop:
	while current_index > 0 do
		if current_element < F[current_index − 1] then
			F[current_index] := F[current_index − 1];
			current_index--;
		else
			break inner_loop
		fi
	od;
	F[current_index] := current_element
od;
```
^1650721188974
[^1]:[Wikipedia: Insertion Sort](https://en.wikipedia.org/wiki/Insertion_sort)
