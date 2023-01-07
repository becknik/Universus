---
tags: uni dsa practical-cs algorithm text
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Knuth-Morris-Pratt
  - KMP
linter-yaml-title-alias: Knuth-Morris-Pratt
date-of-creation: 2022-07-24
mod-date: 2022-09-07
---

# Knuth-Morris-Pratt
→ [[../../Text-Such-Algorithmem|Text-Such-Algorithmen]]

## Eigenschaften: #fc
- Der Algorithmus stellt durch die Verwendung von *positiven Informationen* aus dem vorherigen Vergleich eine Erweiterung des [[../Muster/Brute Force|Brute Force Ansatzes]] dar
- Liegt durch die Suche & Analyse des Musters in $O(n+m)$
- Ist *Stream*-fähig
- In der Praxis ist der Algorithmus aufgrund der geringen Selbstähnlichkeit der Texte kaum effizienter als die native Suche
	→ In der Bioinformatik hingegen schon
^1656412370585

## Funktionsweise: #fc
- Die Funktion $f$ ermittelt die Länge der Übereinstimmung des Suffix des Präfixes von $p$ ab dem ersten Index ($p[1..k],<|p|$) mit dem nicht modifizierten $p[0,\dots,|p|-1]$
- Wenn beim Vergleichen ein Mismatch an der $j.$ Stelle auftritt, dann entspricht $f(j-1)$ dem *Index von $p$*, der an die Mismatch-Position gerückt wird
- Wenn $j == 0$ gilt, dann wird das Muster nur *um einen Index verrückt*
Beispiel:
$k=0\quad\quad\quad[a|b|a|c|a|b]\quad\rightarrow f(0)=0$
$k=1\quad b\quad\quad[a|b|a|c|a|b]\quad\rightarrow f(0)=0$
$k=2\quad b\underline{a}\quad\quad[\underline{a}|b|a|c|a|b]\quad\rightarrow f(0)=1$
$k=3\quad bac\quad\quad[a|b|a|c|a|b]\quad\rightarrow f(0)=0$
$k=4\quad bac\underline{a}\quad\quad[\underline{a}|b|a|c|a|b]\quad\rightarrow f(0)=1$
$k=5\quad bac\underline{ab}\quad\quad[\underline{a}|\underline{b}|a|c|a|b]\quad\rightarrow f(0)=2$
-
| Position $k$ im Pattern | 0 | 1 | 2 | 3 | 4 | 5 |
| ----------------------------- | --- | --- | --- | --- | --- | --- |
| Pattern $p[k]$ | a | b | a | c | a | b |
| Längstes Präfix$[k]$: $f(k)$ | 0 | 0 | 1 | 0 | 1 | 2 |
^1655838192596
