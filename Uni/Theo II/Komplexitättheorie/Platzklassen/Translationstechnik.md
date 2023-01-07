---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Translationstechnik
linter-yaml-title-alias: Translationstechnik
date-of-creation: 2022-08-13
mod-date: 2022-10-24
---

# Translationstechnik

## Definition: #fc
$$f:\mathbb{N}\rightarrow\mathbb{N}\text{ mit }\forall n:n\leq f(n):Pad_f(L):=\{w\#^{f(\mid w\mid)-\mid w\mid}\mid w\in L\},\#\notin\Sigma$$
- "Eine ausgestopfte Version einer Sprache wird erzeugt, um den Rechenaufwand für die künstlich aufgeblähte Eingabelänge kleiner wird"
- *Aussagen* der Translationssätze:
	- Resultate für *Gleichheiten* oder *Inklusionen* können aus KLEINEREN $\Rightarrow$ größere [[Platzkomplexität|Platzklassen]] übertragen werden
	- Resultate für *Separationen* können GRÖSSEREN Platzklassen $\Rightarrow$ Kleinere übertragen werden
- [[../Translationssätze|Translationssätze]]
^1660502896409

## Folgerungen: #fc
- $DSPACE(n)\subsetneq NSPACE(n)\Rightarrow L\subsetneq NL$
- Kombination aus dem Translationssatz für Platz- und Zeitklassen: $DSPACE(n)\neq P$
^1660945844407
