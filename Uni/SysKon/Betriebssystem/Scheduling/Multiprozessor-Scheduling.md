---
tags: uni practical-cs syskon os scheduling
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Multiprozessor-Scheduling
  - Affinität
  - Load-Sharing
linter-yaml-title-alias: Multiprozessor-Scheduling
date-of-creation: 2022-11-25
mod-date: 2023-01-03
---

# Multiprozessor-Scheduling
→ [[../Scheduling|Scheduling]]

## Art des Problems
- Wann soll ein Prozess (oder kernel-Level Thread) ausgeführt werden?
	→ Gleichzeitiges Scheduling von interagierenden Prozessen
- Auf welcher CPU soll ein Prozess ausgeführt werden?
	→ Prozesse haben wegen [[../../../Ro I/Cache|Caching]] und [[../../../Ro I/Aktuelles/Shared Memory|NUMA]] Affinität zu Prozessoren

## Unabhängige Prozesse

### Load-Sharing

#### Prinzip #fc
- Eine globale Warteschlange für Prozesse
	→ Sobald ein Prozessor in IDLE übergeht, wird ihm ein Prozess aus der Warteschlange zugewiesen
	→ Auswahlstrategien: [[Uniprozessoren-Scheduling#FIFO fc|FIFO]], Prozess mit der kleinsten Anzahl an Threads, etc.
^1669411044698

#### Vor- & Nachteile #fc
- Automatische Last-Balancierung zwischen Prozessoren
- [[../Prozess|Prozesse]] müssen zwischen verschiedenen Prozessoren migrieren
	→ Bricht Affinität zum Prozessor durch kalte not-shared Low-Level [[../../../Ro I/Cache#Levels: fc|Cache]]
	→ Bei Server-CPUs wird die Affinität durch [[../../../Ro I/Aktuelles/Shared Memory|NUMA]] zusätzlich beeinflusst
^1669411044701

### Scheduling mit Affinität & Lastbalancierung #fc
1. Lastbalancierung: Beim Erzeugen eines [[../Prozess|Prozesses]] wird er der CPU mit der geringsten Last zugewiesen
	→ Eine Queue pro CPU
	→ Hohe Affinität, aber schlechte Auslastung durch das Fehlen von dynamischer Verteilung nach Fülle der Warteschlangen
2. Lokales [[Uniprozessoren-Scheduling]] pro CPU
- *Besser*: Dynamische Last-Balancierung
	- Sobald ein [[../Prozess|Prozess]] *Ready* wird, wird eine CPU für ihn festgelegt
	- *Work-Stealing*: Wenn eine CPU IDLE wird, wird versucht ein Prozess aus der Warteschlange einer anderen CPU zu migrieren
		→Keine Prozess-Migration, wenn die Kosten zu hoch sind
		→ Kosten werden durch CPU-Topologie ([[../../../Ro I/Aktuelles/Shared Memory|NUMA]]) und inaktiver Zeit abgeschätzt
	- Periodische Lastbalancierung findet alle $n\cdot10^{-3}$ Sekunden statt ($n\leq10$)
^1669416234697

## Interaktive Prozesse

### Eigenschaften & Lösungen #fc
→ Viele Betriebssysteme planen Threads unabhängig ein
- Das *gleichzeitige Ablaufen* von interagierenden Threads verbessert die Durchlaufzeit der Thread-Menge
- Partitionierung von interagierenden Threads in…
	- …*Spaces*, die gemeinsam eingeplant werden (*Space-Sharing*)
		→ Menge von Threads können nur ausgeführt werden, wenn die Partition von Threads IDLEt
	- …*Gangs*, die zeitgleich auf mehreren Prozessoren aufgebracht werden (*Gang-Scheduling* = *Space-Sharing* & *Time-Sharing*)
		→ Alle Mitglieder einer Gang bekommen ein synchronisiertes Zeitquantum zugeteilt
		→ Probleme: IDLEn von CPUs, wenn die Ganz zu groß ist, I/O bei einem Mitglied der Gang verschwendet Ressourcen
		→ Lösungsansätze: *Paired-Gang-Scheduling*
^1669416234700
