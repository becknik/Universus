---
tags: uni dsa practical-cs tree trait
cards-deck: Uni::Courses::DSA
completed: true
aliases: Geordneter Baum
linter-yaml-title-alias: Geordneter Baum
date-of-creation: 2022-07-22
mod-date: 2022-09-05
---

# Geordneter Baum

## Definition: #fc
- Die Kindknoten jedes Knotens eines geordneten Baums sind nach einer bestimmten Reihenfolge geordnet
	→ [[Suchbaum|Suchbäume]] sind spezielle geordnete Bäume
^1651672421318

## Binärisierung: #fc
- Gegeben sei ein geordneter, $n$-ärer Baum
- Vorgehen:
	- Jeder *rechte Knoten* auf demselben Niveau eines jeden inneren Knotens des Ausgangsbaums wird im Binärbaum zu seinem *rechten* Kindknoten
	- Der äußerste, *linke Kindknoten* eines inneren Knoten im Ausgangsbaum wird zu dem linke Knoten des Binärbaums
→ Kann auch umgekehrt angewandt werden
^1651409767250
