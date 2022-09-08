---
tags: uni dsa practical-cs struct abstraction
cards-deck: Uni::Courses::DSA
status: 
aliases: Datenstrukturen
linter-yaml-title-alias: Datenstrukturen
date: 2022-07-21
mod-date: 2022-09-08
---

# Datenstrukturen

## Prinzip: #fc
- Verwalten eine Menge von Daten
- Verknüpfen die enthaltenen Daten über Operationen
- Ermöglichen einen Zugriff in einer geeigneter Weise
- Ermöglichen eine Manipulation der enthaltenen Daten
-> "Erst rechnerverarbeitbare Darstellungen von Informationen erlauben es Programmieren realistischer Probleme in angemessenen Abstraktionsebene"[^1]
^1649750641843

## Eigenschaften: #fc
- *Effizienz*: Im Bezug des Zugriffs oder der Speicherung
	-> In manchen Anwendungsfällen können auch *eigenständige Implementierung* für eine Steigerung der Effizienz verwendet werden
- (Meistens) *Wiederverwendbarkeit*: Gegeben durch Generizität und Bibliotheken
^1649750745819

## Varianten:
- [[Datenstrukturen/Linked List|Liste]]
	-> [[Datenstrukturen/Iterator|Iterator]]
- Zugriffsbeschränkt:
	- [[Datenstrukturen/Queues|Queues]]
	- [[Datenstrukturen/Stacks|Stacks]]
- [[Datenstrukturen/Set|Sets]] (implementiert durch [[Bäume]])
- [[Bäume/Heap|Heap]]
- [[Datenstrukturen für Graphen|Datenstrukturen für Graphen]]
- [[Hashfunktionen|Hashtabellen]]
- [[Nebenläufige Abläufe/Semaphor|Semaphor]]

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021.