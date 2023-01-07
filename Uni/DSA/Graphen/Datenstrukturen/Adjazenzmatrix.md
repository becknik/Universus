---
tags: uni dsa practical-cs graph indexstruct
cards-deck: Uni::Courses::DSA
completed: true
aliases: Adjazenzmatrix
date-of-creation: 2022-07-25
mod-date: 2022-07-27
linter-yaml-title-alias: Adjazenzmatrix
---

# Adjazenzmatrix

## Eigenschaften: #fc
- Speichert die Beziehungen zwischen Knoten in einer $|V| \times |V|$-Array-Matrix
	→ Der Spaltenindex gleicht dem Startknoten
- Einige Operationen sind als Matritzenoperationen möglich
- Für [[../Ungerichtete Graphen|ungerichtete Graphen]] reicht die Dreiecksmatrix ohne die Diagonale
- Alle Operationen sind unabhängig von der Anzahl der Kanten
^1653691477336

## Einfügen:
- Ohne Umkopieren kann durch das Vorreservieren von Speicher auch in $\mathbfcal{O}(n)$ anstatt von $\mathbfcal{O}(n²)$ geschehen
