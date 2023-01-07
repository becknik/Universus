---
tags: uni dsa practical-cs tree indexstruct
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Rot-Schwarz-Baum
  - RS-Baum
linter-yaml-title-alias: Rot-Schwarz-Baum
date-of-creation: 2022-07-22
mod-date: 2022-09-06
---

# Rot-Schwarz-Baum

## Eigenschaften: #fc
- Repräsentieren [[2-3-4-Baum|2-3-4-Bäume]] binär, wobei verbindende Kanten $\text{ROT}$ gefärbt sein sollen
	→ Knoten nehmen das Farbattribut der Kante zu ihren Elternknoten $\in \{\text{ROT}, ~\text{SCHWARZ}\}$ an
	→ Die *Wurzel* muss schwarz gefärbt sein
	→ *Kinder* eines roten Knotens müssen schwarz sein
- **Schwarztiefe**: Jeder Pfad von einem Knoten $k$ zu einem Blatt enthält die gleiche Anzahl schwarzer Knoten
- Alle *Nil-Knoten* sind schwarz gefärbt
- Ein RS-Bäume müssen nicht komplett balanciert sein, damit Operationen auf ihnen $\in \mathbfcal{O}(\log n)$ liegen
- Kommen in Java viel zum Einsatz
^1652127802082

## Ausgleichsstrategien beim Einfügen: #fc
- *Top-Down*: Alle besuchten 4-Knoten auf dem Weg zum Zielknoten werden gesplittet (=umgefärbt)
- *Bottom-Up*: Einfügen und dann ggf. zum Ausgleich rückwärts splitten oder rotieren
	→ Da nicht-aneinanderhängende 4-Knoten nicht gespleißt werden, ist diese Methode "besser"
^1662133357840

## Fälle beim Splitten: #fc
- 4-Knoten hängt an einem 2-Knoten:
	- Die unteren, roten Farbattribute werden von den äußeren zwei Knoten auf den mittleren Knoten des 4-Knotens übertragen
- 4-Knoten hängt an einem 3-Knoten:
	1. Die roten Farbattribute der unteren Knoten des 4-Knotens werden auf den Mittleren übertragen
		→ Nun hängen zwei rote Knoten hintereinander, was die RS-Eigenschaften verletzt
	2. Eine Rotation des unteren, rot gefärbten Knoten des 3-Knotens wird über den oberen, schwarz Knoten des 3-Knotens durchgeführt
		 → Da der rot gefärbte Knoten des 3-Knotens nun oben steht, sind die Eigenschaften des RS-Baums immer noch nicht erfüllt
	3. Der Knoten mit dem rote Farbattribut des ehemaligen unteren 3-Knotens wird nun auf den sich nun auf seiner Seite befindenden, ehemalig oberen Knoten des 3-Knotens übertragen
		→ Die beiden rote Knoten (ehemalig oberer 3-Knoten und oberer 4-Knoten) sowie die schwarz gefärbten Knoten liegen nun auf demselben Niveau
^1654723211883

## Einfügen: #fc
1. Die Einfügeposition suchen und und einen neuen Blattknoten an der geeigneten Stelle erstellen
	 → Top-Down- oder Bottom-Up-Spleißen
2. Die Eigenschaften des Rot-Schwarz-Baums durch Spleißen und Rotieren wiederherstellen, wenn notwendig
^1662387494109
