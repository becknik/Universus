---
tags: uni practical-cs syskon os process
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Prozesskontrollblock
  - PCB
linter-yaml-title-alias: Prozesskontrollblock
date-of-creation: 2022-11-12
mod-date: 2023-01-02
---

# Prozesskontrollblock

## Prozessabbild mit PCB #fc
- *Prozesskontrollblock*
	→ Zugriff nur in [[../../OS|Ring-0]] möglich
	→ Der wesentliche *Zustand eines Betriebssystems* besteht aus Kontrollblöcken
- User-Stack
- [[../../../Ro I/OS & Environment/Speicherorganisation|Rechnerorganisation I/Speicherorganisation]]:
	→ Bilden den *privaten Adressraum des Prozesses*
- Gemeinsamer Adressraum
^1668288356125

## Aufbau (6+1) #fc
- Prozessidentität *PID*: Eine eindeutige Nummer
- Prozessstatus (Ausführungskontext): [[../../../Ro I/RISC-V/Problem Counter|PC]], Stapelzeiger, [[../../../Ro I/RISC-V/Register|Register]], *Process Status Word*
- [[../Scheduling|Scheduling]]-Information: Prozessorzustand, Priorität, Wartezeit, etc.
- I/O-Informationen: Geöffnete Dateien, I/O-Geräte
- Speicherinformationen: [[../../../Ro I/Virtualisierung/Seitentabelle|Seitentabellen]], etc.
- Accounting-Informationen: [[../../../Ro I/Performanz/CPU-Time|CPU-Time]]
- Mögliche weitere Informationen: PID der Eltern-Prozesse, etc.
^1668288356133
