---
tags: uni dsa practical-cs algorithm sort
cards-deck: Uni::Courses::DSA
complete: true
aliases: SelectionSort
linter-yaml-title-alias: SelectionSort
date: 2022-07-21
mod-date: 2022-09-02
---

# SelectionSort
![](https://corte.si/posts/code/visualisingsorting/selection.png)

## Funktionsweise:
- Sortieren erfolgt durch Auswahl des größten Elements in der Folge
- Das größte Element wird an den Index der oberen Schranke getauscht, dann wird die Schranke um Eins verringert

## Eigenschaften:
- Der Algorithmus benötigt immer $n$ Vertauschungen

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
