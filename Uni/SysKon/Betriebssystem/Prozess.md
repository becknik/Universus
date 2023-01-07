---
tags: uni practical-cs syskon os
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Prozess
  - Prozesszustand
linter-yaml-title-alias: Prozess
date-of-creation: 2022-10-28
mod-date: 2023-01-02
---

# Prozess

## Definition: #fc
- Ein Prozess besteht aus einem Tupel $(P,Z)$
	- $P=\{p_1,p_2,\dots,p_n\}:$ Eine Zerlegung des Programmtextes (Text-Segments) in *atomare Befehle*
	- $Z=\{z_1,z_2,\dots,z_m\}:$ Eine Menge von *Kontroll- und Zustandsinformationen*
		 → [[../../../Ro I/OS & Environment/Speicherorganisation|Programmdaten]] im Speicher und Ausführungskontext in den [[../../../Ro I/RISC-V/Register|Registern]]
		 → [[Prozesse/Prozesskontrollblock|Prozessabbild]], [[../../../Ro I/Virtualisierung/Virtueller Speicher|Virtueller Speicher]]
- Sei $c_p=p_i$ der in einer Ausführung als nächstes ausführbare Befehl definiert
	→ [[../../../Ro I/RISC-V/Problem Counter|Problem Counter]]
^1667058688569

## 7-Zustände-Modell: #fc
- *Neu*: Der Prozess ist bekannt, aber noch nicht gestartet
- *Bereit*: Nach einer Prozess-Zulassung, eines Blocks oder einem *Präemptions-Timeouts*
- *Aktiv*: Der Prozess bekommt [[../../../Ro I/Performanz/CPU-Time|CPU-Time]]
- *Blockiert*: Warten auf Ergebnisse wie I/O, Freigabe einer Sperre, etc.
	→ Mehrere *Blocked-Queues* für unterschiedliche Ereignis-Klassen
- *Suspendiert*: Auslagerung des Prozesses in den *Swap-Speicher*
	→ Man unterscheidet zwischen *bereit-suspendiert* und *blockiert-suspendiert* (+1)
	→ Durch Suspendieren ist die [[../Korrektheitskriterien|Fairness]] nicht mehr erfüllt
	→ Die [[../../../Ro I/Virtualisierung/Virtueller Speicher|virtuellere Speicherverwaltung]] ermöglicht eine Auslagerung von Speicherseiten
- *Terminiert*: Es folgen Aufräumen & Abrechnen
	- *Zombie*: Terminierter Prozess, dessen Exit-Code noch Relevanz für den Elternprozess besitzt/ noch nicht vom Eltern-Prozess abgefragt wurde
		→ "Wenn ein Kind stirbt, welchen Exit-Code hat es?" ~ Frank Dürr
		→ Exit-Code: `echo $`
^1668685376955

## Erstellung (5) #fc
1. Weise dem Prozess wird eine neue *PID* zu
	 → Die Identität wird im in der Prozessliste verwaltet
2. Allokiere Speicher für den Prozess
3. Initialisiere [[Prozesse/Prozesskontrollblock|PCB]]
4. Verlinke den Prozess mit dem [[../OS|OS]]
	→ Zum Beispiel durch die Einordnung in die Ready-Queue
5. Erstelle & erweitere *OS-Verwaltungsstrukturen*
^1668880398096

## Start #fc
- Ein Prozess wird immer von einem anderen Prozess gestartet
- POSIX `fork()` erstellt einen Kind-Prozess aus einer fast exakten "Kopie" des Eltern-Prozesses
	→ Unterschiedliche *PID*, gleiche *offenen Dateien*
	→ Ausführung des Eltern-Programms wird nach Terminierung des Kind-Prozesses fortgesetzt
- `clone()` entspricht `fork()` mit *präziser Kontroller* über Daten, die zwischen Kind- und Eltern-Prozess geteilt werden
	→ "Linux Torvalds skaliert nicht, denn er kann sich nicht klonen"
- `exec()` ersetzt das aktuelle Prozessabbild durch ein neues Programm
	→ Welches Programm ausgeführt wird, wird über einen Parameter-String spezifiziert
^1668880415898

## Eigenschaften: #fc
- Mehrere Prozesse können sich Ressourcen teilen
	→ z.B. über gemeinsame Speicherbereiche
- Der Zustand auf gemeinsamen Speicher ist durch die Reihenfolge der Zugriffe definiert
	→ Die Zugriffsordnung ist innerhalb eines Prozesses eindeutig durch die Sequenz atomarer Operationen definiert
	→ Der Speicher stellt die Atomizität von (parallelen) Operationen auf Mehrprozessorsystemen sicher
- Prozesse kümmern sich nicht selbst um das Management der Systemressourcen
	→ Das macht das [[../OS|OS]] selber
^1667058688578
