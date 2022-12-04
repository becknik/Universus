---
tags: uni practical-cs syskon os
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - Scheduling
  - SPN
linter-yaml-title-alias: Scheduling
date: 2022-11-19
mod-date: 2022-11-25
---

# Scheduling
"And you have to realize that there are not very many things that aged as well as the scheduler. Which is just another proof that scheduling is easy"
	~ Linux Torvalds, The Linux Mailing List, Feb 2001

## Drei Ebenen: #fc
1. Langfristig: Bei der Zulassung von neuen Prozessen aus der *Entrance-Queue*
2. Mittelfristig: Scheduling zwischen den RAM und Speicher aufgrund von *ausgegangenen Ressourcen*
	 -> *Trashing*: Wenn der Grad der Multiprogrammierung die verfügbaren Ressourcen übersteigt und es durch Swapping zu zu vielen [[../../Ro I/Virtualisierung/Virtueller Speicher|Seitenfehlern]] kommt
3. Kurzfristig: Scheduling der aktiven, [[Prozesse/Prozesswechsel|wechselnden Prozessen]]
	 -> Wichtig für Nebenläufigkeit
^1668895130998

## Eigenschaften:
- Teilt die Rechenzeit in Zeitscheiben zwischen $10^{-4}$ und $10^{-5}$ Sekunden ein
- Je mehr Prozesse, desto effizienter die Ausnutzung von I/O

## Kurzfristig

### Wichtige Kriterien: #fc
- Schneller [[Prozesse/Prozesswechsel|Kontextwechsel]]
- Schnelle Entscheidung in der Auswahl des [[Prozess|Prozesses]]
^1668895131006

### Eigenschaften: #fc
- Hier wendet für verschiedenen [[../Hardware/Systemarchitekturen|Systemarchitekturen]] unterschiedliche Verfahren an
- *CPU-Burst*: Anzahl der Prozessorbefehle in Serie, bis I/O notwendig
	-> Ausführung eines Programmes kann *Prozessorlastig* oder *I/O-lastig* sein
^1668895131008

### Leistungskriterien (5): #fc
- *Auslastung*: Der Prozessor soll möglichst immer beschäftigt sein
- *Durchsatz*: Möglichst hohe Zahl der erledigten Tasks pro Zeiteinheit
- *Antwortzeit*: Niedrige Zeit für die Ausführung und das Warten im *Ready*-Zustand
	-> Um Antwortzeiten zu erfüllen, muss man auch auf Fairness acht geben
	-> Interessant für Echtzeit-Systeme
- *Durchlaufzeit*: Zeit eine bestimmten Prozess inklusive I/O auszuführen
	-> Für Datenbank-Systeme interessant
- *Fairness*: Jeder Prozess macht Fortschritte
	-> Wichtig für die [[../Korrektheitskriterien|Lebendigkeitseigenschaft]]
^1668895131010

## Varianten
- [[Scheduling/Uniprozessoren-Scheduling|Uniprozessoren-Scheduling]]
- [[Scheduling/Multiprozessoren-Scheduling|Multiprozessoren-Scheduling]]

### Realtime

### Eigenschaften: #fc
-> Siehe [[OS-Echtzeitfähigkeit|Echtzeitfähigkeit]]
- Beim Hinzufügen eines neuen Prozesses wird überprüft, ob das System Ressourcen-technisch mit der Einhaltung der Deadline hinterher kommt
^1668895131026
