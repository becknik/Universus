---
tags: uni practical-cs syskon os process
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - Prozesskontrollblock
  - PCB
linter-yaml-title-alias: Prozesskontrollblock
date: 2022-11-12
mod-date: 2022-11-12
---

# Prozesskontrollblock

## Komposition #fc
- PCB
	-> Der wesentliche Zustand eines Betriebssystems besteht aus Kontrollblöcken
- [[../../../Ro I/OS & Environment/Speicherorganisation|Rechnerorganisation I/Speicherorganisation]]:
	-> User-Stack, Heap, BSS, Data, Text-Segment
- Gemeinsamer Adressraum
^1668288356125

## Aufbau: (6) #fc
- Prozessidentität: Eine eindeutige Nummer
- Prozessstatus: PC, Stapelzeiger, Regster, Process Status Word
- Scheduling-Information: Prozessorstand (=neu, bereit, blockiert), Priorität, Wartezeit…
- I/O-Informationen: Zugehörige Dateien, I/O-Geräte
- Speicherinformationen: Seitentabellen
- Accounting-Informationen: CPU-Zeit
- Weitere Informationen wie z.B. PID der Eltern-Prozesse
^1668288356133
