---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
complete: false
aliases:
  - Message Passing Interface
  - Interprozesskommunikation
  - MPI
linter-yaml-title-alias: Message Passing Interface
date: 2022-11-10
mod-date: 2022-11-19
---

# Message Passing Interface
-> [[../../../DSA/Nebenläufige Abläufe/Message Passing Interface|DSA: Message Passing Interface]]

## Funktionsweise: #fc
- Kommunikation zwischen Prozessen läuft über Sockets des Betriebssystems (/der Netzwerkschnittstelle) ab
	1. Zugriff auf RAM des [[../../OS|OS]] über den Socket/ (Named) Pipes des Programms
	2. Queuing der Nachricht in einen [[../../../DSA/Datenstrukturen/Queue|FIFO-Speicher]] vor dem Socket des Ziel-Prozesses
	3. Kopieren aus der Queue in den *privaten Adressraum* des Programms
^1667835013893

### Zero-Copy: !!!
- Es wird direkt in den Speicher des Ziel-Prozesses geschrieben
	-> Optimiert den "Umweg" über das Betriebssystem weg

## Triviales Beispiel: #fc
```
Procedure p:
	int x < 2;
	send(q,x)
Procedure q:
	int x < 0;
	receive(x)
```
^1667422174745
