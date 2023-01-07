---
tags: uni theo-2 theoretical-cs halteproblem
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Halteproblem auf leerem Band
linter-yaml-title-alias: Halteproblem auf leerem Band
date-of-creation: 2022-07-03
mod-date: 2022-10-02
---

# Halteproblem auf leerem Band
→ [[Gödelisierung|Gödelisierung]]

## Definition #fc
$$H_0 = \{w~| M_w\text{ hält auf auf der Eingabe }\varepsilon\}$$
^1660502790633

### Beweis: $H_0$ ist nicht entscheidbar #fc
- Zu zeigen: [[Halteprobleme/Allgemeines Halteproblem|H]] $\leq H_0$
- Sei $M(w,x)$ in Abhängigkeit von $w,x$ definiert als:
```
Schreibe x aufs Band
Setze Schreib-/Lesekopf an den Anfang von x
Arbeite weiter wie M_w
```
→ $M(w,x)$ arbeitet ohne Input, nur mit gegebenen Zeichenketten $w, x$
- Zu $M(x,w)$ kann ein [[Gödelisierung|Gödelindex]] $M_{w'}$ berechnet werden
- Sei $f$ eine totale und berechenbare Funktion mit $f(w\#x) = w',f(z\neq w\#x)=w_0 \notin H_0$
- $M_{w'} = M(w,x)$ arbeitet auf $\varepsilon$ wie $M_w$ auf $x$, woraus folgt, dass
$$w' \in H_0 \Leftrightarrow w\#x \in H \quad\text{oder}\quad w\#x \in H \Leftrightarrow f(w\#x) \in H_0$$
	→ $H_0$ ist unentscheidbar $\quad\square$
^1664742799788
