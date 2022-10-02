---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases:
  - Platzkonstruierbarkeit
  - platzkonstruierbar
date: 2022-08-13
mod-date: 2022-08-22
linter-yaml-title-alias: Platzkonstruierbarkeit
---

# Platzkonstruierbarkeit
-> [[../Zeitklassen/Zeitkonstruierbarkeit|zeitkonstruierbar]]

## Definition: #fc
- Eine Funktion $f:\mathbb{N}\rightarrow\mathbb{N}$ mit $f\in\Omega(\log n)$ ist **platzkonstruierbar**, wenn $\exists$ [[../../../Theo I/Turingmaschinen|deterministische Turingmaschine]] $M$, die auf der Eingabe $a^n$ ($n$ ist unär kodiert) genau $f(n)$ *Felder markiert* und *den markierten Platz nicht verlässt*
	-> $\exists$ "Platzzähler"
^1660502938355
