---
tags: uni dsa practical-cs hash algorithm
cards-deck: Uni::Courses::DSA
completed: true
aliases: Multiplikationsverfahren
linter-yaml-title-alias: Multiplikationsverfahren
date-of-creation: 2022-07-24
mod-date: 2022-09-05
---

# Multiplikationsverfahren

## Funktionsweise: #fc
1. Der Objektschlüssel $s$ wird mit der *möglichst unrationalen* Zahl $0 < z < 1$ multipliziert
	→ Beispielsweise kommt die Dezimalbruchentwicklung der harmonischen Reihe, die Goldene Zahl etc. infrage
2. Ganzzahl wird entfernt: $g(s) = s\cdot z-\lfloor s\cdot z\rfloor$
3. Addition mit $p$ und abrunden: $h(s)=\lfloor p\cdot g(s)\rfloor$
^1656966172271

## Beispiel: #fc
Beispiel: $z=0,6180339887$
| $s$ | $s*z$      | $g(s)$     | $h(s)$ |
| --- | ---------- | ---------- | ------ |
| 0   | 0          | 0          | 0      |
| 1   | 0,61803399 | 0,61803399 | 6      |
| 2   | 1,23606798 | 0,23606798 | 2      |
| 3   | 1,85410197 | 0,85410197 | 8      |
| 4   | 2,47213595 | 0,47213595 | 4      |
| 5   | 3,09016994 | 0,09016994 | 0      |
| 6   | 3,70820393 | 0,70820393 | 7      |
| 7   | 4,32623792 | 0,32623792 | 3      |
| 8   | 4,94427191 | 0,94427191 | 9      |
| 9   | 5,56230590 | 0,5623059  | 5      |
^1659709231556
