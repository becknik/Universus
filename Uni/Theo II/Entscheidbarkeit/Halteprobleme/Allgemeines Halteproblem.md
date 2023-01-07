---
tags: uni theo-2 theoretical-cs halteproblem
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Allgemeines Halteproblem
  - H
linter-yaml-title-alias: Allgemeines Halteproblem
date-of-creation: 2022-07-03
mod-date: 2022-09-12
---

# Allgemeines Halteproblem
→ [[Gödelisierung]]

## Definition & Beweis: #fc
$$H = \{w\#x~| M_w\text{ hält auf der Eingabe }x\}$$
**Beweis:** $H$ ist *nicht [[../../Entscheidbarkeit|entscheidbar]]*
- Zu zeigen: [[Halteprobleme/Spezielles Halteproblem|K]] $\leq H$
- Sei $f: f(w) = w\#w$, dann ist $f$ total und berechenbar und es gilt: $w \in K\Leftrightarrow f(w) \in H$.
	→ Wäre also $H$ entscheidbar, dann wäre es auch [[Halteprobleme/Spezielles Halteproblem|K]] entscheidbar $\quad\square$
^1660502721082

## Alternative Herleitung:[^1]
- Gäbe es einen Algorithmus, der für ein beliebiges $y\in dom~\varphi_x$ entscheidet, dann könnte man damit auch im Speziellen $x\in dom~\varphi_x$ entscheiden

## Eigenschaften:
- **Aussage**: *Hält Algorithmus $x$ auf der Eingabe $y$?*
	→ $y\in dom~\varphi_x$, dem definierten Urbild des Algorithmus' $x\in A^{Stern}$ (Alphabet für Algorithmen)

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021.
