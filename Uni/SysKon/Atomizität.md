---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Atomizität
  - atomar
  - atomarer Befehl
linter-yaml-title-alias: Atomizität
date-of-creation: 2023-01-02
mod-date: 2023-01-03
---

# Atomizität

## Definition #fc
- Ein Befehl verwendet maximal einen Lese- oder Schreibzugriff auf gemeinsame Ressourcen
	→ Auf geteilten Datentypen sind Lese- und Schreiboperationen atomar (`volatile` Keyword in [[../../Informatik/Softwareentwicklung/ProgLangs/Java|Java]])
	→ Auf geteilten Datenstrukturen sind Zugriffe *nicht atomar*
- Grundlegende Annahmen:
	- $x\leftarrow n+1$ ist atomar, wenn $x$ lokal und $n$ geteilt ist
	- $x\leftarrow++n$ ist nicht atomar, wenn $n$ geteilt ist
^1668079574864
