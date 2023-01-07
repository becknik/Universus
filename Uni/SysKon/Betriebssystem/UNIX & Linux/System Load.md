---
tags: uni practical-cs syskon os unix
cards-deck: Uni::Courses::SysKon
completed: true
aliases: System Load
linter-yaml-title-alias: System Load
date-of-creation: 2022-11-19
mod-date: 2023-01-04
---

# System Load

## Definition & Eigenschaften #fc
- UNIX: Jeder [[../Prozess|Prozess]]/ [[../Prozesse/Threads|Thread]], der die CPU benutzt oder in einer *Ready-Queue* auf die Benutzung wartet, erhöht den Wert um 1
	→ Jeder terminierende Thread/ Prozess reduziert den Wert um 1
	→ *Linux* bezieht Prozess in *uninterruptable sleep states* (sprich *Blocked-Queues*, meistens waiting for I/O) mit ein
	→ Ob ein Thread oder Prozess den Wert inkrementiert, hängt vom Handling der Threads durch das [[../../OS|OS]] ab (z.B. [[../Prozesse/Threads#Solaris fc|Solaris]])
- Wird für 1, 5 und 15 Minuten über exponentiell gewichtete Mittelwerte berechnet
	→ Der 1 Minuten Wert besteht aus $1-\frac{1}{e}\approx63\%$ aus dem Load der letzten Minuten, der Rest ergibt sich aus dem Messungen seit dem Systemstart
- *Interpretation*: In den letzten $n$ Minuten war das System zu $\approx\frac{0.63\cdot n\text{SystemLoad}}{\text{Virtual CPUs}}\%$ durch Prozesse in *Ready*- (& *Uninterruptable Sleep*-) Queues und CPU-Time ausgelastet
^1672846262509

[1]: [Wikipedia](https://en.wikipedia.org/wiki/Load_(computing))
