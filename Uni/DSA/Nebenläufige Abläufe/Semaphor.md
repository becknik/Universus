---
tags: uni dsa practical-cs
cards-deck: Uni::Courses::DSA
completed: true
aliases: Semaphor
linter-yaml-title-alias: Semaphor
date-of-creation: 2022-07-20
mod-date: 2022-09-13
---

# Semaphor

## Funktionsweise: #fc
- Setzt sich aus einem Zähler und einer [[../Datenstrukturen/Queue|Queue]] zusammen
	→ Der Zähler repräsentiert die Anzahl der Prozesse, die auf den *kritischen Bereich* zugreifen dürfen
- Wenn der Zähler auf 0 sinkt, werden nachfolgende Prozesse in die Queue gelegt
- Semaphor Operationen:
	- *down()*: Warteoperation - Betreten des kritischen Abschnitts
	- *up()*: Signaloperation - Verlassen des kritischen Abschnitts
^1657020897497

## Eigenschaften:
- Sind eher Inhalte der Synchronisation zugrunde liegender Konzepte, wie sie beispielsweise in Betriebssystemen vorkommen[^1]

## Code: #fc
```
Method: down (int semaphor)
if 1 ≤ semaphor then
	semaphor--;
else
	Blockiere den ausführenden Prozess
	Trage den Prozess in die Warteschlange W(s) ein
fi
```
```
Methode: up (int semaphor);
semaphor++;
if Warteschlange W(s) nicht leer then
	Wähle Prozess Q aus W(s) aus
	Versetze Q in den Zustand 'bereit‘
fi
```
^1658939300279

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021. S.282
