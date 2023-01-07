---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Konstruierbarkeit
  - Platzkonstruierbarkeit
  - platzkonstruierbar
  - Zeitkonstruierbarkeit
  - zeitkonstruierbar
linter-yaml-title-alias: Konstruierbarkeit
date-of-creation: 2022-10-24
mod-date: 2022-10-24
---

# Konstruierbarkeit

## Platz

### Definition: #fc
- Die Funktion $f:\mathbb{N}\rightarrow\mathbb{N}$ mit $f\in\Omega(\log n)$ ist *platzkonstruierbar*, falls $\exists$ [[../../../Theo I/Turingmaschinen|DTM]] $M$, die auf der Eingabe $a^n$ ($n$ ist unär kodiert) genau $f(n)$ *Felder markiert* und *den markierten Platz nicht verlässt*
- Aussage: Es existiert ein "*Platzzähler*" für $M$
^1660502938355

## Zeit

### Definition: #fc
- Die Funktion $f:\mathbb{N}\rightarrow\mathbb{N},f\in\Omega(n)$ ist *zeitkonstruierbar*, wennfalls$\exists$ [[../../../Theo I/Turingmaschinen|DTM]], die auf der Eingaben $a^n$ ($n$ ist unär kodiert) nach genau $f(n)$ Schritten hält
- *Aussage*: Es existiert eine "*Stopuhr*" für $M$, die während der Berechnung läuft
^1660862516425
