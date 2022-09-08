---
tags: uni dsa practical-cs
cards-deck: Uni::Courses::DSA
status: 
aliases: Semaphor
linter-yaml-title-alias: Semaphor
date: 2022-07-20
mod-date: 2022-09-04
---

# Semaphor

## Funktionsweise: #fc
- Setzt sich aus einem Zähler und einer [[../Datenstrukturen/Queues|Queue]] zusammen
	-> Der Zähler repräsentiert die Anzahl der Prozesse, die auf den *kritischen Bereich* zugreifen dürfen
- Wenn der Zähler auf 0 sinkt, werden nachfolgende Prozesse in die Queue gelegt
- Semaphor Operationen:
	- *down()*: Warteoperation - Betreten des kritischen Abschnitts
	- *up()*: Signaloperation - Verlassen des kritischen Abschnitts
^1657020897497

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
