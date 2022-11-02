---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
complete: true
aliases: Prozess
linter-yaml-title-alias: Prozess
date: 2022-10-28
mod-date: 2022-10-31
---

# Prozess

## Definition: #fc
- Ein Prozess besteht aus einem Tupel $(P,Z)$
	- $P=\{p_1,p_2,\dots,p_n\}:$ Eine Zerlegung des Programmtextes in *atomare Befehle*
		 -> Das *Textsegment*
	- $Z=\{z_1,z_2,\dots,z_m\}:$ Eine Menge von *Kontroll- und Zustandsinformationen*
		 -> Daten im Speicher und Status der Register
- Sei $c_p=p_i$ der in einer Ausführung als nächstes ausführbare Befehl definiert
	-> [[../../Ro I/RISC-V/Problem Counter|Problem Counter]]
^1667058688569

## Eigenschaften: #fc
- Mehrere Prozesse können sich Ressourcen teilen
	-> z.B. über gemeinsame Speicherbereiche
- Der Zustand auf gemeinsamen Speicher ist durch die Reihenfolge der Zugriffe definiert
	-> Die Zugriffsordnung ist innerhalb eines Prozesses eindeutig durch die Sequenz atomarer Operationen definiert 
	-> Der Speicher stellt die Atomizität von (parallelen) Operationen auf Mehrprozessorsystemen sicher
^1667058688578
