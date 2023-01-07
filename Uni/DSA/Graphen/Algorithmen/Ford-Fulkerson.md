---
tags: uni dsa practical-cs graph flow algorithm bipartit
cards-deck: Uni::Courses::DSA
completed: false
aliases: Ford-Fulkerson
linter-yaml-title-alias: Ford-Fulkerson
date-of-creation: 2022-07-24
mod-date: 2022-09-10
---

# Ford-Fulkerson

## Eigenschaften:
- Berechnet den [[../Maximaler Fluss|maximalen Fluss]] in einem Graphen
- Er ist eigentlich formal betrachtet kein Algorithmus
	→ Es gibt allerdings Strategien mit minimaler Schrittzahl !!!

## Funktionsweise: #fc
- Es werden so lange wie möglich Pfade zum Gesamtfluss hinzugefügt
	→ Die Auswahl der Pfade ist standardmäßig nicht festgelegt, z.B. durch Verwendung der [[Tiefensuche|Tiefensuche]]
- Der ausgewählte Pfad kann das Netzwerk auch in umgekehrter Richtung folgen (?)
- Der resultierende Durchfluss wird mit $c_f$ angegeben und der Gesamtfluss daraufhin angepasst
- Der Pfad kann Kanten auch in umgekehrter Richtung folgen
- Es gibt verschiedene Strategien zur Auswahl eines nutzbaren Pfades (z.B. [[Tiefensuche|Tiefensuche]])
^1655042347577

## Algorithmus: !!!
```
for each (u, v) ∊ E[G] do
	f(u,v) = 0;
	f(v,u) = 0;
od;
while es existiert Pfad p von s nach t im Restnetzwerk G_f do
	c_f(p) = min {c_f(u,v) | (u,v) ∊ p};
	for each (u,v) in p do
		// Vergrößerung des Flusses in Pfadrichtung
		f(u,v) = f(u,v) + c_f(p)
		// Verkleinerung des Flusses in entgegengesetzter Richtung
		f(v,u) = f(v,u) – c_f(p)
	od;
od;
```

## Reduktion auf Bipartite Graphen [[../Matching|Matching]]: #fc
1. Ungerichtete Kanten werden in gerichtete Kanten von $A$ nach $B$ umgewandelt
	 → [[../Bipartite Graphen|Bipartite Graphen]]
2. Hinzufügen von einer Quelle $s$ mit gerichteten Kanten zu $\forall a \in A$ und einer Senke $t$ mit Kanten von $\forall b \in B$
3. Alle Kantengewichte werden auf 1 gesetzt
4. Bestimme den maximalen Durchfluss durch die Ausführung des Ford-Fulkerson Algorithmus
^1659708933065
