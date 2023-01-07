---
tags: uni dsa practical-cs graph bipartit algorithm
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Ungarische Methode
  - Kuhn-Munkres
linter-yaml-title-alias: Ungarische Methode
date-of-creation: 2022-07-24
mod-date: 2022-09-07
---

# Ungarische Methode

## Eigenschaften: #fc
- Wird auch *Kuhn-Munkres-Algorithmus* genannt
- Ziel: Es soll ein [[../Matching|Matching]] mit dem maximalen oder minimalen Gewicht auf einem [[../Bipartite Graphen|bipartiten Graphen]] gefunden werden
- Annahme für den bipartiten Graphen: $|A| = |B|$
	→ Eine Erweiterung existiert
^1658939217852

## Funktionsweise: #fc
- Eine [[../Datenstrukturen/Adjazenzmatrix|Adjazenzmatrix]] aus $A$ (Zeile) und $B$ (Spalte) wird erstellt
	→ Falls $|A|\neq|B|$ gilt, soll mit 0-Zeilen und -Spalten aufgefüllt werden
0. Falls ein maximales Matching (für jedes Paar ist der maximale Wert gesucht) gesucht ist: Suche das Maximum in de Matrix und ersetzte alle Werte durch die Differenz zu diesem Wert
	 → Die Matrix sollte nun aus nicht-negativen Werten und dort 0-Werten bestehen, wo vorher die maximalen Zahlenwerte standen
1. Für jede Zeile ($a\in A$): Finde den *kleinsten Wert* und *subtrahiere* ihn von jedem Wert dieser Zeile
2. Für jede Spalte ($b\in B$): Finde den *kleinsten Wert* und *subtrahiere* ihn von jedem Wert dieser Spalte
- Wiederhole:
	3. Bedecke alle 0-Werte mit der *minimalen Anzahl* an Bedeckungen
		4. Falls |Bedeckungen| = $|A|$ ist: `return Zuweisungen`
	5. Der kleinste, durch keine Line bedeckte Wert wird gespeichert
	und von jeder *unbedeckten* Zeile ($a\in A$) *subtrahiert*
	und auf jede bedeckten Spalte ($b\in B$) *addiert*
		→ *Alle Werte* in einer *nicht-durchgestrichenen Zeile* müssen sind von der Subtraktion betroffen, egal ob die Spalte bedeckt ist oder nicht
^1655393399501

## Anwendung:
- *Schema Matching*: Der Austausch von Daten zwischen zwei Datenbanken erfordert eine Zuordnung möglichst ähnlicher Attribute/ Werte oder mit möglichst wenig Distanz

## Algorithmus für Minimale Bedeckungen: #fc
```
zeilenbedeckungen := alle Zeilen;
spaltenbedeckungen := {};
while nicht alle 0-Werte mit ★ oder x markiert sind do
	zeile := Zeile mit minimaler Anzahl an 0-Werten;
	Markiere nicht-merkierten 0-Wert von zeile mit ★
	if Spalte des nun mit ★ markierten 0-Werts beinhaltet weitere 0-Werte
		Markiere diese 0-Werte mit x
	fi;
od
for each zeile (A), die keine ★-Markierung hat do
	if zeile (A) enthält eine x-Markierung then
		x := Spalte (B) mit x-Markierung in der atuellen zeile
		Füge x zu spaltenbedeckungen hinzu;
		stern := Zeile (A) der ★-Markierung in der Spalte x;
		Entferne Zeile stern aus zeilenbedeckungen;
	fi
	entferne zeile aus zeilenbedeckungen
od
return zeilenbedeckungen, spaltenbedeckungen
-→ Die finale Zuordnung entspricht den ★-Markeriungen 
```
→ Wichtig ist nicht die Durchführung, sonder dass die Anzahl an Bedeckungen minimal ist
^1658939217855
