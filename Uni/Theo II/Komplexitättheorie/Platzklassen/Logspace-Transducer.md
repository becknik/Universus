---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases:
  - Logspace-Transducer
  - logspace-berechenbar
date: 2022-08-12
mod-date: 2022-08-19
linter-yaml-title-alias: Logspace-Transducer
---

# Logspace-Transducer

## Definition: #fc
- Eine *deterministische* [[../../../Theo I/Turingmaschinen|TM]], die folgende Eigenschaften erfüllt:
	- *Read-Only Eingabeband*
	- *logarithmisch beschränkten Arbeitsband*
	- *Write-Only Ausgabeband*, auf dem der Schreib-/Lesekopf *nicht nach links bewegt* werden kann
	-> Annahme: Der Transducer stoppt nach endlich vielen Schritten
- Die Funktion $f:\Sigma^.\rightarrow\Sigma^.$ ist *logspace-berechenbar*, wenn es einen Logspace-Transdurcer $M$ gibt, der $f$ auf dem Ausgabeband berechnet
-> [[../Logspace-Reduktion|Logspace-Reduktion]]
^1660503035406
