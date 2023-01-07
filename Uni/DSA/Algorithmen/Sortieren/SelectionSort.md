---
tags: uni dsa practical-cs algorithm sort
cards-deck: Uni::Courses::DSA
completed: true
aliases: SelectionSort
linter-yaml-title-alias: SelectionSort
date-of-creation: 2022-07-21
mod-date: 2022-09-11
---

# SelectionSort
![](https://corte.si/posts/code/visualisingsorting/selection.png)

## Funktionsweise:
- Sortieren erfolgt durch Auswahl des größten Elements in der Folge
	→ "Sortieren durch Selektion"
- Das größte Element wird an den Index der oberen Schranke getauscht, dann wird die Schranke um Eins verringert

## Eigenschaften:
- Der Algorithmus benötigt unabhängig von der der Art der Eingabefolge immer $n$ *Vergleiche*
- Im Mittel sind unter $n$ *Vertauschungen* notwendig, im schlechtesten Fall $\in\mathbfcal{O}(n^2)$[^1]

## Algorithmus: #fc
```
Methode: SelectionSort (F)
p := n − 1;
while p > 0 do
	g := Index des größten Elementes aus F im Bereich 0 … p;
	Vertausche Werte von F[p] und F[g];
	p := p − 1
```
^1658939319552
[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021.
