---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Systemarchitekturen
  - quasi-parallel
linter-yaml-title-alias: Systemarchitekturen
date-of-creation: 2022-10-24
mod-date: 2022-11-10
---

# Systemarchitekturen

## Einzelkernprozessoren
- Es kann höchstens eine Instruktion zu jedem Zeitpunkt ausgeführt werden
- Quasi-Parallelität durch Multitasking bei Warten auf Interrupts oder I/O
	→ Trägt zur erhöhten Ausnutzung des Prozessorkerns bei

### Ausführung von [[Nebenläufige Programme|nebenläufigen Programmen]] #fc
- Sei $\Pi=\{p,q\},p=\{p_1,\dots,p_{n(p)}\},q=\{q_1,\dots,q_{n(q}\}$, dann verläuft die Ausführung von $\Pi$ mit Unterbrechungen durch das Betriebssystem $o=\{o_1,\dots,o_{n(o)}\}$:
$$\text{Systemsicht: }p_1,\dots,p_j\mid o_1,\dots,o_k\mid q_1,\dots,q_l\mid o_{k+1},\dots,o_m\mid p_{j+1},\dots,p_n$$
^1667816585177

## Mehrkernprozessoren
- Alle Kerne greifen auf einen gemeinsamen Speicher zu
- Echtere Parallelität kann durch Multi-Tasking auf jedem Kern stattfinden

### Speicher-Ressourcen #fc
- *Lokal*: [[../../Ro I/Cache|Cache]] und lokaler Speicher
	→ Dienen der effizienten Ausführung des Prozesses (→ [[../../Ro I/Performanz/Out-Of-Order Issue|Out-Of-Order Issue]])
	- Lokaler Speicher: Hier leben nicht geteilte Variablen
		→ Werden von [[Memory Protection Units]] zugesichert
		→ [[../../Ro I/Aktuelles/Shared Memory|NUMA]]
- *Gemeinsame Ressourcen*: [[../../Ro I/Aktuelles/Shared Memory|Shared Memory]]
	→ Aktualisierung des gemeinsamen Zustands
^1667816775288

#### Cache Coherence #fc
- Bei Schreib-Zugriff auf zwischen Threads geteilte Speicheradressen treten Hardwaresperren ein
	→ Der Memory Bus blockiert durch ein *Cache-Coherence Protokoll*
^1667830091499

## Multiprozessor-Systeme
- Mehrere Prozessoren (mit mehreren Kernen) arbeiten zusammen
- Jeder Prozessor hat seinen eigenen Speicher
- Häufig existiert ein globaler Speicher, den alle Prozessoren nutzen

## Verteilte Systeme
→ [[Verteilte Systeme|Verteilte Systeme]]
