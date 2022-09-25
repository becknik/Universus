---
tags: uni theo-1 theoretical-cs chomsky
cards-deck: Uni::Courses::Theo-I
complete: true
aliases: Erkennung durch Monoide
linter-yaml-title-alias: Erkennung durch Monoide
date: 2022-09-20
mod-date: 2022-09-20
---

# Erkennung durch Monoide
-> V.9 F.17.2

## Definition:
- Sei $L$ eine [[../Formale Sprache|formale Sprache]] und $M$ ein [[../Monoid|Monoid]], dann schreiben wir $M$ erkennt $L$, wenn $A\subseteq M$ und ein [[Homomorphismus]] $\varphi:\Sigma^*\rightarrow M$ existieren, so dass $$w\in L\quad\Leftrightarrow\quad\varphi(w)\in A$$ gilt


## Eigenschaften:
- Eine [[../Formale Sprache|formale Sprache]] $L$ heißt *erkennbar*, wenn sie durch ein endliches [[../Monoid|Monoid]] erkannt wird
- Für jede [[../Formale Sprache|formale Sprache]] $L\subseteq\Sigma^*$ sind die folgenden Aussagen äquivalent:
	1. $L$ ist eine [[../Typ-3|reguläre Sprache]]
	2. $L$ ist erkennbar
	3. $Synt(L)<\infty$
