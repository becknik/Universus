---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
complete: true
aliases:
  - Binomialkoeffizient
  - Fakultät
linter-yaml-title-alias: Binomialkoeffizient
date: 2022-11-02
mod-date: 2022-11-02
---

# Binomialkoeffizient

## Definition: #fc
- Seien $n\in\mathbb{N}$ und $k\in\mathbb{N}_0,$ so beschreibt $\binom{n}{k}$ die Anzahl der [[Mengenlehre|Teilmengen]] von $\{1,\dots,n\}$ mit genau $k$ Elementen
	-> Für $n=k=0:\binom{0}{0}=1$
	-> Für $n=,k\geqslant0:\binom{0}{0}=0$
- Die Symbole $\binom{n}{k}$ heißen *Binomealkooefizienten*
^1667418056521

## Pascal-Dreieck: #fc
- $\forall n,k\in\mathbb{N}$ gilt: $$\binom{n}{k}=\binom{n-1}{k-1}+\binom{n-1}{k}$$
^1667418056528

## Fakultät: #fc
- Für alle $m\in\mathbb{N}$ heißt $m!=1\cdot2\cdot3\cdot\dots\cdot m$ Fakultät von $m$
	-> Konvention: $0!:=1$
- $\forall n,k\in\mathbb{N}$ mit $0\leqslant k\leqslant n$ gilt: $$\binom{n}{k}=\frac{n!}{k!(n-k)!}$$
^1667418135047
