---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Satz von Immerman–Szelepcsényi
  - Komplementabschluss von NSPACE(s)
linter-yaml-title-alias: Satz von Immerman–Szelepcsényi
date-of-creation: 2022-08-13
mod-date: 2022-10-24
---

# Satz von Immerman–Szelepcsényi

## Definition: #fc
- Sei $f\in\Omega(\log n),$ dann gilt: $$NSPACE(f)=coNSPACE(f)$$
- *Aussage*: Bei [[SPACE|NSPACE]] kriegt man sowohl verlässliche JA-, als auch NEIN-Aussagen, bei [[../Zeitklassen/TIME|NTIME]] hingegen nicht
	→ Bei [[../../../Theo I/Grundlegendes/Determinismus|Determinismus]] ist das viel einfacher, da man JA und NEIN vertauchen kann
	→ Bei [[../../../Theo I/Grundlegendes/Nichtdeterminismus|Nichtdeterminismus]] kann es für eine NEIN-Aussage mehrere Berechnungspfade geben
^1660502966505

## Folgerungen:
- Die Sprachklasse [[../../../Theo I/Typ-1|Typ-1/ CSL]] ist *gegen Komplementbildung abgeschlossen*

## Eigenschaften:
- (Zuerst ?) von Robert Szelepcsénsyi als Studen und (dann ?) von Neil Immerman entdeckt
- [[SPACE|DSPACE]] und [[SPACE|NSPACE]] sind $\forall f\in\Omega(\log n)$ gegen Komplement abgeschlossen

## Beweis:
- Metode: *Induktives Zählen*
- Prüfe für [[../../../Theo I/Turingmaschinen|NTM]] mit $w$ als Eingabe, ob $w\notin L(M)$ in $SPACE(\mathcal{O}(f(n))$
- Beweis: (F35.6ff.) (ist ewig lang…)
