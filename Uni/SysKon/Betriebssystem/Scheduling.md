---
tags: uni practical-cs syskon os
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Scheduling
linter-yaml-title-alias: Scheduling
date-of-creation: 2022-11-19
mod-date: 2023-01-03
---

# Scheduling
→ [[Scheduling/Uniprozessoren-Scheduling|Uniprozessoren-Scheduling]], [[Scheduling/Multiprozessor-Scheduling|Multiprozessoren-Scheduling]]
"And you have to realize that there are not very many things that aged as well as the scheduler. Which is just another proof that scheduling is easy"
	~ Linux Torvalds, The Linux Mailing List, Feb 2001

## Ebenen (3) #fc
→ [[Prozess#7-Zustände-Modell: fc|7-Zustände-Modell]]
1. Langfristig: Bei der Zulassung von *neuen* Prozessen aus der *Entrance-Queue*
2. Mittelfristig: Scheduling zwischen den RAM und Speicher aufgrund von *ausgegangenen Ressourcen*
	→ Die Ausnutzung des verfügbaren I/Os & CPU-Utilization wächst mit der Zahl der laufenden Prozesse
	 → *Trashing*: Wenn der Grad der Multiprogrammierung die verfügbaren Ressourcen übersteigt und es durch Swapping zu zu vielen [[../../Ro I/Virtualisierung/Virtueller Speicher|Seitenfehlern]] kommt
3. Kurzfristig: Scheduling der aktiven, [[Prozesse/Prozesswechsel|wechselnden Prozessen]]
	 → Unterschiedliche Verfahren für [[Scheduling/Uniprozessoren-Scheduling|Uniprozessoren]], [[Scheduling/Multiprozessor-Scheduling|Multiprozessoren]] & Echtzeitsysteme
	 → Wichtig für [[../Nebenläufigkeit|Nebenläufigkeit]]
^1668895130998

### Zustandsübergänge #fc
→ [[Prozess#7-Zustände-Modell: fc|7-Zustände-Modell]]
- *Kurzfristig*:
	- $\fbox{Active}\leftrightarrow\fbox{Ready}$
	- $\fbox{Active}\to\fbox{Blocked}$
	- $\fbox{Blocked}\to\fbox{Ready}$
	- $\fbox{Blocked/Suspended}\to\fbox{Ready/Suspended}$
- *Mittelfristig*:
	- $\fbox{Active}\to\fbox{Ready/Suspended}$
	- $\fbox{Ready}\leftrightarrow\fbox{Ready/Suspended}$
	- $\fbox{Blocked}\leftrightarrow\fbox{Blocked/Suspended}$
- *Langfristig*:
	- $\fbox{Ready/Suspended}$
	- $\fbox{Ready}$
^1672684307337

## Leistungskriterien (5) #fc
- *Auslastung*: Der Prozessor soll möglichst *immer beschäftigt* sein
- *Durchsatz*: Möglichst hohe Zahl der *erledigten Tasks pro Zeiteinheit*
- *Antwortzeit*: Niedrige Zeit für die Ausführung und das Warten im *Ready*-Zustand
	→ Um Antwortzeiten zu erfüllen, muss man auch auf Fairness acht geben
	→ Interessant für [[Echtzeitfähigkeit|Echtzeit]]-Systeme
- *Durchlaufzeit*: Geringe Durchlaufzeit eines Prozesses (inklusive I/O)
	→ Für Datenbank-Systeme interessant
- *Fairness*: Jeder Prozess macht Fortschritte
	→ Wichtig für die [[../Korrektheitskriterien|Lebendigkeitseigenschaft]]
^1668895131010

## Eigenschaften
- Teilt die Rechenzeit in Zeitscheiben zwischen $10^{-4}$ und $10^{-5}$ Sekunden ein
- Je mehr Prozesse, desto effizienter die Ausnutzung von I/O

## Kurzfristige Scheduling-[[#Ebenen (3) fc|Ebene]]

### Wichtige Kriterien #fc
- Schneller [[Prozesse/Prozesswechsel|Kontextwechsel]]
- Schnelle Entscheidung in der Auswahl des nächsten [[Prozess|Prozesses]]
^1668895131006

### Eigenschaften #fc
- Verschiedenen [[../Systemarchitekturen|Systemarchitekturen]] für unterschiedliche Verfahren:
	- [[Scheduling/Uniprozessoren-Scheduling|Uniprozessoren-Scheduling]]
	- [[Scheduling/Multiprozessor-Scheduling|Multiprozessoren-Scheduling]]
- *CPU-Burst*: Anzahl der Prozessorbefehle in Serie, bis I/O notwendig
	→ Ausführung eines Programmes kann *Prozessorlastig* oder *I/O-lastig* sein
^1668895131008

### Kriterien für [[Echtzeitfähigkeit|Echtzeitfähigkeit]] (1) #fc
- Beim Hinzufügen eines neuen Prozesses wird überprüft, ob das System Ressourcen-technisch mit der Einhaltung der Deadline hinterher kommt
^1668895131026
