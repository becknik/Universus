---
tags: uni dsa practical-cs algorithm sort
cards-deck: Uni::Courses::DSA
completed: true
aliases: InsertionSort
linter-yaml-title-alias: InsertionSort
date-of-creation: 2022-07-21
mod-date: 2022-09-11
---

# InsertionSort
![](https://corte.si/posts/code/visualisingsorting/listinsertion.png)

## Funktionsweise:
- Sortierung durch Einfügen von kleineren Elementen in den Präfix der Folgen
	→ "Sortieren durch Einfügen"

## Eigenschaften:
- Das momentan betrachtete Element ist immer zwischengespeichert
- Die Anzahl der Vertauschungen beträgt im Mittel $\approx\frac{n^2}{8}$[^1]
- Ist ein stabiles [[../../Sortierverfahren|in-situ]] Verfahren
- Menschen sortieren Spielkarten auf der Hand nach dem Prinzip von Insertion Sort[^2]

## Algorithmus: #fc
```
Method: InsertionSort (Folge F)
for i := 1 to n−1 do
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
[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021. S.151
[^2]:[Wikipedia: Insertion Sort](https://en.wikipedia.org/wiki/Insertion_sort)
