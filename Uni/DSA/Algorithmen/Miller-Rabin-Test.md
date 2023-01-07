---
tags: uni dsa practical-cs maths algorithm problem
cards-deck: Uni::Courses::DSA
completed: true
aliases: Miller-Rabin-Test
linter-yaml-title-alias: Miller-Rabin-Test
date-of-creation: 2022-07-27
mod-date: 2022-09-05
---

# Miller-Rabin-Test

## Funktionsweise: #fc
- *Gegeben*: Ein ungerades $n\in\mathbb{N}$
- *Gesucht*: Ist $n\in\mathbb{P}?$
1. Wähle ein $a$ *zufällig* aus $\{2,3,\dots,n-1\}$
2. Bestimme $j,(d$ *ungerade*$)$ aus $n-1=2^j\cdot d$
3. Konstruiere die Folge $(a^{2{^0}d},a^{2^1d},a^{2^2d},\dots,a^{2^{j-1}d},1\equiv a^{n-1}\equiv a^{2^jd})$
	→ Letzteres folgt aus dem kleinen fermatschen Satz
4. Teste für alle Elemente der Folge $a^{2^{0\dots j-1}d}\equiv 1,n-1\pmod n$
	→ $=1$ darf nur beim ersten Element der Folge gelten
	→ Falls daraus eine Folge aus Einsen entsteht, ist $n$ wahrscheinlich $\in\mathbb{P}$
Beispiel:
- $n=221,\quad n-1 = 55*2^2 \quad\rightarrow d = 55, j = 2$
- $a^{2^0d}\pmod n=174^{55}\pmod n=47\neq1,n−1$
- $a^{2^1d} \pmod n = 174^{110} \pmod n = 220 = n-1$
→ $n$ ist ein starker Lügner und daher unwahrscheinlich $\in\mathbb{P}$
^1658939366453

## Eigenschaften:
- Ist ein [[Muster/Monte-Carlo|Monte-Carlo Algorithmus]]
- Die Wahrscheinlichkeit für eine Fehlerklassifikation bei einer Durchführung liegt bei 10 Schritten $< \frac{1}{4}^10<10^{-6}$
