---
tags: uni practical-cs syskon os parallel threads
cards-deck: Uni::Courses::SysKon
complete: true
aliases: Threads
linter-yaml-title-alias: Threads
date: 2022-11-19
mod-date: 2022-11-26
---

# Threads

## Eigenschaften: #fc
- Threads teilen sich gemeinsame Ressourcen eines Prozesses
	-> Die Verwaltungseinheit für Ressourcen Management stellt der Prozess dar
- Sie bilden eine Verwaltungseinheit fürs [[Scheduling]]
- Erfordern Thread-Synchronisierung
^1668884128898

## Charakteristika: #fc
- Ausführungszustand
- Thread Control Block *TCB*
- Ein eigener [[../../../Ro I/OS & Environment/Stack|Stack]] für Thread-Variablen und lokale Funktionsaufrufe
- Zugriff auf gemeinsame Ressourcen, insbesondere Speicher
^1668884128907

## Vorteile: #fc
- Kommunikation erfordert aufgrund von geteilten lokalen Variablen keine [[../Komponenten/Message Passing Interface|Interprozesskommunikation]] mit OS-Kernel [[../../../Ro I/Performanz/CPU-Time|CPU-Time]]
	-> Keine [[../Komponenten/System Calls|System Calls]], keine [[Unterbrechungen|Software-Interrupts]], Modus- & [[Prozesse/Prozesswechsel|Kontextwechsel]] (-> abhängig vom Synchronisationsmechanismus)
- I/O und Berechnungen überlappen sich
- Echt-parallele Ausführung auf Multiprozessoren
- Minimierung des Zeitaufwands bei Erstellen, Terminierung und wechsel zwischen Threads innerhalb eines Programms
^1668884128909

## Verhältnis Thread - Prozess: #fc
- Ein Prozess - Ein Thread
	-> Embends
- Ein Prozess - Mehrere Threads
- Mehrere Prozesse - Ein Thread
	-> Zugriff auf den Hauptspeicher erfolgt über [[../Komponenten/Message Passing Interface|Interprozesskommunikation]]
- Mehrere Prozesse - Mehrere Threads
	-> Aktuell
^1668884156679

## Varianten

### Kernel-Level

#### Zustände: #fc
- Der Kernel kennt die Zustände und aller Threads über die Thread-Tabelle und Thread Control Blocks
- Der Kernel (-Scheduler) kann bereite Threads individuell aktivieren
^1668884156681

#### Vorteile: #fc
- Blockierung von einzelnen Threads stellt kein Problem dar
- Threads können in (mehrere) Prozesse aufgeteilt werden
^1668884156683

#### Nachteile: #fc
- Kein benutzerdefiniertes Scheduling
- Overhead durch [[Prozesswechsel|Kontextwechsel]] und Management (Start, Umschalten, Terminierung)
	-> Werden durch eine Thread-Tabelle verwaltet
^1668884156685

### User-Level

#### Zustände: #fc
- Der User-Level-Scheduler kann Threads "aktivieren", da der Kernel sie gar nicht sehen kann
- Aktive Threads können nur ausführen, wenn der Prozess aktiv ist
- Ein blockierter Zustand blockiert den gesamten Prozess -> alle Unser-Level Threads
^1668884156686

#### Eigenschaften & Vorteile: #fc
- User-Level Threads werden durch Thread-Bibliotheken zur Laufzeit verwaltet
	-> Der Kernel weiß nicht von ihrer Existenz
- Scheduling ist benutzerdefiniert einstellbar
- Laufen auf jedem Betriebssystem
- Die Erzeugung ist aufgrund dessen, dass keine [[Prozesswechsel|Prozesswechsel]] notwendig sind, deutlich leichtgewichtiger
^1668884156688

#### Nachteile: #fc
- Threads können nicht auf verschiedene Ressourcen verteilt werden
- Blockierende Zustände blockieren alle Threads
^1668884156690

### Hybride Implementierungen

#### Multiplexing-Varianten: #fc
1. Mehrere *Pure User-Level* Threads bilden durch die Threads-Library auf einen OS-[[../Prozess|Prozess]] ab
2. *Pure Kernel-Level*: Je ein *User-Level Thread* bildet auf einen *Kernel-Level Thread* ab, die in einen Prozess existieren
3. *Combined*: $n$ *Unser-Level Threads* bilden gemeinsam auf $m\leqslant n$ viele *Kernel-Level Threads* ab, die wiederum auf einen Prozess abbilden
^1668884156692
