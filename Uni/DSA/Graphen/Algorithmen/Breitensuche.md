---
tags: uni dsa practical-cs graph algorithm
cards-deck: Uni::Courses::DSA
completed: true
aliases: Breitensuche
linter-yaml-title-alias: Breitensuche
date-of-creation: 2022-07-23
mod-date: 2022-09-08
---

# Breitensuche

## Eigenschaften: #fc
- ! Finden des kürzesten Weges bei ungewichteten Kanten
- ! Nur für [[../Ungerichtete Graphen|ungerichtete Graphen]]: Bestimmung der [[../Zusammenhangskomponenten|Zusammenhangskomponenten]]
- Die BFS kann auch als [[../../Suchverfahren|Suchverfahren]] und zur [[../../Algorithmen auf Graphen||Traversierung]] verwendet werden
- Durch das Setzen einer zusätzlichen Referenz $\pi$ in jedem Knoten lässt sich ein [[../Spann- & Wurzelbaum|Spannbaum]]/ [[../Spann- & Wurzelbaum|Wurzelbaum]] erstellen
- Speziell für [[../Gerichtete Graphen|gerichtete Graphen]] lassen sich mit Hilfe der BFS Entry Points bestimmen
- Kann nur bei [[../Gewichteter Graph|ungewichteten Graphen]] zur Bestimmung des kürzesten Weges verwendet werden
	→ Die Erweiterung für Gewichtete: Der [[Dijkstra]]
- Liegt im schlechtesten Fall in $\mathbfcal{O}(|V|+|E|)$
^1653921689772

## Funktionsweise: #fc
1. Bestimme einen *Startknoten*, färbe ihn blau und lege ihn in die *Queue*
2. Alle Knoten im Graphen, den Startknoten ausgeschlossen, werden weiß markiert und die Distanz $d$ zum Wurzelknoten auf $\infty$ gesetzt
3. Wiederhole, solange die [[../../Datenstrukturen/Queue|Queue]] nicht leer ist:
	- Ein Knoten $u$ wird aus der Queue gepeekt
	- Bei Suche: Wenn das entnommene Element dem Gesuchten entspricht, ist die Suche beendet
	- Die Folgeknoten von Knoten $u$ werden, wenn sie noch nicht in der Queue sind, blau markiert, ihr Entfernungswert aktualisiert und auch in die Queue gelegt
		→ Bei Spannbaum: Die Referenz $\pi$ des aktuellen Knotens wird zusätzlich auf die noch nicht blau markierten Knoten gesetzt
	- Der Knoten $u$ wird schwarz gefärbt und aus der Queue entfernt
4. Wenn die Queue leer ist, liegt das gesuchte Element nicht in der [[../Zusammenhangskomponenten|schwachen Zusammenhangskomponente]]
	→ Element nicht gefunden
^1653921378754

## Algorithmus:
```
Method: BFS (G, start)
for each Knoten u:V[G]\start do
	farbe[u] = weiß;
	D[u] = ∞;
	π[u] = null;
od
farbe[start] = blau;
d[start] = 0;
π[start] = null;
Q = [start];
while !Q.isEmpty() do
	current = Q.front();
	for each Knoten v ∊ current.ZielknotenAusgehenderKanten do
		if farbe[v] = weiß then
			farbe[v] = blau;
			d[v] = d[current]+1;
			π[v] = current;
			Q.join(v);
		fi;
	od;
	Q.leave(current); //?
	farbe[u] = schwarz;
od;
```
