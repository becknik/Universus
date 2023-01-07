---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Producer-Consumer
linter-yaml-title-alias: Producer-Consumer
date-of-creation: 2023-01-04
mod-date: 2023-01-04
---

# Producer-Consumer

## Korrektheitskriterien
- [[../../Atomizität]] beim Einfügen und Auslesen aus dem Puffer
- Kein Pufferüberlauf
- Keine Verklemmung/ kein Aushungern

## Prinzip #fc
- Zwei Aufgaben, die nacheinander ablaufen müssen, werden entkoppelt
	→ Die Tasks müssen unabhängig voneinander parallelisiert werden können
- Aufgliederung der Aufgaben in einen Daten erzeugenden $\fbox{Produzenten}$ und einen empfangenden & verarbeitenden $\fbox{Konsumenten}$
- Die [[../../Betriebssystem/Prozess|Prozesse]] "pipen" (`append()`, `consume()`) über einen *Puffer*
	→ Der Konsument kann ggf. selber entscheiden, welche Task er beim Empfang eines Datums anwendet
^1666630152014

## Lösung

### [[Semaphore|Semaphor]] #fc
- Verwenden von zwei *generellen Semaphoren* für die Puffergröße
	- Ein Semaphor `notFull`$\leftarrow(N,\emptyset)$ zeigt für die Produzenten an, wie viele Elemente noch in den Puffer passen
		→ Produzenten signalisieren Einfügen über `notEmpty.signal()`
	- Ein Semaphor `notEmpty`$\leftarrow(0,\emptyset)$ zeigt für die Konsumenten an, wie viele Daten sich im Puffer befinden
		→ Konsumenten signalisieren Entfernen über `notFull.signal()`
- Wenn `notFull.value > 1 || notEmpty.value > 1` lassen die Semaphore mehrere Produzenten `||` Konsumenten gleichzeitig passieren
- Verwenden von einem *binären Semaphor* für den [[../../Betriebssystem/Prozesse/Threads|Thread]]-sicheren Zugriff auf den Puffer-Speicher in dessen [[../../Kritischer Abschnitt|KA]]
^1672844600329
