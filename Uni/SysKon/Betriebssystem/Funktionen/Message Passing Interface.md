---
tags: uni practical-cs syskon os parallel
cards-deck: Uni::Courses::SysKon
completed: false
aliases:
  - Message Passing Interface
  - Interprozesskommunikation
  - MPI
linter-yaml-title-alias: Message Passing Interface
date-of-creation: 2022-11-10
mod-date: 2023-01-02
---

# Message Passing Interface
→ [[../../../DSA/Nebenläufige Abläufe/Message Passing Interface|DSA: Message Passing Interface]]

## Interprozesskommunikation

### Funktionsweise #fc
1. Übertragung der Nachricht des [[../Prozess|Prozesses]] A auf den [[../../../Ro I/Speicher/DRAM|RAM]]
	 → Funktioniert über [[Sockets]]/ (named) Pipes ([[../../OS|OS]]) des Prozesses $A$
2. Die zu übergebende Nachricht landet in einem [[../../../DSA/Datenstrukturen/Queue|FIFO-Speicher]] vor dem Socket des Ziel-Prozesses $B$
3. Die Nachricht wird aus dem FIFO-Speicher in den *privaten Adressraum* des Prozesses $B$ kopiert
^1667835013893

## Beispiel #fc
```
Procedure p:
	int x < 2;
	send(q,x)
Procedure q:
	int x < 0;
	receive(x)
```
^1667422174745

## Zero-Copy: !!
→ [[../../OS|OS]]
- Schreibt direkt in den Speicher des Ziel-Prozesses, anstelle den "Umweg" über das Betriebssystem zu nehmen
