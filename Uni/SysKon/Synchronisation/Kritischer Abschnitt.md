---
tags: uni practical-cs syskon parallel sync
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - Kritischer Abschnitt
  - Critical Section Problem
  - Präprotokoll
  - Postprotokoll
linter-yaml-title-alias: Kritischer Abschnitt
date: 2022-11-26
mod-date: 2022-12-05
---

# Kritischer Abschnitt
-> Wechselseitiger Ausschluss: "Zwei Menschen stehen an einer Tür und \"Nach Dir\"-en abwechselnd für immer"

## Definition #fc
- Ein nicht *atomar ausführbarer Befehl* auf *gemeinsame Daten*/ Ressource in einem Programmabschnitt
^1669419445822

## Beweis:
- Annahme, der verbotene Zustand wird erreicht
	-> Schrittweise rück-verfolgen & zum Widerspruch führen

## Thread-Sicht #fc
- Ein *Präprotokoll* soll keine Race-Conditions des Zugriffs von einem [[Betriebssystem/Prozesse/Threads|Thread]] auf die Daten sicher stellen
- Die anderen Threads müssen auf die Ausführung des *Postprotokolls* warten
	-> Vor und nach dem Kritischen Abschnitt ist eine beliebige Verschachtelung der Befehle und Ausführungszeit möglich
^1669419445825

## Korrektheitskriterien

### Schwache Formulierung: #fc
- Jede Lösung zum Problem des *kritischen Abschnitts* muss sie erfüllen
1. *Mutual Exclusion*: Keine Verschachtelung von Befehlen zweier [[Betriebssystem/Prozesse/Threads|Threads]] in einem kritischen Abschnitt
2. *Keine Deadlocks/ Verklemmungen*: Letztendlich ist ein Thread bei dem Versuch einen kritischen Abschnitt zu betreten erfolgreich
	 -> Auch wenn mehrere Threads versuchen ihn zu betreten
- Ein Fortschreiten in der Ausführung wird garantiert
	-> Kein individueller Fortschritt eines bestimmten Threads ist garantiert

### Starke Formulierung: #fc
- Zusätzlich zur [[Kritischer Abschnitt|schwachen Formulierung]]:
3. *Kein Aushungern*: Wenn ein [[Betriebssystem/Prozesse/Threads|Thread]] einen Abschnitt betreten möchte, wird er ihn letztendlich betreten
	 -> Muss von Aushungern muss für jede beliebige [[Korrektheitskriterien|schwache faire]] Ausführung sichergestellt werden
	 -> Dafür ist neben der Fairness ein zusätzlicher Aufwand notwendig wird
^1669419082099

## Verklemmung #fc
- Eine Menge von Prozessen kann nicht in der Ausführung fortschreiten, da…
1. $\forall t\in$ Menge der Threads wartet auf das *Ereignis* eines anderen Threads $t'$
2. Das Auftreten des *Ereignisses* erfordert einen Fortschritt in der Menge
^1669419445827
