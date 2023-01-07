---
tags: uni dsa practical-cs hash trait
cards-deck: Uni::Courses::DSA
completed: true
aliases: Geschlossenes Hashing
linter-yaml-title-alias: Geschlossenes Hashing
date-of-creation: 2022-07-26
mod-date: 2022-09-06
---

# Geschlossenes Hashing

## Eigenschaften: #fc
- Bei einer Kollision durch $h(s)$ wird über $G(s,i)$ eine neue Position in der Hashtabelle gesucht
	→ $i$ steht für die Versuchsnummer
- Sondieren muss nicht nur beim Einfügen, sondern auch beim *Suchen und Löschen* beachtet werden
- Für den Auslastungsgrad $\lambda$ gilt: $\lambda = \frac{k}{p} \leq 1$, wobei $k$ der Anzahl der gespeicherten Elemente entspricht
^1658939281405

## Lineares Sondieren: #fc
- $G(s, i) = (h(s) + i*c)\pmod p$
- ! $ggT(c,p) = 1$, da ansonsten nicht alle Positionen ausprobiert werden
- Durch die Linearität kann es leicht zu sich selbst vergrößernde *Cluster* durch *Sekundärkollisionen* kommen
	→ Lineares Sondieren ist hingegen nicht immer besser als quadratisches
- *Löschen*:
	1. *deleted-Flags* werden für jedes gelöschte Feld gesetzt, das nur beim Suchen beachtet wird
	2. *Zurückkopieren* über Einträge, die sich laut $G(s,i)$ anbieten
^1656967139890

## Quadratisches Sondieren: #fc
- $G(s, i) = (h(s) + i²*c) \pmod p$
	→ Für $p$ sollte eine Primzahl gewählt werden
	→ Muss sowohl beim *Einfügen*, als auch beim *Suchen* angewendet werden
- Löschen ist "sehr kompliziert" und nur durch *deleted-Flags* möglich
^1656967539699
