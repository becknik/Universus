---
tags: uni dsa practical-cs struct
cards-deck: Uni::Courses::DSA
completed: true
aliases: Linked List
linter-yaml-title-alias: Linked List
date-of-creation: 2022-07-21
mod-date: 2022-09-07
---

# Linked List
→ Ein Spezialfall eines (entarteten) [[../Graphen|Graphen]]

## Eigenschaften: #fc
- Besitzt einen speziellen *Head*-Knoten
- Kann zur Laufzeit *dynamisch* wachsen und schrumpfen
	→ Verschwendet keinen unnötigen Speicherplatz
	→ Wird immer auf dem Heap initialisiert
	→ Das Umsortieren der Liste benötigt *keine umkopieren*
- Das Zusammenführen von zwei Listen der Länge $n$ und $m$ liegt $\in\mathbfcal{O}(n)$
	→ Durch die erste Liste einmal iterieren und dann den letzten Zeiger auf den 0. Index der zweiten Folge setzten
	→ Bei doppelter Verkettung $\in\mathbfcal{O}(1)$ möglich
- Kann für die Realisierung von [[Stack|Stacks]] verwendet werden
	→ Verkettungen von Head- und Tail-Node ermöglichen das Implementieren von [[Queue]]
- Der *wahlfreie Zugriff* bei verketteten Listen liegt in $\mathbfcal{O}(n)$
	→ Auch sind die Zugriffsoperationen *komplizierter* als die von Arrays
^1649751812441

## Einfügen: #fc
- Die spezifizierte Einfüge-Position wird durch einen [[Iterator]] *gesucht*
- Ein *neuer Knoten* wird angelegt
- "*Umzeigern*":
	- Die Referenz des neu erstellten Knotens wird auf den Knoten des *Folgeknotens* gesetzt
	- Die Referenz des *Vorgängerknotens* wird auf den neu erstellten Knoten gesetzt
^1649752034184

## Doppelt Verkettete Liste:
- Besitzt neben einem *Head*- auch einen *Tail*-Knoten
	→ Hier ist der Zugriff auf das letzte Element ist in $\mathbfcal{O}(1)$ möglich
