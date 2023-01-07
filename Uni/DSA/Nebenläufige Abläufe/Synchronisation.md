---
tags: uni dsa practical-cs parallel java  
cards-deck: Uni::Courses::DSA
completed: true
aliases: Synchronisation
date-of-creation: 2022-07-27
mod-date: 2022-08-05
linter-yaml-title-alias: Synchronisation
---

# Synchronisation

## Interprozess: #fc
- Prozesse interagieren untereinander durch Kommunikation z.B. über [[../../Ro I/Aktuelles/Shared Memory|Shared Memory]] oder Dateizugriffe
- Bei verteilten Systemen erfolgt die Kommunikation über (Level 4) Netzwerkprotokolle oder High-Level Protokolle
^1657017634566

## Intraprozess: #fc
- Synchronisation der Threads mit Hilfe von Monitoren
- **Monitor**: Regelt den Zugriff von Threads auf *kritische Bereiche* durch das Sicherstellen von *Wechselseitigen Ausschluss* von Threads
	→ *synchronized* in Java
- [[Semaphor|Semaphor]]
^1657019361152
