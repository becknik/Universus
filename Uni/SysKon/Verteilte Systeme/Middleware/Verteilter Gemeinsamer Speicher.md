---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Verteilter Gemeinsamer Speicher
  - Tupelräume
linter-yaml-title-alias: Verteilter Gemeinsamer Speicher
date-of-creation: 2023-01-06
mod-date: 2023-01-06
---

# Verteilter Gemeinsamer Speicher

## Prinzip
- Speicherseiten werden zwischen mehreren Systemen geteilt
- Zugriff erfordert explizite Kommunikation
	→ Kann auch im [[../../OS|OS]] integriert sein

## Eigenschaften #fc
- Erfordert Sperrungen bei [[../../Kritischer Abschnitt|KAs]]
- Mehr Synchronisation, weniger Parallelität → schlechtere Skalierbarkeit
- Archaische Programmierung des Speichers, da keine Datentypen & Typ-Unsicherheit herrscht
	→ Typ-Unsicherheit kann durch den Einsatz von [[Verteilter Gemeinsamer Speicher|Tupelräumen]] gelöst werden
^1673038480045

## Tupelräume
- Abstraktion von konkreten Speicher & stellen Datentypen zur Verfügung
- VGT Grundprobleme (Konsistenz & Synchronisation) bleiben trotz Abstraktion bestehen
- Tupelraum-Systeme:
	- Linda - der Tupelraum-Pionier
	- JavaSpaces
