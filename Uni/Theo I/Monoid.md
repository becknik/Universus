---
tags: uni theo-1 theoretical-cs formal-languages
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Monoid
  - freies Monoid
linter-yaml-title-alias: Monoid
date-of-creation: 2022-09-13
mod-date: 2022-10-31
---

# Monoid

## Definition #fc
- Ein Monoid ist eine *Menge* mit einer *assoziativen Verknüpfung* und einem *neutralen Element*
- Formalisiert: Ein Tripel, bestehend aus der *Menge* $M,$ einer *binären Verknüpfungs-Funktion* $M\times M\rightarrow M,(m,n)\mapsto m\circ n$ und einem *neutralen Element* $e$ bilden ein Monoid $(M,\circ,e)$, wenn sie folgende Eigenschaften besitzt:
	1. *Assoziativität*: $(n\circ m)\circ k=n\circ(m\circ k),\forall m,n,k\in M$
	2. Eigenschaft des neutralem Elements: $e\circ m=m\circ e=m,\forall m\in M$
→ Aus der binären Verknüpfungsfunktion folgt, dass $\forall m,n\in M:m\circ n\in M$ gelten muss
^1664630602391

### Das freie Monoid über $\Sigma$: #fc
- Die Menge der endlichen Zeichenketten, deren Zeichen $\in\Sigma$ sind, bilden mit der *Konkatenation* ein freies Monid $\Sigma^{Stern}$
	→ $\Sigma^{Stern}$ ist *abzählbar unendlich*
- Neurales Element: das [[Grundlegendes/Leeres Wort|leere Wort]] $\varepsilon$
^1664630602394

## Erkennbarkeit: #fc
- Die [[Formale Sprachen|formale Sprache]] $L$ wird von einem Monoid $(M,\circ,e)$ erkannt, wenn ein [[3. Typ - REG/Homomorphismus|Homomorphismus]] $\varphi:\Sigma^{Stern}\rightarrow\Sigma^{Stern}$ existiert, so dass das *Urbild* des Homomorphismus $\varphi,\varphi^{-1}=L$ ist
^1664630602396

> *Könne auch nicht stimmen… Ich bin mir bei dem Thema leider sehr unschlüssig*
