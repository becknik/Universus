---
tags: uni theo-1 theoretical-cs chomsky
cards-deck: Uni::Courses::Theo-I
completed: true
aliases: Syntaktisches Monoid
linter-yaml-title-alias: Syntaktisches Monoid
date-of-creation: 2022-09-25
mod-date: 2022-09-25
---

# Syntaktisches Monoid

## Definition: #fc
- Das Quotienten-[[../Monoid|Monoid]] wird als $\Sigma^{Stern}\setminus\equiv_L$ notiert
	→ "Wir nennen es das *Syntaktisches Monoid* $Synt(L)$ der Sprache $L$ […]"
- Die Elemente des Quotientenmonoids entsprechen der Äquivalenzklassen der verfeinerten [[Myhill-Nerode|Myhill-Nerode Äquivalenz]]
^1664631017961

## Eigenschaften: #fc
- Für jede [[../Formale Sprachen|formale Sprache]] $L:Synt(L)$ erkennt $L$ durch den [[Homomorphismus]] $\varphi:w\mapsto[w]$
	→ $\varphi$ bildet also $\forall w\in L$ aus die zugehörigen Äquivalenzklassen der Kongruenz ab
> *Bei letzteren Folgepfeil handelt es sich um unsichere Mutmaßungen, anders macht es für mich allerdings keinen Sinn :/*
- $\forall L$ mit $Synt(L)<\infty:L$ ist eine [[../Typ-3|reguläre Sprache]] und von einem endlichen [[../Monoid|Monoid erkennbar]]
^1664631017964
