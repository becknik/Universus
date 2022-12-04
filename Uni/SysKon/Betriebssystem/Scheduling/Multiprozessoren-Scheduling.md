---
tags: uni practical-cs syskon os scheduling
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - Multiprozessoren-Scheduling
  - Affinität
  - Load-Sharing
linter-yaml-title-alias: Multiprozessoren-Scheduling
date: 2022-11-25
mod-date: 2022-11-25
---

# Multiprozessoren-Scheduling
-> [[../Scheduling|Scheduling]]

## Art des Problems: #fc
- Wann soll ein Prozess (oder kernel-Level Thread) ausgeführt werden?
	-> Gleichzeitiges Scheduling von interagierenden Prozessen
- Auf welcher CPU soll ein Prozess ausgeführt werden?
	-> Prozesse haben wegen [[../../../Ro I/Cache|Caching]] und [[../../../Ro I/Aktuelles/Shared Memory|NUMA]] Affinität zu Prozessoren
^1668895131025

## Unabhängige Prozesse

### Load-Sharing

#### Prinzip: #fc
- Eine globale Warteschlange
- Sobald ein Prozessor frei wird, wird ihm ein Prozess aus der Warteschlange zugewiesen
	-> Auswahlstrategien: [[../../../DSA/Datenstrukturen/Queue|FIFO]], Prozess mit der kleinsten Anzahl an Threads
^1669411044698

#### Nachteile: #fc
- [[../Prozess|Prozesse]] müssen zwischen verschiedenen Prozessoren migrieren
	-> Bricht Affinität zum Prozessor durch kalte Cache ([[../../../Ro I/Aktuelles/Shared Memory|NUMA]])
^1669411044701

### Scheduling mit Affinität & Lastbalancierung #fc
- Eine Ready-[[../../../DSA/Datenstrukturen/Queue|Queue]] pro CPU
- Dynamische Last-Balancierung/ Migration:
	- Sobald ein [[../Prozess|Prozess]] Ready wird, wird entschieden, auf welcher CPU dieser ausgeführt werden soll
	- *Work-Stealing*: Wenn eine CPU idle wird, wird versucht ein Prozess aus der Warteschlange einer anderen CPU zu migrieren
		-> Periodische Überprüfung alle paar $10^{-3}$ sec
- Rücksichtnahme auf Affinität unter Rücksichtnahme auf Kosten
	-> "*Entfernung*" zwischen zwei CPUs (CPU-Topologie/ [[../../../Ro I/Aktuelles/Shared Memory|NUMA]])
	-> Inaktive Zeit & verbundene "Frische" der [[../../../Ro I/Cache|Cache]]
	-> Durch das "verfallenen" der Cache nimmt die *Affinität* zu Threads über Zeit ab
^1669416234697

### Interaktive Threads: #fc
-> Viele Betriebssysteme planen Threads unabhängig ein
- Das gleichzeitige Ausführen von interagierenden Threads verbessert die Durchlaufzeit der Thread-Menge
	-> Partitionierung von interagierenden Threads in…
	- "Spaces", die gemeinsam eingeplant werden
	- "Gangs", die zeitgleich auf mehreren Prozessoren aufgebracht werden (=*Space-Sharing*)
		-> Bekommen alle ein synchronisiert beginnendes, begrenztes Zeitquantum (=*Space-Sharing*)
		-> Probleme: Idlen von CPUs, wenn die Ganz zu groß ist
		-> I/O bei einem Thread verschwendet [[../../../Ro I/Performanz/CPU-Time|CPU-Time]] (Lösungsansätze: Paired-Gang-Scheduling)
^1669416234700
