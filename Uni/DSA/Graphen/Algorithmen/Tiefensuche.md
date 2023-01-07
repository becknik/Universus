---
tags: uni dsa practical-cs graph algorithm
cards-deck: Uni::Courses::DSA
completed: false
aliases: Tiefensuche
linter-yaml-title-alias: Tiefensuche
date-of-creation: 2022-07-23
mod-date: 2022-09-08
---

# Tiefensuche

## Eigenschaften: #fc
- ! [[../Topologische Sortierung|Topologisches Sortieren]]
- ! Zum Testen auf Zyklen durch die Detektion von Rückwärtskanten
- Kann zur [[../../Suchverfahren|Suche]] und [[../../Algorithmen auf Graphen||Traversierung]] eingesetzt werden
- Kann zur Konstruktion des [[../Spann- & Wurzelbaum|Spann- & Wurzelbaum]] eingesetzt werden
- Nur für [[../Ungerichtete Graphen|Ungerichteter Graphen]]: Zum Finden von [[../Zusammenhangskomponenten|Zusammenhangskomponenten]]
	- → Variation für [[../Gerichtete Graphen|gerichtete Graphen]]: z.B. [[Algorithmus von Tarjan]]
- Kann zur Überprüfung, ob ein Graph [[../Planarer Graph|planar]] ist, verwendet werden[^1]
- Liegt im schlechtesten Fall in $\mathbfcal{O}(|V|+|E|)$
^1654949633212

## Funktionsweise: #fc
→ Für mehrere [[../Zusammenhangskomponenten|Zusammenhangskomponenten]] muss der Algorithmus so lange iterativ ausgeführt werden, bis kein weißer Knoten mehr im Graph existiert
1. Ein Startknoten wird bestimmt, blau gefärbt und auf den Stack gelegt
2. Alle Knoten werden weiß gefärbt und die initiale Distanz $d$ zum Startknoten wird auf $\infty$ gesetzt
3. Wiederhole, solange der [[../../Datenstrukturen/Stack|Stack]] noch nicht leer ist:
	- Ein Knoten $u$ wird vom Stack gepeekt
	- Bei Suche: Wenn das entnommene Element dem gesuchten Element entspricht, wird die Suche beendet
	- Falls der Knoten $u$ kein nicht-blauen Nachfolger mehr hat, wird er schwarz gefärbt und vom Stack gepopt
		→ [[../Topologische Sortierung|Topologisches Sortieren]]: Der Knoten wird in eine Liste eingetragen und am Ende des Algorithmus ausgegeben
	- Sonst wird der lexikographisch kleinste, noch nicht blau markierte Nachfolgeknoten von $u$ wird blau gefärbt, sein Distanzwert geupdatet und auf den Stack gelegt
4. Wenn der Stack leer ist, liegt das gesuchte Element nicht in der [[../Zusammenhangskomponenten|Zusammenhangskomponente]]
	 → Gebe "nicht gefunden" zurück
^1653923422595

## (Rekursiver) Algorithmus:
```
Methode: DFS (G)
for each Knoten ∊ V[G] do
	farbe[u] = weiß; π[u] = null;
od;
zeit = 0;
for each Knoten u ∊ V[G] do
	if farbe[u] = weiß then 
		DFS-visit(u);
	fi
od
```
```
Methode: DFS-visit (Knoten u)
farbe[u] = blau;
zeit = zeit + 1;
D[u] = zeit;
for each v ∊ u.ZielknotenAusgehenderKanten do
	if farbe[v] = weiß then
		 π[v] = u;
		 DFS-visit(v);
	fi
od
farbe[u] = schwarz;
zeit = zeit + 1;
f[u] = zeit;
```

[^1]: [Wikipedia](https://de.wikipedia.org/wiki/Tiefensuche#Eigenschaften) (25.07.2022)
