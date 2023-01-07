---
tags: uni practical-cs syskon parallel sync
cards-deck: Uni::Courses::SysKon
completed: false
aliases: Dekkers Algorithmus
linter-yaml-title-alias: Dekkers Algorithmus
date-of-creation: 2022-12-03
mod-date: 2023-01-03
---

# Dekkers Algorithmus
→ [[../Kritischer Abschnitt|Kritischer Abschnitt]]

## Annahmen
- [[../Atomizität|Atomizität]] im Schreiben auf gemeinsame Variablen
- [[../Synchronisation/Sequenzielle Konsistenz|Sequenzielle Konsistenz]] bei Speicherzugriffen
- [[../Korrektheitskriterien|Schwach fairer]] [[../Betriebssystem/Scheduling|Scheduler]]

## Eigenschaften
- Die erste bekannte Lösung des [[../Kritischer Abschnitt|Critical Section Problems]]
- Funktioniert nur für 2 [[../Betriebssystem/Prozesse/Threads|Threads]]
- Unter dem Einsatz von [[../Synchronisation/Sequenzielle Konsistenz|Memory Order Models]] nicht mehr korrekt
- Einfachere Alternative: Pettersons Algorithmus !!!

## Algorithmus #fc
```
Procedure p:
loop:
	<Nicht kritischer Abschnitt>
	want_p ← true
	while want_q
		if process_turn = 2
			want_p ← false
			await (process_turn == 1)
			want_p ← true
	<Kritischer Abschnitt>
	process_turn ← 2
	want_p ← false
```
```
Procedure q:
loop:
	<Nicht kritischer Abschnitt>
	want_q ← true
	while want_p
		if process_turn = 1
			want_q ← false
			await (process_turn == 2)
			want_q ← true
	<Kritischer Abschnitt>
	process_turn ← 1
	want_q ← false
```
- Invarainten:
	1. Entweder `want_p` oder `want_q` gilt, jeweils wenn `p` oder `q` sich im [[../Kritischer Abschnitt|KA]] befinden
	2. `process_turn` ändert sich nicht, wenn `p` und `q` in der while-`want_`-Schleife festhängen
^1670080850045

## Beweise

### Wechselseitiger Ausschluss
- Übergänge zu dem imaginären [[../Betriebssystem/Prozess|Prozesszustand]], in dem sich `p` & `q` im [[../Kritischer Abschnitt|KA]] befinden ist nicht möglich
	→ `want_p`/`want_q` verhindert den Austritt aus der `while`-Schleife

### Keine Verklemmungen
1. Verklemmung bei `await (process_turn = = 1)` und `await (process_turn = = 2)`
	 → 2. Invariante: Keine Veränderung von `process_turn` im [[../Kritischer Abschnitt|Präprotokoll]]
2. Verklemmung in den `while`-Schleifen an den `wantp` und `wantq` Bedingungen

### Kein Aushungern
