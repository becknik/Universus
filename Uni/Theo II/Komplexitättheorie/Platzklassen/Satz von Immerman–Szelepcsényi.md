---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases:
  - Satz Von Immerman–Szelepcsényi
  - Komplementabschluss von NSPACE(s)
linter-yaml-title-alias: Satz Von Immerman–Szelepcsényi
date: 2022-08-13
mod-date: 2022-09-22
---

# Satz Von Immerman–Szelepcsényi

## Definition: #fc
- Sei $f\in\Omega(\log n),$ dann gilt $$NSPACE(f)=coNSPACE(f)$$
-> *Aussage*: Bei $SPACE$ kriegt man sowohl verlässliche JA-, als auch NEIN-Aussagen, bei $NTIME$ hingegen nicht
	-> Bei *Determinismus* ist das viel einfacher, da man JA und NEIN vertauchen kann
	-> Bei *nicht-Determinismus* kann es für eine NEIN-Aussage mehrere Berechnungspfade geben
^1660502966505

## Eigenschaften:
- (Zuerst?) von Robert Szelepcsénsyi als Studen und (dann?) von Neil Immerman entdeckt
- Eine Folgerung: Die Sprachklasse [[../../../Theo I/Typ-1|Typ-1/ CSL]] ist gegen Komplementbildung abgeschlossen
- $SPACE$ und $NSPACE$ sind $\forall f\in\Omega(\log n)$ gegen Komplement abgeschlossen

## Beweis:
- *Induktives Zählen*
- Prüfe für [[../../../Theo I/Turingmaschinen|NTM]] mit $w$ als Eingabe, ob $w\notin L(M)$ in $SPACE(\mathcal{O}(f(n))$
- Beweis: (F35.6ff.) (ist ewig lang…)
