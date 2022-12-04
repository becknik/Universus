---
tags: uni practical-cs syskon parallel sync
cards-deck: Uni::Courses::SysKon
complete: true
aliases: Dekkers Algorithmus
linter-yaml-title-alias: Dekkers Algorithmus
date: 2022-12-03
mod-date: 2022-12-03
---

# Dekkers Algorithmus
-> [[Kritischer Abschnitt|Kritischer Abschnitt]]
-> Einfachere Alternative: [[Pettersons Algorithmus]]

## Eigenschaften: #fc
- Die erste bekannte Lösung des [[Kritischer Abschnitt|Critical Section Problems]]
- Funktioniert nur für 2 [[../Betriebssystem/Prozesse/Threads|Threads]]
- Unter dem Einsatz von [[../Sequenzielle Konsistenz|Memory Order Models]] nicht mehr korrekt
^1670082513496

## Algorithmus: #fc
```
Procedure p:
loop:
	<Nicht kritischer Abschnitt>
	want_p ← true
	while want_q
		if process_turn = 2
			want_p ← false
			await process_turn = 1
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
			await process_turn = 2
			want_q ← true
	<Kritischer Abschnitt>
	process_turn ← 1
	want_q ← false
```
- Invarainten:
	- Entweder `want_p` oder `want_q` sind `true`
	- `process_turn` ändert sich nicht, wenn `p` und `q` in der while-Schleife festhängen
^1670080850045
