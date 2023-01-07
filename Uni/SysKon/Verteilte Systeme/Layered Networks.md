---
tags: uni practical-cs syskon distributed-systems
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Layered Networks
  - Layer
linter-yaml-title-alias: Layered Networks
date-of-creation: 2023-01-05
mod-date: 2023-01-06
---

# Layered Networks

## Prinzipien #fc
- Zur Koordination der komplexen Funktionen auf unterschiedlichen Abstraktionsebenen gliedert man die Kommunikationen in mehrere Architektur-Schichten auf
- Jede Architektur-Schicht…
	- Realisiert eine Ebene der Abstraktion
	- Stellt der darüberlegenden Schicht eine Service-Primitiv-*Schnittstelle* bereit (*Einkapselung*)
- Zwischen Parteien desselben Architektur-Layers wird auf verschiedenen Geräten mittels [[Protokolle|Protokollen]] kommuniziert
^1673037052746
