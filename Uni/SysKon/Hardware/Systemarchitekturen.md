---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - Systemarchitekturen
  - quasi-parallel
linter-yaml-title-alias: Systemarchitekturen
date: 2022-10-24
mod-date: 2022-10-24
---

# Systemarchitekturen

## Einzelkernprozessoren
- Es kann höchstens eine Instruktion zu jedem Zeitpunkt ausgeführt werden
- Quasi-Parallelität durch Multitasking bei Warten auf Interrupts oder I/O
	-> Trägt zur erhöhten Ausnutzung des Prozessorkerns bei

## Mehrkernprozessoren
- Alle Kerne greifen auf einen gemeinsamen Speicher zu
- Echtere Parallelität kann durch Multi-Tasking auf jedem Kern stattfinden

## Multiprozessor-Systeme
- Mehrere Prozessoren (mit mehreren Kernen) arbeiten zusammen
- Jeder Prozessor hat seinen eigenen Speicher
- Häufig existiert ein globaler Speicher, den alle Prozessoren nutzen

## Verteilte Systeme
- Eine Menge von Computing-Nodes aus Einzel- und Mehrkernprozessoren
	-> Doppelt-echte Parallelität
- Es existiert kein gemeinsamer Speicher zwischen den Knoten
- Ein Rechnernetz ermöglicht die Kommunikation zwischen den Knoten
- Echte Parallelität findet zwischen Knoten, Prozessoren eines Knotens und Kernen eines Prozessors statt
