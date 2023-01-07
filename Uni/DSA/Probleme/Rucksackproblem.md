---
tags: dsa practical-cs problem algorithm
cards-deck: Uni::Courses::DSA
completed: false
aliases: Rucksackproblem
linter-yaml-title-alias: Rucksackproblem
date-of-creation: 2022-07-19
mod-date: 2022-09-08
---

# Rucksackproblem

## Prinzip:
- Gegeben:
	- Ein Rucksack mit der Kapazität $C$
	- Eine Menge von $n$ Gegenständen $\in (g_i,w_i)$ mit Gewicht $g_i$ und Wert $w_i$
- Gesucht:
	- Eine Auswahl von Gegenständen über die Indexmenge $I \subseteq \{1,\dots,n\}$, sodass *C* nicht überschritten ist und $\sum_{i \in I} w_i$ maximal ist
- *Approximative Lösung* durch einen [[../Algorithmen/Muster/Greedy|Greedy-Algorithmus]]:
	- Array wird nach Werten sortiert
	- Das Array soll vom wertvollsten zum wertlosesten Element durchlaufen werden und das in den Rucksack packen, was noch reinpasst

## Eigenschaften:
- Entscheidungsvariante: [[../../Theo II/Komplexitättheorie/Zeitklassen/NP|NP-vollständig]]
- Optimierungsproblem: [[../../Theo II/Komplexitättheorie/Zeitklassen/NP|NP-hart]]

## Algorithmus:
```
Method: rucksack (n, int C)
f : Array [2..n][0..C] int;
// Initialisiere für i = n
for rc = 0 to C do
	if rc < g_i then
		f(n,rc) := 0
	else
		f(n,rc) := w_ii
	fi
od;
for i = n − 1 to 2 do
	for rc = 0 to C do
		if rc < g_i then
			f(i,rc) := f(i + 1,rc)
		else
			f(i,rc) := max(f(i + 1,rc), f(i + 1, rc − g_i) + w_i)
		fi
	od
od;
// Berechne f(1,C)
if C < g1
	then return f(2,C)
	else return max(f(2,C), f(2,C − g_1) + w_1)
fi
```
→ Garantiert optimale Lösung durch [[../Algorithmen/Muster/Dynamische Programmierung|dynamische Programmierung]]
