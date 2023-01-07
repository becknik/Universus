---
tags: uni dsa practical-cs text
cards-deck: Uni::Courses::DSA
completed: true
aliases: Levenshtein-Distanz
linter-yaml-title-alias: Levenshtein-Distanz
date-of-creation: 2022-07-24
mod-date: 2022-09-02
---

# Levenshtein-Distanz

## Eigenschaften:
- Auch *Editierdistanz* genannt

## Funktion: #fc
- Basiert auf einer $(m+1) \times (n+1)$ großen Matrix
	→ Initialisiert durch $D_{0,0} =\varepsilon, D_{i,0}=w_1[i], D_{0,j} = w_2[j]$
- Gleichteure Editier-Operationen:
	- *insert(c)*
	- *update(a $\Rightarrow$ b)*
	- *delete(c)*
- Die Matrix wird nach dem Prinzip der [[../Algorithmen/Muster/Dynamische Programmierung|dynamischen Programmierung]] von links oben nach rechts unten abgelaufen
- Nach der Ausfüllung der Tabelle steht rechts unten die Levenshtein-Distanz
^1656412906962

## Anwendung:
- Rechtschreibüberprüfung
- Alternativvorschläge bei Suchmaschinen
