---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Referenzarchitektur
linter-yaml-title-alias: Referenzarchitektur
date-of-creation: 2022-10-24
mod-date: 2022-11-12
---

# Referenzarchitektur
→ *Modell der Nebenläufigkeit*

## Anwendung #fc
- Nebenläufige integrierende Prozesse/ Threads
	→ Können auch auf mehrere Knoten verteilt sein
^1666632369067

## Middleware #fc
- Stellt höhere Konzepte zur Kommunikation und Synchronisierung bereit
- Kann auf eine Programmiersprache spezialisiert oder sprachunabhängig sein
^1666632369070

## Betriebssystem #fc
- Dynamisches Management der Rechnerressourcen (CPU, Speicher, I/O) und Vergabe dessen an Prozesse
	→ Ermöglicht eine dynamische Erstellung/ Terminierung von Prozessen
- Bildet eine wohldefinierte Schnittstelle zum Zugriff auf Systemressourcen
- Bietet Schutzmechanismen
^1668270787846

### *Rechnernetz* #fc
- Management der Netzressourcen
- Netzwerkkommunikation zwischen Threads
^1666632369073

## Komposition
- [[Betriebssystem/OS-Struktur|Struktur]]
- [[Betriebssystem/Prozesse/Prozesswechsel|Prozesswechsel]]
- [[Betriebssystem/Prozess|Prozessverwaltung]]
- [[Betriebssystem/OS-Echtzeitfähigkeit|Echtzeitfähigkeit]]
- [[../Ro I/Aktuelles/Shared Memory|Shared Memory Management]]
- [[Betriebssystem/Komponenten/Message Passing Interface|Interprozesskommunikation]]
