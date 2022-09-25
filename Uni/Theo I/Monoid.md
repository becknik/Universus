---
tags: uni theo-1 theoretical-cs formal-languages
cards-deck: Uni::Courses::Theo-I
complete: true
aliases:
  - Monoid
  - freies Monoid
linter-yaml-title-alias: Monoid
date: 2022-09-13
mod-date: 2022-09-25
---

# Monoid

## Definition
- Ein Monoid ist eine *Menge* mit einer *assoziativen Verknüpfung* und einem *neutralen Element*
- Formalisiert: Ein Tripel, bestehend aus der *Menge* $M,$ einer *binären Verknüpfungs-Funktion* $M\times M\rightarrow M,(m,n)\mapsto m\circ n$ und einem *neutralen Element* $e$ bilden ein Monoid $(M,\circ,e)$, wenn sie folgende Eigenschaften besitzt:
	1. *Assoziativität*: $(n\circ m)\circ k=n\circ(m\circ k),\forall m,n,k\in M$
	2. Eigenschaft des neutralem Elements: $e\circ m=m\circ e=m,\forall m\in M$
-> Aus der binären Verknüpfungsfunktion folgt, dass $\forall m,n\in M:m\circ n\in M$ gelten muss

## Das freie Monoid über $\Sigma$:
- Die Menge der endlichen Zeichenketten, deren Zeichen $\in\Sigma$ sind, bilden mit der *Konkatenation* ein freies Monid $\Sigma^*$
	-> $\Sigma^*$ ist *abzählbar unendlich*
- Neurales Element: das [[Grundlegendes/Leeres Wort|leere Wort]] $\varepsilon$

## Erkennbarkeit:
- Die [[Formale Sprache|formale Sprache]] $L$ wird von einem Monoid $(M,\circ,e)$ erkannt, wenn ein [[3. Typ - REG/Homomorphismus|Homomorphismus]] $\varphi:\Sigma^*\rightarrow\Sigma^*$ existiert, so dass das *Urbild* des Homomorphismus $\varphi,\varphi^{-1}=L$ ist
> Könne nicht stimmen… Ich bin mir bei dem Thema leider sehr unschlüssig
