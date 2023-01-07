---
tags: uni dsa practical-cs graph indexstruct
cards-deck: Uni::Courses::DSA
completed: true
aliases: Adjazenzliste
date-of-creation: 2022-07-25
mod-date: 2022-07-27
linter-yaml-title-alias: Adjazenzliste
---

# Adjazenzliste

## Eigenschaften: #fc
- Nachbarschaften werden durch eine Liste in einer für den Knotenindex verantwortlichen Liste gespeichert
	→ Die Zeitkomplexität ist von der Realisierung der verwendeten Liste abhängig
- Die Datenstruktur kann wie eine [[../../Datenstrukturen/Linked List|Linked List]] dynamisch wachsen
- Die Leerstellen einer [[Adjazenzmatrix|Adjazenzmatrix]] werden eingespart
- Kann bedarfsgerecht auch mit Arrays kombiniert werden
^1658939224056

## Einfügen Von Kanten: #fc
- Bedarf den Test, ob die Kant schon existiert
	→ Teurer als bei [[Adjazenzmatrix|Adjazenzmatritzen]]
^1658939224065

## Löschen Von Knoten: #fc
- Ist im Vergleich zu [[Adjazenzmatrix|Adjazenzmatritzen]] sehr teuer, da alle sekundären Listen nach dem Knoten abgesucht werden müssen
^1658939224068
