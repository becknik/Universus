---
tags: uni dsa practical-cs abstraction algorithm
cards-deck: Uni::Courses::DSA
status: unfinished
aliases: Suchverfahren
linter-yaml-title-alias: Suchverfahren
date: 2022-07-24
mod-date: 2022-09-08
---

# Suchverfahren
-> [[Algorithmen auf Graphen|Algorithmen Auf Graphen]]
- [[Text-Such-Algorithmem|Text-Such-Algorithmen]]
	-> [[Text/Reguläre Audrücke|Reguläre Ausdrücke]]
- [[Hashfunktionen|Hashfunktionen]]

## Komplexitäten von Varianten:
| Verfahren                                        | Bester Fall | Schlechtester Fall | Durchschnitt: Erfolgreich | Durchschnitt: Erfolglos |
| ------------------------------------------------ | ----------- | ------------------ | ------------------------- | ----------------------- |
| [[Algorithmen/Suche/Sequenzielle Suche\|Sequenzielle Suche]] | 1           | $n$                | $\frac{n+1}{2}$           | $n$                     |
| [[Algorithmen/Suche/Binäre Suche\|Binäre Suche]]             | 1           | $\log n$           | $\log n$                  | $\lceil\log n\rceil$                |
| [[Bäume/Suchbaum\|Suchbäume]]                    | 1            | $\log n$                   | $\log n$                          | $\lceil\frac{\log n}{2}\rceil$                        |
