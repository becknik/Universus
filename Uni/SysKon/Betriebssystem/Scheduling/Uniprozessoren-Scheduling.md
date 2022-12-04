---
tags: uni practical-cs syskon os scheduling
cards-deck: Uni::Courses::SysKon
complete: true
aliases: Uniprozessoren-Scheduling
linter-yaml-title-alias: Uniprozessoren-Scheduling
date: 2022-11-25
mod-date: 2022-11-26
---

# Uniprozessoren-Scheduling
-> [[../Scheduling|Scheduling]]

## Nicht-Präemptiv #fc
- Ein aktiver Prozess bekommt so lange CPU-Zeit, bis er sich unterbricht oder terminiert
	-> Häufig bei Batch-Systemen im Einsatz
- Soll eine möglichst hohe Prozessorauslastung und eine kurze durchschnittliche Antwortzeit erzielen
	-> Quese sollen möglichst kurz gehalten werden
- Möglichkeit des *Aushungerns* von Prozessen mit *niedriger Priorität*
	-> Triviales Beispiel: Ein unendlich laufenden Programmen (*CPU-Burst*) ohne natürliche [[Unterbrechungen|Interrupts]]
	-> [[../../Korrektheitskriterien|Lebendigkeit]] benötigt immer Fairness
^1668895131016

### Queues: #fc
- Entnahme entsprechend der Einfüge-Reihenfolge/ der längsten Wartezeit
	-> *Konvoy-Effekt*: Prozesse mit langen CPU-Burst halten kürzere Prozesse auf
	-> Ungünstig für den Durchsatz
^1668895131017

### Shortest Process Next: #fc
- Der Prozess mit der kürzesten *CPU-Burst* wird als nächstes ausgeführt
	-> Maximiert den Durchsatz
	-> Optimal unter den nicht-präemptives Uniprozessor-Scheduling
- *Abschätzung* des *CPU-Bursts* bei Blockierung des Prozesses durch $\Pi($*Ausführungshistorie*$)$ mit exponentiell geglätteten Mittelwert: $$B_{i+1}=\alpha B_i+(1-\alpha)B_\text{aktuell},\alpha\in[0,1]$$
	-> Der Einfluss der letzten Ausführungen nimmt exponentiell ab
	-> Effizient zu berechnen und zu speichern
^1668895131019

## Präemptiv #fc
- Ein aktiver Prozess kann und wird unterbrochen, auch wenn er noch bereit ist
	-> Wird für interaktive Anwendungen benötigt
- Jeder Prozess soll eine ausreichend gute Antwortzeit haben
- Stellt die [[../../Korrektheitskriterien|Fairness]] bei der Ausführung sicher
^1668895131021

### Round Robin: #fc
- Jeder Prozess erhält eine *Zeitscheibe* der Prozessorzeit
	-> Ohne [[Unterbrechungen|Interrupts]] ist der Anteil der Gesamtprozessorzeit gleich verteilt
- [[../../Korrektheitskriterien|Faires Scheduling]] ohne harte Deadlines
- Länge des Zeitquantums entscheidet über den Aufwand durch entstehende [[Prozesse/Prozesswechsel|Kontextwechsel]]
	-> In der Praxis werden Zeitscheiben zwischen $10^{-4}-10^{-5}$ Sekunden gewählt
^1668895131023

### Aging: #fc
- Es existieren mehrere *Ready-[[../../../DSA/Datenstrukturen/Queue|Queues]]*, von denen Prozessen aus den unteren Queues *größere Zeit-Quanten* zugewiesen werden
	-> Prozesse mit hoher *CPU-Burst* oder Prozesse mit *geringer Priorität* wandern in der Queue-Struktur weiter nach unten
- Uhren-[[Unterbrechungen|UBRs]] werden sensitiv zu dem *Ready-Queue-Level* eingestellt
	-> Wenn die erste *Ready-Queue* eine geringe Zeitscheibe hat, ermöglicht die Einteilung eine Annäherung an das *Shortest Process Next* Auswahlverfahren
^1668895131012

### Statische Prioritäten: #fc
- Verschiedene *Ready-Queues* für Klassen von Prioritätenbereichen
	-> Prozesse mit höheren Prioritäten unterbrechen/ laufen vor Prozessen mit niedriger Priorität
- Alle als User gestarteten Programme laufen unter UNIX in der Priorität 0
  -> Bei der Festlegung der Priorität im Quellcode sollte ein Wert unter den OS-Diensten gewählt werden
- Die *Schedule-Policy* (=Bewertungsfunktion) definiert die Prozess-Position innerhalb der Warteschlange
	-> *Niceness* bei UNIX-Systemen: Wie viel [[../../../Ro I/Performanz/CPU-Time|CPU-Time]] ein Prozess gerne freiwillig abgibt
	-> Im nicht-privilegierten Modus lässt sich nur Niceness abgeben, die Fairness kann also so nur besser verteilt werden
	-> Beispiele: [[../../../DSA/Datenstrukturen/Queue|FIFO]], *Round-Robin*
^1668895131014

#### Eigenschaften:
- Es existiert eine Policy für [[../OS-Echtzeitfähigkeit|Echtzeitfähigkeit]], die wird aber in der Praxis nicht benutzt
