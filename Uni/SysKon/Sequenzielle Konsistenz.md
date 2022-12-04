---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - Sequenzielle Konsistenz
  - Memory Order Models
linter-yaml-title-alias: Sequenzielle Konsistenz
date: 2022-11-07
mod-date: 2022-12-03
---

# Sequenzielle Konsistenz
-> [[Nebenläufige Programme]]

## Definition: #fc
- Alle Prozesse/Threads sehen Ergebnisse von Schreiboperationen in gleicher sequentieller Ordnung.
^1667833625245

## C

## Memory Order Models: #fc
- *Relaxierte Ordnung*: Lese- und Schreiboperationen auf den Speicher dürfen umgeordnet werden, so lange die Single-Threaded-Semantik erhalten bleibt
- *Aquire/Release-Semantik*: Lese- und Schreiboperationen in einem kritischen Abschnitt bleiben auch dort
^1667833625254
