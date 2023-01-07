---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Philosophenproblem
linter-yaml-title-alias: Philosophenproblem
date-of-creation: 2023-01-04
mod-date: 2023-01-04
---

# Philosophenproblem
→ [[Philosophenproblem|DSA: Philosophenproblem]]

## Allgemeine Problemstellung #fc
- Mehrere [[../Betriebssystem/Prozess|Prozesse]] greifen nebenläufig auf $n\geq2$ Ressourcen zu, die sie zur Ausführung benötigen
	→ Wie lässt sich die Zuweisung koordinieren, so dass *keine Verklemmungen* zwischen mehreren Prozessen auf eine Ressource kommt?
	→ Wie vermeidet man das *Aushungern* einzelner Prozesse?
	→ Wie erreicht man eine möglichst *feine Granularität* bei der Allokation der Ressourcen?
^1672841797734

## Aufbau & Zustände #fc
- $N=5$ Philosophen, wobei der $i.$ Philosoph auf die linke ($i.$) und rechte ($(i+1\mod N).$) Gabel *allokieren* muss
	→ Lösungen funktionieren für beliebige $N\geq1$
- Die Philiosophen durchlaufen die Zustände $\fbox{Denken}$, $\fbox{Hungrig}$ und $\fbox{Essen}$
	→ Nicht [[../Kritischer Abschnitt|KA]], Präprotokoll und KA
^1672841797738

## Lösungen

### [[../Korrektheitskriterien|Faire]] [[Semaphore]] #fc
- Naive Lösung: Benachbarte Philosophen $P_{i}$ und $P_{i+1}$ streiten sich aus Sicht von $P_i$ um die zweite/rechte Gabel und aus Sicht von $P_{i+1}$ um die erste/linke Gabel
	→ Lasse gerade $P_i$ sich zuerst die *linke Gabel* schnappen, ungerade $P_i'$ dagegen zuerst die *rechte Gabel* an sich nehmen
	→ Ein Philosoph bekommt die Gabel garantiert
→ Asymmetrischer Zugriff
^1672841797741

### [[Monitore]] #fc
- Nur ein Philosoph kann gleichzeitig `getForks()` oder `releaseForks()` ausführen und damit auf alle Gabeln zugreifen
	→ Nur ein Paar wird modifiziert, was den potentiellen Zugriff auf $N-2$ Gabeln verschwendet
	→ Weniger Nebenläufigkeit als bei der Lösung mit Hilfe von [[#../Korrektheitskriterien Faire Semaphore|Sempahoren]]
^1672841797744
