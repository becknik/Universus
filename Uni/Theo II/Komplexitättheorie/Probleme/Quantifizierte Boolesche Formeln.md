---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Quantifizierte Boolesche Formeln
  - QBF
date-of-creation: 2022-08-18
mod-date: 2022-08-18
linter-yaml-title-alias: Quantifizierte Boolesche Formeln
---

# Quantifizierte Boolesche Formeln
→ Erweiterung der [[../../Logik/Aussagenlogik|Aussagenlogik]]

## Definition:
$$QBF=\{F\mid F \text{ ist eine geschlossene QBF-Formel und lässt sich zum Wert }TRUE\text{ auswerten}\}$$
- Seien alle $x_{1\leq i}$ QBF-Formeln, dann sind auch $(\neg E),(E\wedge F),(E\vee F),\forall x_iE,\exists x_iE$ QBF-Formeln
	→ Quantoren laufen nur über die Werte $TRUE,FALSE:$
	$\forall x_iE=T\Leftrightarrow (E[x_i/T]\wedge E[x_i/F])=T$ unter derselben Belegung
	$\exists x_iE=T\Leftrightarrow (E[x_i/T]\vee E[x_i/F])=T$ unter derselben Belegung
	→ $x_i$ sind im Gegensatz zur [[../../Logik/Prädikatenlogik|Prädikatenlogik]] einfache Variablen
- *Geschlossene QBF-Formel*: Eine QBF-Formel ohne freie Variablen
	→ Der Wert hängt nicht von der Belegung ab - Erfüllbarkeit ergibt keinen Sinn

## Eigenschaften:
- Ist ein [[../Platzklassen/PSPACE|PSPACE-hartes]] Problem
- Für den Beweis kommt die Master-Reduktion und die $Reach(X,Y,i)$ aus dem Beweis vom [[../Platzklassen/Satz von Savitch|Satz Von Savitch]] zu Einsatz
