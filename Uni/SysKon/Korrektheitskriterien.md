---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Korrektheitskriterien
  - Fairness
  - schwache Fairness
  - starke Fairness
  - Sicherheit
  - Lebendigkeit
linter-yaml-title-alias: Korrektheitskriterien
date-of-creation: 2022-11-07
mod-date: 2022-11-10
---

# Korrektheitskriterien

## Sicherheit #fc
- Im Sinne von "Es muss immer/ darf niemals gelten"
- Für eine *Sicherheitseigenschaft* eines Programms gilt:
	- Sie muss in **jeden** möglichen *Ausführungszustands* des Programms **immer** gelten
	→ Das Programm ist korrekt oder nicht
^1667836898083

## Lebendigkeit #fc
- Für eine *Lebendigkeitseigenschaft* gilt:
	- *Für jeden Zustand* eines Programms gibt es eine *Ausführungs-Fortsetzung,* in der die Eigenschaft in *endlich vielen Schritten* erfüllt wird
	→ Lebendigkeit definiert keine obere Zeitschranke
- Voraussetzung: jeder Befehl wird endlich ausgeführt
	→ Lebendigkeit benötigt immer Fairness
^1667836898088

## Beispiel
- Gegeben: Ein Programm mit zwei nebenläufigen Prozessen $p,q$, die jeweils 50 Mal eine globale Variable hochzählen und sie dann ausgeben
- Sicherheit:
	- Druche nur Zahlen $\in[1\dots100]$
	- Keine Zahl wird mehrfach gedrucht
- Lebendigkeit:
	- Jede Zahl $\in[1\dots100]$ wird schließlich ausgegeben

## Analyse
- Es ist nicht nötig, sämtliche Zustände zu betrachten
	→ Es reicht etwas geschicktes hinzuschreiben

## Fairness

### Schwach #fc
- Jeder *ständig ausführ-bereite Befehl* eines schwach-fair ausgeführten Prozesses wird vom System schließlich ausgeführt
	→ Die Ausführung von Befehlen, die nicht ständig ausführ-bereit sind (wie zum Beispiel das Verarbeiten von Anfragen), wird nicht garantiert
^1668079035538

### Stark #fc
- Jeder nicht notwendigerweise ständig, aber unendlich oft ausführ-bereite Befehl eines stark-fair ausgeführten Prozesses wird unendlich oft ausgeführt
	→ Da Betriebssysteme Gedächtnislose Prozesse sind, ist es schwer zu implementieren
^1668079035541
