---
tags: uni practical-cs syskon os scheduling
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Uniprozessoren-Scheduling
  - SPN
  - Round Robin
  - Aging
  - Multi Level Feedback Queue
  - Priority Scheduling
linter-yaml-title-alias: Uniprozessoren-Scheduling
date-of-creation: 2022-11-25
mod-date: 2023-01-07
---

# Uniprozessoren-Scheduling
→ [[../Scheduling|Scheduling]]

## Nicht-Präemptiv

### Prinzip #fc
- Ein aktiver [[../Prozess|Prozess]] bekommt so lange CPU-Zeit, bis er sich [[../Unterbrechungen|unterbrochen wird]] oder terminiert (→ Batch-Systeme)
- Durch kurz-Haltung der Queues soll eine möglichst *hohe Prozessorauslastung* und eine *kurze durchschnittliche Antwortzeit* erzielen
	→ [[../Scheduling#Leistungskriterien (5) fc|Leistungskriterien]]
- Ermöglicht des *Aushungerns* von Prozessen mit *niedriger Priorität*
	→ Triviales Beispiel: Ein unendlich laufenden Programmen (*CPU-Burst*) ohne natürliche [[Unterbrechungen|Interrupts]]
	→ [[../../Korrektheitskriterien|Lebendigkeitseigenschaft]] benötigt immer *Fairness*, die hier nicht erfüllt wird
^1673100594739

### Verfahren

#### FIFO
→ Optimiert die [[../Scheduling#Leistungskriterien (5) fc|Auslastung]]
- Entnehme $P_\text{next}$ entsprechend der längsten Wartezeit in der Queue/ Ringpuffer
	→ Geringer Aufwand für den Scheduler
- *Konvoy-Effekt*: "Langsame" Prozesse mit langen CPU-Burst halten kürzere "schnellere" Prozesse auf
	→ Ungünstig für den [[../Scheduling#Leistungskriterien (5) fc|Durchsatz]]

#### Shortest Process Next (SPN) #fc
- Der Prozess mit der kürzesten *CPU-Burst* wird als nächstes ausgeführt
	→ Maximiert den [[../Scheduling#Leistungskriterien (5) fc|Durchsatz]] bei minimaler *durchschnittlicher Antwortzeit*
- Optimal für "nicht-präemptives Uniprozessor-Scheduling"
- Realisiert durch [[../../../DSA/Bäume/Heap|Min-Heaps]] und Approximation der CPU-Burst-Zeit
	- *Abschätzung* des *CPU-Bursts* bei Blockierung des Prozesses durch $\Pi(\text{Ausführungshistorie})$ mit exponentiell geglätteten Mittelwert: $$B_{i+1}=\alpha B_i+(1-\alpha)B_\text{act},\quad\alpha\in[0,1]$$
		→ $B_\text{act}$: CPU-Burst der letzten Ausführung
		→ Der Einfluss der letzten Ausführungen nimmt exponentiell ab
		→ Effizient zu berechnen und speichern
^1673100594747

## Präemptiv

### Prinzip
- Ein aktiver Prozess wird unterbrochen, auch wenn er noch bereit ist
	→ Wird für interaktive Anwendungen benötigt
- Jeder Prozess soll eine ausreichend gute Antwortzeit haben
- Stellt die [[../../Korrektheitskriterien|Fairness]] bei der Ausführung sicher

### Round Robin #fc
- Verhält sich wie [[#Nicht-Präemptiv#FIFO fc|FIFO]] mit einer maximalen Zeit
- Jeder Prozess erhält eine identische *Zeitscheibe* der Prozessorzeit, wenn man I/O-[[Unterbrechungen|Interrupts]] außer acht lässt
	→ [[../../Korrektheitskriterien|Faires Scheduling]] ohne harte Zeitschranken #TODO
- Länge des Zeitquantums entscheidet über den Aufwand durch entstehende [[Prozesse/Prozesswechsel|Kontextwechsel]]
	→ In der Praxis werden Zeitscheiben zwischen $10^{-4}-10^{-5}$ Sekunden gewählt
^1673100594750

### Aging (Multi Level Feedback Queue) #fc
- Es existieren mehrere *Ready-[[../../../DSA/Datenstrukturen/Queue|Queues]]*, von denen Prozessen aus den unteren Queues *größere Zeit-Quanten* zugewiesen werden
	→ Ermöglicht eine präemptive Annäherung an den [[#Nicht-Präemptiv#Shortest Process Next (SPN) fc|SPN]]
	→ Prozesse mit hoher *CPU-Burst* wandern in der Queue-Struktur weiter nach unten
^1673100594753

### Statische Prioritäten #fc
- Verschiedene *Ready-Queues* für Klassen von Prioritätenbereichen
	→ Prozesse mit höheren Prioritäten unterbrechen bzw. laufen vor Prozessen mit niedriger Priorität
- Die Zeitquanten in den unteren Queues werden niedriger
- Die *Schedule-Policy* (=Bewertungsfunktion) definiert die Prozess-Position innerhalb der *Ready-Queue*
	→ Beispiele: [[#Nicht-Präemptiv#FIFO fc|FIFO]], [[#Round Robin fc|Round-Robin]]
^1673100594755

#### Eigenschaften #fc
- Alle [[../../OS|Ring-3]] Programme laufen nach der Zulassung (unter UNIX) in der Priorität 0
	→ Priorität 0 ist die niedrigste Unix-Priorität
	→ Bei der Festlegung der Priorität im Quellcode sollte ein Wert unter den OS-Diensten gewählt werden
- Unter der *Scheduling-Policy* `SCHED_OTHER` hat der Niceness-Wert des Prozesses Einfluss auf die dynamisch vergebene [[../../../Ro I/Performanz/CPU-Time|CPU-Time]]:
	- *Niceness* bei UNIX-Systemen: Wie viel [[../../../Ro I/Performanz/CPU-Time|CPU-Time]] ein Prozess gerne freiwillig abgibt
		→ Im nicht-privilegierten Modus lässt sich nur Niceness abgeben, die Fairness kann also so nur besser verteilt werden
^1673100594759

## Beispiele #fc
| Prozess | Ankunftszeit | Prozessorzeit |
| ------- | ------------ | ------------- |
| A       | 0            | 3             |
| B       | 2            | 6             |
| C       | 4            | 4             |
| D       | 6            | 5             |
| E       | 8            | 2             |
- FIFO:
$$\displaylines{\fbox{1}\fbox{2}\fbox{3}\fbox{4}\fbox{5}\fbox{6}\fbox{7}\fbox{8}\fbox{9}\fbox{10}\fbox{11}\fbox{12}\fbox{13}\fbox{14}\fbox{15}\fbox{16}\fbox{17}\fbox{18}\fbox{19}\fbox{20}\\
\fbox{A\quad\quad}\fbox{B\quad\quad\quad\qquad}\fbox{C\quad\quad\quad\qquad}\fbox{D\qquad\qquad\qquad}\fbox{E\qquad}}$$
- Shortest Process Next (SPN):
$$\displaylines{\fbox{1}\fbox{2}\fbox{3}\fbox{4}\fbox{5}\fbox{6}\fbox{7}\fbox{8}\fbox{9}\fbox{10}\fbox{11}\fbox{12}\fbox{13}\fbox{14}\fbox{15}\fbox{16}\fbox{17}\fbox{18}\fbox{19}\fbox{20}\\
\fbox{A\quad\quad}\fbox{B\quad\quad\quad\qquad}\fbox{E\qquad}\fbox{C\quad\quad\quad\qquad}\fbox{D\qquad\qquad\qquad}}$$
- Round Robin:
$$\displaylines{\fbox{1}\fbox{2}\fbox{3}\fbox{4}\fbox{5}\fbox{6}\fbox{7}\fbox{8}\fbox{9}\fbox{10}\fbox{11}\fbox{12}\fbox{13}\fbox{14}\fbox{15}\fbox{16}\fbox{17}\fbox{18}\fbox{19}\fbox{20}\\
\fbox{A\quad}\fbox{B}\fbox{A}\fbox{B}\fbox{C}\fbox{B}\fbox{D}\fbox{C}\fbox{B}\fbox{E}\fbox{D}\fbox{C}\fbox{B}\fbox{E}\fbox{D}\fbox{C}\fbox{B}\fbox{D\quad}}$$
^1673100631098

### Eigenschaften
- Es existiert eine Policy für [[../Echtzeitfähigkeit|Echtzeitfähigkeit]], die wird aber in der Praxis nicht benutzt
