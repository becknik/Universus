---
tags: uni practical-cs syskon os
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - OS-Echtzeitfähigkeit
  - Realtime
  - Echtzeit
linter-yaml-title-alias: OS-Echtzeitfähigkeit
date: 2022-11-10
mod-date: 2022-11-19
---

# OS-Echtzeitfähigkeit

## Anforderungen: #fc
- Reaktion rechtzeitig in Echtzeit
	-> Garantiert echtzeitkritischen Prozessen Zugriff auf CPU innerhalb geforderter aufgabenspezifischer Zeitspannen
	-> *Millisekunden*: Multimedia
	-> *Teilweise Mikrosekunden*: Überwachung, Steuerung & Regelung von "Cyber-Physical Systems ", Robotik, …
- Korrektheit des Systems hängt nicht nur vom logischen Resultat ab
- Der Zeitpunkt der ausgeführten Berechnung ist (teilweise) wichtig
	-> Jede Berechnung hat eine Zeitschranke, weshalb die Ergebnisse rechtzeitig vorliegen müssen oder die [[../Korrektheitskriterien|Sicherheit]] der Ausführung gefährden
- Eine minimale Antwortzeit ist nicht das Ziel von Echtzeitsystemen, sondern garantierte Antwortzeit
^1668895281296

## Gründe:
- Dedizierte Rechner für eine Aufgabe sind teils (aus mehreren Gründen) nicht erwünscht
	-> Mehrere Prozesse auf der selben Hardware sind erwünscht

## Eigenschaften:
- Ermöglicht Interaktion von Prozessen mit der physischen Umgebung
