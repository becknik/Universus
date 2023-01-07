---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Nebenläufige Programme
linter-yaml-title-alias: Nebenläufige Programme
date-of-creation: 2022-10-29
mod-date: 2022-11-07
---

# Nebenläufige Programme

## Definition #fc
- Ein nebenläufiges Programm besteht aus einer endlichen Menge interagierender [[Betriebssystem/Prozess|Prozessen]] $\Pi=\{p^{(1)},\dots,p^{(l)}\}$, die auf einer Menge von Ressourcen $R_\Pi$ ausgeführt werden
- Dabei muss gelten:
	1. Die *Ausführung* kann durch eine Sequenz von atomaren Befehlen beschrieben werden, in der jeweils genau ein Prozess voranschreitet
	2. Paare von Prozessen können sich *Ressourcen* $r\in R_\Pi$ teilen und deren *Belegung* ändern
	3. Nach Veränderung der Belegung eines geteilten $r\in R_\Pi$ ist diese Änderung im nächsten Ausführungsschritt sichtbar
^1667060692644

### Zustand #fc
- Die Menge der Kontroll- und Zustandsinformation sämtlicher beteiligter [[Betriebssystem/Prozess|Prozesse]]
- Notation (für Prozess $p,$ globale Variable $n$ & Lokale Variablen $a,b$): $$\displaylines{p_1:n\leftarrow a\\a=1,b=2\mid n=0}$$
	→ Bei mehreren Programmen werden mögliche parallele Instruktionen der beiden Programme untereinander geschrieben und Verzweigungen gezeichnet
^1667060692654

### Szenario #fc
| Prozess $p$             | Prozess $q$             | $n$ | $a$ | $b$ |
| ----------------------- | ----------------------- | --- | --- | --- |
| $\bf p_1:n\leftarrow a$ | $q_1:n\leftarrow b$     | 0   | 1   | 2   |
| (end)                   | $\bf q_1:n\leftarrow b$ | 1   | 1   | 2   |
| (end)                   | (end)                   | 2   | 1   | 2   |
- Ein Szenario ist durch eine Folge von Zuständen definiert
^1667060692658

## Ausführung

### Multiprozessoren #fc
- Zwei Sequenzen von Zustandsübergängen führen in einem nebenläufigen Programm bei Ausführung auf [[Systemarchitekturen|Multikernprozesooren]] zum selben Endzustand, wenn folgende Eigenschaften erfüllt werden:
	1. Die sequenzielle Ordnung der Befehle bleibt erhalten
		 → Dieselbe Ausführungsordnung beim Zugriff auf lokale Ressourcen
	2. Die Ausführungsordnung von Befehlen auf atomar veränderbaren gemeinsamen Ressourcen bleibt erhalten
	→ Betrachte für jeden Zustand nur eine repräsentative Ausführungssequenz, welche die Eigenschaften 1 und 2 erfüllt.
^1667832897093

### Verteilte Systeme #fc
- Auf *verteilten System* führen je zwei Sequenzen von Zustandsübergängen in einem nebenläufigen Programm zum selben Endzustand, wenn…
	1. Die *sequentielle Ordnung* der atomaren Befehle eines Prozesses erhalten bleibt
	2. Die *Ausführungsordnung* von Befehlen unter Einhaltung der *Sende/Empfangs-Relation* bleibt erhalten
^1667834601943
