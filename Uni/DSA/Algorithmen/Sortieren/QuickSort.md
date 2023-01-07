---
tags: uni dsa practical-cs algorithm sort
cards-deck: Uni::Courses::DSA
completed: true
aliases: QuickSort
linter-yaml-title-alias: QuickSort
date-of-creation: 2022-07-21
mod-date: 2022-09-07
---

# QuickSort
![](https://corte.si/posts/code/visualisingsorting/quick.png)

## Funktionsweise:
- Sortieren rekursiv mit Pivot-Elementen

## Eigenschaften:
- Jedes gewählte Pivot ist nach dem *Zerlege*-Teil an dem Index, an dem es auch in der sortierten Folge liegen würde
- QuickSort basiert auf [[../Muster/Divide And Conquer|Divide & Conquer]]
- Der Algorithmus ist *in-Situ*, *instabil* und funktioniert *rekursiv*
- *Worst Case*: Das Maximale Element wird immer als Pivot gewählt[^1]
> Eigentlich würde dann zu 0 Vertauschungen pro Durchlauf kommen, da jedes Element im Zerlege Teil mit sich selbst vertauscht wird - was die Laufzeitkomplexität gar nicht so viel beeinflussen sollte, wie wenn ein paar Vertauschungen stattfinden sollte

## Algorithmus: #fc
```
Method: QuickSort(F, u, o)((()))
Falls u < o:
	pivot_index := Abgerundeter mittler Index der Folge F
	pivot_index_new := Zerlege(F, u, o, p);
	// Die neue Position von p in der nun "semi-sortierten" Folge
	Qucksort(F, u, pivot_index_new - 1);
	Qucksort(F, pivot_index_new + 1, o);
```
```
Method: Zerlege(F, u, o, p) → pivot_index_new
pivot_index_new := u  // Auch pn genannt
// Wenn u zufällig das kleinste Element im F ist, bleibt pn = u
pivot_element := F[p]
Tausche F[p] mit F[o]
FOR (int i = u; i < o; i++):
	Falls F[i] < pivot_element
		Tausche F[i] mit F[pivot_index_new] 
		pivot_index_new++
// Vor pn befinden sich nur noch Werte < pivot_element
Tausche F[o] mit F[pn]  // Pivot bekommt seinen rechmäßigen Platz
return pivot_index_new
```
^1654704450375
[^1]:[Geeks For Geeks](https://www.geeksforgeeks.org/when-does-the-worst-case-of-quicksort-occur/)
