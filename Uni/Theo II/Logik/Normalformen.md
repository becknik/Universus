---
tags: uni theo-2 theoretical-cs logic 
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Normalformen
date-of-creation: 2022-08-05
mod-date: 2022-08-11
linter-yaml-title-alias: Normalformen
---

# Normalformen

## Definitionen: #fc
- *Positives Literal*: Eine atomare Formel $A_i$
- *Negatives Literal*: Eine Negation einer atomaren Formel
- *DNF*: Disjunktion ($\bigvee$) von Konjunktionen ($\bigwedge$) von Literalen
	→ Die Spalten mit positiven [[Belegung|Belegungen]] werden "intern" $\wedge$- und "extern" $\vee$-Verknüpft
- *KNF*: Konjunktion ($\bigwedge$) von Disjunktionen ($\bigvee$) von Literalen (=Klauseln)
	→ Alle Spalten, die für $F$ eine negative Belegung annehmen, werden durch einfügen in die inneren Teilformeln ($\wedge$) der *KNF* ausgeschlossen
^1664741821766

## Eigenschaften: #fc
- Zu jeder Formel $F$ existiert eine semantisch äquivalente *Normalform*
	→ Die Komplexität des Verfahrens liegt in [[../Komplexitättheorie/Zeitklassen/EXPTIME|EXPTIME]]
^1664741828363
