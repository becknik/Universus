---
tags: uni practical-cs syskon sync
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - Spin-Locks
  - Read-Modify-Write
  - RMW
linter-yaml-title-alias: Spin-Locks
date: 2022-12-03
mod-date: 2022-12-03
---

# Spin-Locks

## Annahmen: #fc
- Kommunikation über gemeinsame Variablen im Hauptspeicher
- Ein [[../Korrektheitskriterien|schwach fairer]] Scheduler
- [[../Sequenzielle Konsistenz|Sequenzielle Konsistenz]] beim Speicherzugriffen
	-> *Acquire/Release-Semantik* ist ausreichend
- Die [[../../Ro I/CPU/Befehlssatz Architektur|ISA]] bietet Instruktionen an, die die Ausführung von *Leseoperation*, *Modifikation* und *Schreiboperation* auf einer (primitiven) Variable (Speicher) ermöglicht
^1670104820552

## Funktionsweise: #fc
- Im *Präprotokoll* des [[Kritischer Abschnitt|kritischen Abschnitts]] sperrt genau ein [[../Betriebssystem/Prozess|Prozess]]
	-> `lock.aquire()`
- Nur der Prozess, der die Sperre hält, kann diese auch im *Postprotokoll* wieder aufheben (`lock.release()`)
	-> Unterschied zu [[Semaphore|Semaphoren]]
^1670086229729

## Vor- und Nachteile: #fc
- Auf eine beliebige Anzahl von [[../Betriebssystem/Prozesse/Threads|Threads]] anwendbar
- Sehr effizient bei geringer *Lock-Contention*
	-> Es findet kein Wechsel zwischen Kernel- und User-Mode statt
- Warten auf die Sperre erfolgt durch *Busy-Waiting*, was u.A. eine geringe Latenz auf Sperrung der Locks zur Folge hat
	-> Bei hoher Sperr-Konkurrenz (*Lock-Contention*) steigt der Aufwand
	-> Unterschied zu [[Semaphore|Semaphoren]]
- Bei [[../Korrektheitskriterien|nicht-fairen]] Scheduling (= bei Thread-Prioritäten) ist Aushungern möglich
	- Beispiel: Thread mit niedriger Priorität hindert einen Thread mit hoher Priorität an dem Betreten des *kritischen Abschnitts*
		-> *Bussy Waiting*/ *Spinning on Lock* bedeutet ausführungsbereit für das Betriebssystem
^1670088793640

## Aushungern bei Prioritäten-[[../Betriebssystem/Scheduling|Scheduling]]: #fc
- Annahmen: Threads T(hread)H(igh) & T(hread)L(ow); *quasi-parallele Ausführung*
1. TH ist im *nicht-kritischen* Abschnitt & führt I/O durch
	 -> TH $\to$ Blocked; TL $\to$ Ready
2. TL betritt *kritischen Abschnitt*
	 -> Keine Contention
3. TH wird nach beendeter I/O ausführungsbereit
	 -> [[../Betriebssystem/Scheduling|Scheduler]] unterbricht TL für TH
4. TH will den *kritischen Abschnitt* betreten und ist daher *spinning on Lock*
	 -> Das OS sieht TH als ständig ausführungsbereit
	 -> TL führt aufgrund der höheren Priorität von TH nicht aus
^1670089158172

## Varianten

### Test & Set: #fc
```
int test_and_set (int *i) {
	int oldvalue = *i;
	if (*i == 0) {*i = 1;}
	return oldvalue;
}
```
- Schwache Lösung von [[Kritischer Abschnitt|Critical Section Problem]]
	-> Aushungern möglich
^1670086229723

### Compare & Swap: #fc
- Atomare Ausführung ohne Unterbrechung notwendig
```
boolean cmpswp (int *i, int erwartet, int neu) {
	if (*i == erwartet) {
		*i = neu;
		return true;
	} else {
		return false;
	}
}
```
- Schwache Lösung von [[Kritischer Abschnitt|Critical Section Problem]]
	-> Aushungern möglich
^1670086235417

### Fetch & Add

#### Prinzip: #fc
- Atomare Ausführung ohne Unterbrechung notwendig
```
int fetchadd (int *i, int value) {
	int oldvalue = *i;
	*i = *i + value;
	return oldvalue;
}
```
^1670088793642

#### Ticket-Lock: #fc
-> Ähnlich zum [[Bakery-Algorithmus]]
1. Threads ziehen eine eindeutige, streng monoton steigende Nummer
2. Threads treten anhand der Ticket Nummer in den [[Kritischer Abschnitt|kritischen Abschnitt]] ein
^1670089433640
