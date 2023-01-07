---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Satz Von Savitch
linter-yaml-title-alias: Satz Von Savitch
date-of-creation: 2022-08-12
mod-date: 2022-10-24
---

# Satz Von Savitch

## Definition: #fc
- Sei $s\in\Omega(\log n)$, dann gilt: $$NSPACE(s)\subseteq DSPACE(s^2)$$
- Das Gegenstück fehlt für die [[../Zeitkomplexität|Zeitkomplexität]]
^1660502972256

## Beweis:
- Annahme: $s$ ist [[../Konstruierbarkeit|platzkonstruierbar]]
- Sei $M$ eine nichtdeterministische [[../../../Theo I/Turingmaschinen|TM]], deren Platzbedarf von $s$ beschränkt ist
- $\text{Conf}(M,w):$ Die Menge aller Konfigurationen $\alpha$ der Größe $\leq s(|w|)$
- $\text{Conf}(M,w)$ hat genau eine akzepierende Konfiguration $\alpha_f$
- $Reach(\alpha,\beta,i)\Leftrightarrow\exists k\leq 2^i\text{ Schritten}$
	→ Rekursive Berechnung: $Reach(\alpha,\beta,i)\Leftrightarrow\exists\gamma\in Conf(M,w):$$Reach(\alpha,\gamma,i-1)\wedge Reach(\gamma,\beta,i-1)$
→ $\gamma$ lässt sich nicht raten, daher müssen alle möglichen Gammas durchprobiert werden:
```
FUNCTION Reach(α, β, i): BOOLEAN;
	b := FALSE;
	IF i = 0 THEN b := [α = β OR α \vdash β]
	ELSE FORALL γ ∊ Conf(M, w) DO
		IF (NOT b) AND Reach(α, γ, i − 1) THEN //Platz des Reach-Aufrufs wird für den folgenden Aufruf wiederverwendet
			b := Reach(γ, β, i−1);
	RETURN b
END FUNCTION
```
→ Der Gesamtplatzbedarf liegt in aufgrund der zwei rekursiven Aufrufe in $\mathcal{O}(s(|w|)^2)$
- Die Platzkonstruierbarkeit ist nicht notwendig, da man mit dem Reach-Prädikat in einem Vorab-Durchlauf testen kann, wie hoch der benötigte Platz ist
	→ Hochzählen von $n$ und immer wieder prüfen, ob eine Konfiguration dieser Länge (mit $n=\text{Startkonfiguration}$) erreicht werden kann

## Folgerungen: #fc
- [[../Probleme/Grapherreichbarkeitsproblem|GAP]] $\in DSPACE(\log^2(n))$
- [[PSPACE|PSPACE]] $=\bigcup_{1\leq k}NSPACE(n^k)=\bigcup_{1\leq k}DSPACE(n^k)$
^1660502991756
