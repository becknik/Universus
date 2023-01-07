---
tags: uni dsa practical-cs algorithm tree algorithm sort
cards-deck: Uni::Courses::DSA
completed: true
aliases: HeapSort
linter-yaml-title-alias: HeapSort
date-of-creation: 2022-07-21
mod-date: 2022-09-05
---

# HeapSort
![](https://corte.si/posts/code/visualisingsorting/heap.png)

## Eigenschaften:
- Nutzt die Eigenschaften eines [[../../Bäume/Heap|Heaps]] auf einem Array
- Liegt in $\mathbfcal{O}(n \log n)$
- Im schlechtesten Fall liegt der Algorithmus in $\Theta(\frac{3n}{2} \log n)$

## Funktionsweise: #fc
1. [[../../Bäume/Heap|Herstellung der partiellen Ordnung]]
2. Wiederhole, so lange Elemente im Heap sind:
```
Vertausche F[0] und F[letztePos];
Versenke F[0] im Heap F[0..letztePos-1];
letztePos := letztePos−1
```
^1652814891205
