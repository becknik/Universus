---
tags: uni dsa practical-cs graph algorithm
cards-deck: Uni::Courses::DSA
completed: false
aliases: Dijkstra
linter-yaml-title-alias: Dijkstra
date-of-creation: 2022-07-23
mod-date: 2022-09-10
---

# Dijkstra

## Eigenschaften: #fc
- Berechnet den *kürzesten Weg* von einem Startknoten zu allen erreichbaren Knoten eines [[../Gewichteter Graph|gewichteten Graphen]] ohne*negativen Kantengewichte*
- Wurde 1959 von Edsger W. Dijkstra entworfen
- Verwendet eine [[../../Bäume/Heap|Prioritätswarteschlange]]
	→ Ist eine [[../../Algorithmen/Muster/Greedy|Greedy]] Erweiterung der [[Tiefensuche]]
- Entspricht dem [[A-Stern]] ohne angegebene Heuristik und ist somit eine *uninformierte Suche*
^1658939201003

## Funktionsweise & Algorithmus: #fc
- Ein Startknoten wird bestimmt und in den MinHeap gelegt
- Auf allen Knoten wird die Distanz $d$ initial auf $\infty$ gesetzt, außerdem wer sie weiß gefärbt
1. *Expansion*: Ein weiß markierter Knoten $k$ mit der geringsten Distanz $d$ zum Startknoten wird aus dem Heap entnommen
2. *Distanzupdate*: Für jeden noch nicht besuchten Knoten, der an den entnommenen Knoten angrenzt, wird die Distanz aktualisiert
^1653940126208

## Algorithmus: !!!
```
for (Knoten u: V \ start) do
	D[u]:= ∞
od;
D[start] := 0;
PriorityQueue Q := V;
while !isEmpty(Q) do
	u := extractMinimal(Q);
	for each v ∊ Successor(u) ∩ Q do
		if D[u] + γ((u, v)) < D[v] then
			D[v] := D[u] + γ((u, v));
			adjustiere Q an neuen Wert D[v]
		fi;
	od;
od;
```

## Anwendung:
- Kürzeste Wege bei Flugverbindungen mit km-Angaben/ Kosten oder Straßennetze mit km-Angaben
