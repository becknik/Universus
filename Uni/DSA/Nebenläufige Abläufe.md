---
tags: uni dsa practical-cs parallel abstraction
cards-deck: Uni::Courses::DSA
complete: true
aliases: Nebenläufige Abläufe
linter-yaml-title-alias: Nebenläufige Abläufe
date: 2022-07-27
mod-date: 2022-09-05
---

# Nebenläufige Abläufe

## Eigenschaften:
- Mehrere kommunizierende Automaten werden in Form von Prozessen *koordiniert*
- Kommen bei verteilten oder mehrkernigen Systemen zum Einsatz
	-> [[../../Privat/Programmiersprachen/Java/Java-Threads|Java-Threads]]

## Zustände: #fc
- *Initialisiert* $\Rightarrow$ *Bereit* $\Leftrightarrow$ *Aktiv* $\Rightarrow$ *Terminiert*
- *Blockiert*: Falls eine gemeinsame Ressource durch einen anderen Prozess gesperrt ist
	-> *Aktiv* $\Rightarrow$ *Blockiert* $\Rightarrow$ *Bereit*
^1657017218566

## Themen:
- [[Nebenläufige Abläufe/Petri-Netze|Petri-Netze]]
- [[Nebenläufige Abläufe/Philosophenproblem|Philosophenproblem]]
- [[Nebenläufige Abläufe/Amdahlsches Gesetz|Amdahlsches Gesetz]]
- [[Nebenläufige Abläufe/Message Passing Interface|Message Passing Interface]]
