---
tags: uni practical-cs syskon parallel sync
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Semaphore
  - Generelles Semaphor
  - Binäres Semaphor
linter-yaml-title-alias: Semaphore
date-of-creation: 2022-12-03
mod-date: 2023-01-04
---

# Semaphore
→ [[../../DSA/Nebenläufige Abläufe/Semaphor|DSA: Semaphor]]

## Anforderungen #fc
- [[../OS|OS]] kann [[../Korrektheitskriterien|faire]] [[Spin-Locks]] (wie [[Spin-Locks|Ticket-Locks]]) nutzten
	→ Für die konsistente nebenläufige Aktualisierung der Semaphor-Zustandsvariablen notwendig
- [[../Korrektheitskriterien|Fairness]] (=FIFO) in der [[../../DSA/Datenstrukturen/Queue|Queue]]
	- Queues können auch als Mengen ohne Garantie der Fairness oder als Heap (unfair) implementiert werden
- Fairness im [[../Betriebssystem/Scheduling|Scheduling]]
^1670107430671

## Funktionsweise #fc
- Eine Datenstruktur bestehend aus dem *Passier-Integer $k\geq0$ & [[../../DSA/Datenstrukturen/Queue|Queue]] `queue`$=\emptyset$*
- Die beiden Zustandsvariable werden atomar vom [[../OS|OS]] verwaltet
	→ Zugriff über [[../Betriebssystem/Funktionen/System Calls|System Calls]]
- SysCall `wait()`:
	- Dekrementiert `value`
	- Wenn `value`$\leq0$ gilt,wird der [[../Betriebssystem/Prozesse/Threads|Thread]] *blockiert* und in `queue` eingereiht
- SysCall `signal()`:
	- Inkrementiert `value`
	- Signalisiert den wartenden Threads, dass die Ausführung des *kritischen Abschnitts* beendet ist & ein Thread nachrücken kann
^1670107430678

## Pseudocode - Generelles Semaphor
```
integer sem_wait(Semaphore S)
{
	/* Kontextwechsel in Ring-0 */
	S.lock.acquire(); // faires aktives Warten … aber nur kurz!
	S.value--;
	if (S.value < 0)
		/* Blockiere und platziere Thread in S.queue */
		state(currentThread) ← BLOCKED;
		S.queue.append(currentThread);
	}
	S.lock.release();
}
integer sem_wait(Semaphore S)
{
	/* Kontextwechsel in Ring-0 */
	S.lock.acquire(); // faires aktives Warten … aber nur kurz!
	S.value++;
	if (S.value <= 0)
		/* Blockiere und platziere Thread in S.queue */
		Thread t ← S.queue.pop();
		state(t) ← READY;
	}
	S.lock.release();
}
```
→ [[Spin-Locks#Implementierung von Ticket-Locks fc|Spin-Locks: Ticket Locks]]
