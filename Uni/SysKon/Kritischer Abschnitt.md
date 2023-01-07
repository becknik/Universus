---
tags: uni practical-cs syskon parallel sync
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Kritischer Abschnitt
  - KA
  - Critical Section Problem
  - Präprotokoll
  - Postprotokoll
linter-yaml-title-alias: Kritischer Abschnitt
date-of-creation: 2022-11-26
mod-date: 2023-01-04
---

# Kritischer Abschnitt
→ Wechselseitiger Ausschluss: "Zwei Menschen stehen an einer Tür und \"Nach Dir\"-en abwechselnd für immer"

## Problemstellung #fc
- Gegeben:
	1. Zugriff auf gemeinsame Ressourcen/ Daten
	2. Nicht [[Atomizität|atomar]] ausführbare Befehle auf diesen gemeinsamen Daten, bezeichnet als **kritischer Abschnitt**
 - Gesucht: Die Vermeidung der Verschachtelung von
^1669419445822

## Beweise
- Annahme, der verbotene Zustand wird erreicht
	→ Schrittweise rück-verfolgen & zum Widerspruch führen

## [[Betriebssystem/Prozesse/Threads|Thread]]-Sicht #fc
```
  Nicht kritischer Abschnitt
Präprotokoll
  Kritischer Abschnitt
Postprotokoll
```
- Ein *Präprotokoll* stellt sich, dass…
	- … keine Race-Conditions über die gemeinsamen Ressourcen entstehen
		→ Nur ein Thread gleichzeitig im kritischen Abschnitt
	- … "nicht kritische" Threads müssen auf die Ausführung des *Postprotokolls* waren müssen, um in den KA eintreten zu können
- Vor und nach dem Kritischen Abschnitt ist eine beliebige Verschachtelung der Befehle und Ausführungszeit möglich
	→ Threads müssen den KA nicht zwingend betreten
^1669419445825

## Korrektheitskriterien

### Schwache Formulierung #fc
→ Jede Lösung zum Problem des *kritischen Abschnitts* muss sie erfüllen
1. *Mutual Exclusion*: Keine Verschachtelung von Befehlen zweier [[Betriebssystem/Prozesse/Threads|Threads]] bezüglich der Befehle im KA
2. Kein/e Deadlock/ [[#Verklemmung fc|Verklemmung]]: Letztendlich ist ein Thread (von mehreren) bei dem Versuch einen kritischen Abschnitt zu betreten erfolgreich
- Garantiert die Konsistenz der Daten (*Wechselseitiger Ausschluss*)
- Garantiert ein Fortschreiten in der Ausführung (keine [[#Verklemmung fc|Verklemmung]])
- Garantiert nicht: Dem *individuellen Fortschritt* eines bestimmten Threads
^1672782020780

### Starke Formulierung #fc
→ Zusätzlich zu *Mutual Exclusion* & [[#Verklemmung fc|Verklemmung]] ([[#Schwache Formulierung fc|schwachen Formulierung]]):
- 3. *Kein Aushungern*: Wenn ein [[Betriebssystem/Prozesse/Threads|Thread]] einen Abschnitt betreten möchte, wird er ihn letztendlich betreten
Zu beachten:
 - Neben der [[Betriebssystem/Scheduling|Scheduling]]-Fairness ist zusätzlicher Aufwand nötig
- Muss muss für jede beliebige [[Korrektheitskriterien#Schwach: fc|schwache Fairness]] Ausführung des *Schedulers* sichergestellt werden
^1669419082099

## Verklemmung #fc
- Eine Menge von Threads $T$ kann nicht in der Ausführung fortschreiten, da…
1. $\forall t\in T$ warten auf das *Ereignis* eines anderen Threads $t'$
2. das Auftreten des *Ereignisses* einen Fortschritt in der Menge erfordert
^1669419445827

## Lösungsverfahren
- [[Nebenläufigkeit/Dekkers Algorithmus|Dekkers Algorithmus]]
- [[Nebenläufigkeit/Bakery-Algorithmus|Bakery-Algorithmus]]
- [[Nebenläufigkeit/Spin-Locks|Spin-Locks]] durch [[Nebenläufigkeit/Spin-Locks|RMW]]
- [[Nebenläufigkeit/Semaphore|Semaphore]]
- [[Nebenläufigkeit/Monitore|Monitore]]
