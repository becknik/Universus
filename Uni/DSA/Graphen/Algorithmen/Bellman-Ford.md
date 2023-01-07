---
tags: uni dsa practical-cs graph algorithm
cards-deck: Uni::Courses::DSA
completed: true
aliases: Bellman-Ford
linter-yaml-title-alias: Bellman-Ford
date-of-creation: 2022-07-23
mod-date: 2022-09-10
---

# Bellman-Ford

## Eigenschaften: #fc
- Einstricht einer [[Breitensuche]] mit *iterativen Relaxieren* der Kanten
- Lässt sich auf [[../Gewichteter Graph|Gewichteten Graphen]] anwenden, in dem Kanten mit *negativen Gewichten* vorkommen
- Führt in der Theorie alle Schritte einer Iteration gleichzeitig aus3
^1658939130608

## Funktionsweise: #fc
- Für jede Iteration $i$ wird der kürzeste Pfad mit der Länge der $i$ bestimmt
	→ Da der Algorithmus theoretisch in jeder iterativen Relaxion alle Pfade gleichzeitig durchläuft, muss man in der Anwendung aufpassen, keinen Pfad der Länge $i+1$ in der $i.$ Iteration mit einzubeziehen
- Der längste Pfad im Graphen hat die Länge |V|-1
	→ Falls sich der Distanzwert nach |V|-1 Iterationen doch noch ändert, existiert ein Zyklus mit negativer Gesamtgewichten
	→ Um festzustellen, dass die Distanzen konstant bleiben, benötigt der Algorithmus noch eine zusätzliche Prüf-Iteration - auch, wenn dem menschlichen Auge die Konstanz schon bei der vorherigen Iteration auffallen könnte
^1653941166149

## Algorithmus:
```
Method: BellmanFord(G, s)

for each u ∊ V[G]\{s} do 
	D[u] := ∞;
od;
D[s] := 0;
Initialisiere Array predecessor[|V|];
for i := 1 to |V| − 1 do
	// Alle Kanten aktualisieren
	for each (u, v) ∊ E do
		if D[u] + γ((u, v)) < D[v] then
			// Entfernung anpassen
			D[v] := D[u] + g((u, v))
			// Vorgänger wird speichern
			predecessor[v] := u
		fi
	od
od
// Auf Zyklen prüfen:
for each (u,v) ∊ E do
	if D[u] + g((u, v)) < D[v] then
		Graph enthält negativen Zyklus!
	fi
od
```
