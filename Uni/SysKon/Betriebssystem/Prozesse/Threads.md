---
tags: uni practical-cs syskon os parallel threads
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Threads
  - Thread Contol Block
  - TCB
linter-yaml-title-alias: Threads
date-of-creation: 2022-11-19
mod-date: 2023-01-02
---

# Threads

## Charakteristika (3) #fc
- Ausführungszustand & Kontext
- Zustand im Thread Control Block *TCB*
	→ Verwaltungseinheiten für den [[../Scheduling|Scheduler]]
- Ein eigener [[../../../Ro I/OS & Environment/Stack|Stack]] für Thread-Variablen und lokale Funktionsaufrufe
- Zugriff auf gemeinsame Ressourcen über den virtuellen Adressraum/ Speicher des [[../Prozess|Prozesses]]
^1668884128907

## Vorteile (4) #fc
- Kommunikation über geteilten lokalen Variablen
	→ Keine [[../Funktionen/Message Passing Interface#Interprozesskommunikation|Interprozesskommunikation]] über OS-Kernel [[Prozesswechsel|Kontextwechsel]], mehrfachen Kopieren von Daten
- I/O und Berechnungen überlappen sich
- Echt-parallele Ausführung auf Multiprozessoren
- Minimierung des Zeitaufwands bei Erstellen, Terminierung und Abwechseln von Threads innerhalb eines Programms
^1668884128909

## Alternative Implementierungen

### [[../../OS|Ring-3]]

#### Eigenschaften & Vorteile #fc
- User-Level Threads werden durch Thread-Bibliotheken zur Laufzeit verwaltet
	→ Der Kernel weiß nicht von ihrer Existenz
	→ Aktive Threads können nur ausführen, wenn der Prozess aktiv ist
- Scheduling der Threads ist benutzerdefiniert einstellbar
	→ Der Prozess hält die Thread-Tabelle mit allen *TCBs*, die durch den [[../../OS|Ring-3]]-[[../Scheduling|Scheduler]] verwaltet werden
- Laufen unabhängig des [[../../OS|OS']]
- Erzeugung ist leichtgewichtiger
	→ Keine [[Prozesswechsel|Kontextwechsel]] nötig
^1668884156688

#### Nachteile #fc
- Threads können nicht auf verschiedene Ressourcen *& Prozessoren* verteilt werden
- Aktive Threads können nur ausführen, wenn der Prozess aktiv ist
- Ein blockierender Zustand (z.B. [[../Funktionen/System Calls|SysCall]]) in einem User-Level-Thread blockiert den kompletten Prozess mit allen anderen User-Level-Threads
^1668884156690

### [[../../OS|Ring-0]]

#### Eigenschaften & Vorteile #fc
- Der Kernel kennt die Zustände und aller Threads über die Thread-Tabelle und *TCBs*
	→ Der [[../Scheduling|Scheduler]] kann an Zustände angepasstest Scheduling vornehmen & auf mehrere Prozessoren verteilen
- Die Blockierung von einzelnen Threads stellt kein [[../../Korrektheitskriterien|Fairness]]-Problem dar
^1668884156683

#### Nachteile #fc
- Kein benutzerdefiniertes Scheduling möglich
- Overhead durch [[Prozesswechsel|Kontextwechsel]] und Kernel-Management (=Start, Umschalten, Terminierung)
^1668884156685

## Hybride Implementierungen

### Multiplexing-Varianten (3) #fc
→ Kombination von Vorteilen der [[#Alternative Implementierungen]]
1. Mehrere *Pure User-Level* Threads bilden durch die Threads-Library auf einen OS-Kontext-[[../Prozess|Prozess]] ab
2. *Pure Kernel-Level*: Je ein *User-Level Thread* bildet auf einen *Kernel-Level Thread* ab, die in einen Kontext-Prozess existieren
3. *Combined*: $n$ *Unser-Level Threads* bilden gemeinsam auf $m\leqslant n$ viele *Kernel-Level Threads* ab, die wiederum auf einen Kontext-Prozess abbilden
^1668884156692

### Beispiele

#### Windows #fc
- Ein *Job* entspricht einem Batch von Prozessen
- Ein Prozess beinhaltet $1\leq$ [[../../OS|Ring-0]]-Threads
- Ein Ring-0-Thread beinhaltet $1\leq$ *Fibers* ([[../../OS|Ring-3]]-Threads)
^1672696395963

#### Solaris #fc
→ [[#Multiplexing-Varianten (3) fc|Combined Multiplexing Type Threads]]
- Ein Prozess wird vom einem oder mehreren [[../../OS|Ring-0]]-Threads zugeordnet
- Ein [[../../OS|Ring-0]]-Thread entspricht einem *Lightweight Thread*
- Einer Menge von $|$*Lightweight Threads*$|=n$ werden $n\leq m$ [[../../OS|Ring-3]]-Threads zugeordnet
^1672696395966

## Verhältnis Thread - Prozess
- Ein Prozess - Ein Thread
	→ Embends
- Ein Prozess - Mehrere Threads
- Mehrere Prozesse - Ein Thread
	→ Zugriff auf den Hauptspeicher erfolgt über [[../Funktionen/Message Passing Interface|Interprozesskommunikation]]
- Mehrere Prozesse - Mehrere Threads
	→ Aktuell
