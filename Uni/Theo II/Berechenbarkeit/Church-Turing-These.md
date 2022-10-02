---
tags: uni theo-2 theoretical-cs abstraction theorem
cards-deck: Uni::Courses::Theo-II
complete: true
aliases:
  - Church-Turing-These
  - Church'sche These
linter-yaml-title-alias: Church-Turing-These
date: 2022-08-06
mod-date: 2022-09-13
---

# Church-Turing-These
-> Auch nur "Churchsche These" genannt

## Definition: #fc
- Die Klasse von Funktionen, die [[Turing-berechenbar|Turing-berechenbar]] ist, stimmt mit der Klasse der im *intuitiven Sinne berechenbaren Funktionen* überein
- Die intuitiv berechenbaren Funktionen sind *nicht exakt formalisiert* und beschreibt die Funktionen, die *in irgendeiner Weise berechnet* werden können
	-> Dadurch lässt sich nachweisen, dass Funktionen nicht berechenbar sind
	-> Bis jetzt existiert noch kein Gegenbeweis
^1664742370713

## Eigenschaften:
- Der Beweis der These (konstruktiv geführt) erfolgt über die Angabe eines "Übersetzers", der jeden Algorithmus aus Algorithmenmodell A in einen Algorithmus in Algorithmenmodell B überführt[^1]
	-> Auswendig und langwierig[^2]
- Intuitiv [[../Berechenbarkeit|berechenbare]] Funktionen = [[../../Theo I/Turingmaschinen|Turingmaschinen]] = [[../../../Softwareentwicklung/Algorithmenparadigmen/Imperativ|Imperatives Algorithmenmodell]] = [[../../../Softwareentwicklung/Algorithmenparadigmen/Applikativ|Applikatives Algorithmenmodell]] = [[../../../Softwareentwicklung/Algorithmenmodelle/Makov-Algorithmen|Makov-Algorithmen]] = [[../../../Softwareentwicklung/Algorithmenmodelle/Registermaschinen|Universelle Registermaschinen]] = [[Lambda-Kalkül]] = …

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021. S.170
[^2]: Die erste Hälfte der Theo 2 Vorlesung :)
