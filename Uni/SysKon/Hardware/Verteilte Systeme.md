---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
complete: true
aliases: Verteilte Systeme
linter-yaml-title-alias: Verteilte Systeme
date: 2022-11-07
mod-date: 2022-11-10
---

# Verteilte Systeme
-> [[Hardware/Systemarchitekturen|Systemarchitekturen]]

## Funktionsweise: #fc
- Eine Menge von Computing-Nodes aus Einzel- und Mehrkernprozessoren
	-> Doppelt-echte Parallelität
- Es existiert kein gemeinsamer Speicher zwischen den Knoten
- Ein Rechnernetz ermöglicht die Kommunikation zwischen den Knoten
- Echte Parallelität findet zwischen Knoten, Prozessoren eines Knotens und Kernen eines Prozessors statt
^1668080764562

## Eigenschaften: #fc
- Zeitliche Annahmen zur Befehlsordnung ist aufgrund von der *Heterogenität der Rechnersysteme* und *variierender Übertragungszeit* von Nachrichten kaum treffbar
- Das Warten auf den Eingang von Nachrichten kann unnütz Zeit in Anspruch nehmen
^1667834439570
