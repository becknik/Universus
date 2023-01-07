---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Logspace-Transducer
  - logspace-berechenbar
linter-yaml-title-alias: Logspace-Transducer
date-of-creation: 2022-08-12
mod-date: 2022-10-24
---

# Logspace-Transducer

## Definition: #fc
- Eine [[../../../Theo I/Turingmaschinen|DTM]] ist ein *Logspace-Transducer*, wenn sie die folgenden Eigenschaften erfüllt:
	1. Sie besitzt ein *Read-Only Eingabeband*
	2. Das *Arbeitsband* ist *logarithmisch beschränkt*
	3. Sie weist ein *Write-Only Ausgabeband* auf, auf dem der *Schreib-/ Lesekopf* sich *nicht nach links bewegt* werden kann
- *Annahme*: Der Transducer stoppt nach endlich vielen Schritten
^1660503035406

### Logspace-Berechenbarkeit:
- Die Funktion $f:\Sigma^.\rightarrow\Sigma^.$ ist *logspace-berechenbar*, wenn es einen Logspace-Transdurcer $M$ gibt, der $f$ auf dem Ausgabeband berechnet
	→ [[../Logspace-Reduktion|Logspace-Reduktion]]
