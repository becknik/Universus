---
tags: uni dsa practical-cs tree indexstruct 
cards-deck: Uni::Courses::DSA
completed: true
aliases: Suchbaum
date-of-creation: 2022-07-25
mod-date: 2022-07-27
linter-yaml-title-alias: Suchbaum
---

# Suchbaum

## Einfügen:
1. Finden der Einfügeposition durch Ausnutzung der Sortierung
2. Neuer Knoten mit dem einzufügenden Element wird erstellt und eingefügt
	 → Falls ein Knoten mit dem Element schon an der Einfügeposition existiert, liefert die Operation die Rückgabe *false*

## Löschen: #fc
1. Der zu löschende Knoten $k$ wird gesucht
2. Nachrück-Knoten finden und den Baum dementsprechend anpassen:
	- $k$ ist ein *Blattknoten*: Löschen
	- $k$ hat *ein Kind*: Kind wird hochgezogen
	- $k$ hat *zwei Kindknoten*: Ersetzen durch den *Inorder-Vorgänger*
		→ Damit der Baum nicht entartet, wird in der Praxis zwischen Inorder Vor- und Nachfolger abgewechselt
^1651411457673
