---
tags: uni dsa practical-cs design_pattern
cards-deck: Uni::Courses::DSA
status: 
aliases: Greedy
linter-yaml-title-alias: Greedy
date: 2022-07-19
mod-date: 2022-09-06
---

# Greedy

## Prinzip: #fc
- In jedem Teilschritt wird immer der Folgezustand ausgewählt, der den *größten lokalen Gewinn* oder das *beste lokale Ergebnis* verspricht
	-> Das *globale Optimum* muss nicht unbedingt gefunden werden
- Eine *Bewertungsfunktion* wählt den Folgezustand aus
- "Greedy-Algorithmen versuchen in jedem Teilschritt so viel wie möglich zu erreichen"
^1658939020227

## Anwendung: #fc
- [[../../Graphen/Algorithmen/Dijkstra Algorithmus|Dijkstra-Algorithmus]]
- [[../../Graphen/Algorithmen/Algorithmus von Kruskal|Algorithmus Von Kruskal]]
- Geldwechsel-Problem:
	- Ein Geldbetrag $k < 1€$ soll in so wenige Münzen wie möglich gewechselt werden
	- Greedy-Variante: Nehme die höchst verfügbare Münze und ziehe sie vom Geldbetrag ab und mache dies, bis der Betrag gleich 0 ist
		-> Manchmal ist das gefundene lokales Optimum $\neq$ dem globalen Optimum
		-> Beispielsweise wäre $11+1+1+1+1=15, 5+5+5$ wäre hingegen besser
^1658939020236