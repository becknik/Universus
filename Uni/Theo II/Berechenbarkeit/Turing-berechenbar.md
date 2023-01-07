---
tags: uni theo-2 theoretical-cs computability trait 
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Turing-berechenbar
date-of-creation: 2022-08-06
mod-date: 2022-08-06
linter-yaml-title-alias: Turing-berechenbar
---

# Turing-berechenbar
→ [[../../../Theo I/Turingmaschinen|TM]]

## Definition:
- Eine Funktion $f: \mathbb{N}^k \rightarrow \mathbb{N}$ heißt *Turing-berechenbar*, falls eine [[../../../Theo I/Turingmaschinen|deterministische Turingmaschine]] $M$ existiert, so dass das Ergebnis von $f(n_1,\dots,n_k)$ nach endlich vielen Schritten auf dem Band von $M$ steht
- Die DTM $M$ startet im *Anfangszustand* mit dem Kopf auf dem ersten Zeichen auf dem mit dem $k$-Tupel $(n_1,\dots,n_k)$ in *Binärdarstellung* mit *Trennzeichen* zwischen den Komponenten beschriebenen *Eingabeband*
	→ Wenn die Funktion $f$ nicht *total* ist, dann läuft $M$ für diese undefinierten Werte unendlich lange

## Beispiele:
- $f(a,b)=a+b$
- $g(a,b)=a-b$
- $h(a,b)=a\cdot b$
- $i(a,b)=\lfloor \frac{a}{b} \rfloor, b \neq 0, i(a,0)=a$
