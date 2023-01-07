---
tags: uni dsa practical-cs algorithm graph
cards-deck: Uni::Courses::DSA
completed: true
aliases: Kruskal
linter-yaml-title-alias: Kruskal
date-of-creation: 2022-07-24
mod-date: 2022-09-10
---

# Kruskal

## Eigenschaften:
- Ein Algorithmus auf [[../Gewichteter Graph|gewichteten Graphen]], um den [[../Spann- & Wurzelbaum|minimalen Spannbaum]] des Graphen zu bestimmen
- [[../../Algorithmen/Muster/Greedy|Greedy-Algorithmus]]

## Funktionsweise: #fc
- Initialisiere die Menge $A$
- Die Kantenmenge $E$ wird nach dem Gewicht sortiert
- Wiederhole, solange $|A| < |E|-1$
	- Entnehme das erste Element $e$ aus der Knotenmenge
	- Falls durch das hinzufügen von $e$ zu $A$ kein Zyklus in $A$ entsteht: Füge $e$ zu $A$ hinzu
^1655039482650

## Algorithmus: #fc
```
Method: kruskal(G)
sort(E);
Set A:= {};
Set part_graphs := {{v} | ∀v ∊ V}
while |A| < V(G) do
	e := takeFirst(E);
	// FIND(v ∊ V): Gibt die Menge aus part_graphs zurück, in der sich v befindet
	Set M := FIND(e.origNode());
	Set N := FIND(e.destNode());
	if M ≠ N then
		UNION(M,N) // Vereinigt die Mengen M und N in part_graphs
		A := A ∪ {e};
	fi;
od;
```
^1658939128954
