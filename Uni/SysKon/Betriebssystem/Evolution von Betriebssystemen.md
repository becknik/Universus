---
tags: uni practical-cs syskon os
cards-deck: Uni::Courses::SysKon
completed: false
aliases: Evolution von Betriebssystemen
linter-yaml-title-alias: Evolution von Betriebssystemen
date-of-creation: 2022-11-12
mod-date: 2023-01-02
---

# Evolution von Betriebssystemen
→ [[../OS]]

## Serielle Verarbeitung
- Das manuell aufgebracht Programm muss angeschlossene Geräte selbst steuern und interagieren

## Batch-Systeme
- *Batch*/*Stapel*: Fasst mehrere Programme zusammen und kontrolliert deren Ablauf auf dem System
	→ Monitore steuern das Aufbringen von Programmen, die Hardware und Speicherverwaltung

## Uniprogrammierung
- Programme werden in sequenzieller Reihenfolge abgearbeitet
	→ Mehrere Programme können durch ein Batch auf Lochkarten oder Eigabebändern, ein Programm wird in den Hauptspeicher geladen
	→ Ein Monitor kontrolliert den Programmablauf und gibt das Ergebnis aus
- Zugriffe auf Ein-/Ausgabe ist i.d.R. deutlich langsamer, weshalb kaum Berechnungen auf der CPU ausgeführt werden
- Der Unterschied zwischen Prozessorgeschwindigkeit und I/O wächst (auch durch Cloud Computing oder NAS) stetig
	→ [[../../Ro I/Performanz/Out-Of-Order Issue|Out-Of-Order Issue]] und Prozess Scheduling beim Warten

## Multiprogrammierung/ Multitasking

### Erforderliche Konzepte: (5) #fc
- [[Prozess|Prozesskonzept]]: Verwaltung des Zustands eines Programms
- Die [[Unterbrechungen|Unterbrechung]] der Ausführung eines Prozesses mit Unterbrechungsbehandlung
- Eine Effiziente Steuerung von *I/O-Geräten*
	→ *Unterbrechungsgesteuert I/O*
	→ Direct Memory Access
- Verwaltung *gemeinsamer Ressourcen* im [[../../Ro I/Virtualisierung/Virtueller Speicher|(virtuellen)]] [[../../Ro I/Speicher/DRAM|Speicher]] und *Sekundärspeicher*
- *Scheduling*: Bestimmung des Ausführungszeitpunkts eines [[Prozess|Prozesses]]
	→ Ziel: Maximale [[../../Ro I/Performanz/CPU-Time|CPU-Time]]
^1668082787214

### Time-Sharing #fc
- Unterstützt zusätzlich die Interaktion einer Anwendung mit seiner Umwelt
	→ Zum Beispiel bei Anwendungen mit Nutzerinteraktion
- Optimierungsziele: Kurze Antwortzeit für alle Prozess-Schedulings
- Anforderung: Fairness
^1673097518038

## Echtzeitfähigkeit
→ [[Echtzeitfähigkeit]]
