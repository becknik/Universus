---
tags: uni practical-cs syskon sync
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Spin-Locks
  - Read-Modify-Write
  - RMW
  - Ticket-Locks
linter-yaml-title-alias: Spin-Locks
date-of-creation: 2022-12-03
mod-date: 2023-01-04
---

# Spin-Locks

## Voraussetzungen #fc
- [[../Synchronisation/Sequenzielle Konsistenz|Sequenzielle Konsistenz]] beim Speicherzugriffen
	→ *Acquire/Release-Semantik* ist ausreichend
- Die [[../../Ro I/CPU/Befehlssatz Architektur|ISA]] bietet Instruktionen an, die die
	→ Ausführung von *Lese-*, *Schreiboperation* und *Modifikation* auf speziellen primitiven Variablen in einem atomaren Schritt
- Ein [[../Korrektheitskriterien|schwach fairer]] Scheduler
^1670104820552

## Funktionsweise #fc
- Im *Präprotokoll* des [[../Kritischer Abschnitt|kritischen Abschnitts]] verhängt genau ein [[../Betriebssystem/Prozesse/Threads|Thread]] eine *Sperre* (`lock.aquire()`)
	→ Nur genau ein Thread kann die Sperre halten
- Der sperrende Thread gibt die Sperre im *Postprotokoll* wieder frei (`lock.release()`)
	→ Die übrigen Threads warten "*spinning*" per Bussy-Waiting
	→ Unterschied zu [[Semaphore|Generelles Semaphor]]: Nur ein Thread kann die Sperre wieder freigeben
^1670086229729

## Vorteile #fc
- Auf eine beliebige Anzahl von [[../Betriebssystem/Prozesse/Threads|Threads]] anwendbar
- Einfach zu verifizieren
- Sehr effizient bei geringer *Lock-Contention* (= Sperrkonkurrent)
- Es findet kein Wechsel zwischen Kernel- und User-Mode statt
- Bieten eine geringe Latenz zum KA-Eintritt
^1672790400004

## Nachteile #fc
- Bei hoher *Lock-Contention* steigt der Aufwand aufgrund von *Busy-Waiting*
- Bei [[../Korrektheitskriterien|nicht-fairen]] Scheduling (= bei Thread-Prioritäten) ist Aushungern von Threads möglich
^1670088793640

## Varianten

### Test & Set #fc
```
int test_and_set (int *i) {
	int oldvalue = *i;
	if (*i == 0) {*i = 1;}
	return oldvalue;
}
```
- Schwache Lösung von [[../Kritischer Abschnitt|Critical Section Problem]]
	→ Aushungern eines [[../Betriebssystem/Prozesse/Threads|Threads]], der immer zur falschen Zeitpunkt reserviert, möglich
^1670086229723

### Compare & Swap #fc
```
bool cmpswp (int *i, int erwartet, int neu) {
--- Atomare Ausführung
	if (*i == erwartet) {
		*i = neu;
		return 1;
	} else {
		return 0;
	}
}
```
- Schwache Lösung von [[../Kritischer Abschnitt|Critical Section Problem]]
	→ Aushungern eines [[../Betriebssystem/Prozesse/Threads|Threads]], der immer zur falschen Zeitpunkt reserviert, möglich
^1670086235417

### Fetch & Add #fc
```
int fetchadd (int *i, int value) {
--- Atomare Ausführung
	int oldvalue = *i;
	*i += value;
	return oldvalue;
}
```
^1670088793642

## Implementierung von Ticket-Locks #fc
→ Ähneln den [[Bakery-Algorithmus]]
1. Threads ziehen eine eindeutige, streng monoton steigende Nummer
	 → Das Ziehen von Nummern kann durch keinen anderen Thread dauerhaft verhindert werden
2. Threads treten *in Reihenfolge der Ticket Nummer* in den [[../Kritischer Abschnitt|kritischen Abschnitt]] ein
^1670089433640

## Aushungern bei Prioritäten-[[../Betriebssystem/Scheduling|Scheduling]] #fc
- Annahmen: Threads T(hread)H(igh) & T(hread)L(ow); *quasi-parallele Ausführung*
1. TH ist im *nicht-kritischen* Abschnitt & führt I/O durch
	 → TH $\to$ Blocked; TL $\to$ Ready
2. TL betritt *kritischen Abschnitt*
	 → Keine Contention
3. TH wird nach beendeter I/O ausführungsbereit
	 → [[../Betriebssystem/Scheduling|Scheduler]] unterbricht TL für TH
4. TH will den *kritischen Abschnitt* betreten und ist daher *spinning on Lock*
	 → Das OS sieht TH als ständig ausführungsbereit
	 → TL führt aufgrund der höheren Priorität von TH nicht aus
^1670089158172
