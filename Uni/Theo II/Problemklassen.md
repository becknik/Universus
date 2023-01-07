---
tags: uni theo-2 theoretical-cs complexity
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Problemklassen
  - Entscheidungsproblem
  - Optimierungsproblem
  - Konstruktionsproblem
linter-yaml-title-alias: Problemklassen
date-of-creation: 2022-07-10
mod-date: 2022-09-10
---

# Problemklassen

## Varianten: #fc
- *Entscheidungsproblem*: Existiert eine Lösung ($\leq k$)?
	→ Die Ausgabe "*existiert nicht*" muss vom Algorithmus erzeugt werden können
- *Konstruktionsproblem*: Berechne (falls möglich) die Lösung für $\leq k$
	→ Auch hier muss die Ausgabe "*existiert nicht*" erzeugt werden können
- *Optimierungsproblem*: Berechne die minimale Lösung
^1660502376310

## Selbstreduzierbarkeit: #fc
- Wenn der effiziente Algorithmus des *Entscheidungsproblems* $\in\text{P}$ liegt, so liegt auch das dazugehörige Optimierungsproblem $\in\text{P}$
	→ Der Algorithmus für das Optimierungsproblem lässt sich von dem für das Entscheidungsproblem ableiten
	→ Nicht jedes Problem hat diese Eigenschaften, aber die meisten (z.B. [[Komplexitättheorie/Probleme/Vertex Cover|VC]])
^1664741239338
