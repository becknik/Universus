---
tags: uni theo-1 theoretical-cs
cards-deck: Uni::Courses::Theo-I
complete: true
aliases: Myhill-Nerode Äquivalenz
linter-yaml-title-alias: Myhill-Nerode Äquivalenz
date: 2022-09-20
mod-date: 2022-09-20
---

# Myhill-Nerode Äquivalenz

## Definitionen:
- Die Äquivalenzrelation $R_L$ sei für eine [[../Grundlegendes/Formale Sprache|formale Sprache]] $L$ definiert als $$x~R_L~y\quad\Longleftrightarrow\quad[\forall w\in\Sigma^*:~xw\in L\Leftrightarrow ~yw\in L]$$
	-> Die Relation ist *reflexiv*, *symmetrisch* und *transitiv*
- Sei $L\in\text{REG}\Rightarrow\exists$ ein [[Deterministischer Endlicher Automat|DFA]] $M$ mit $L=T(M)$ und die Äquivalenzrelation $R_M$ ist definiert als $$x~R_M~y\quad\Longleftrightarrow\quad\hat{\delta}(z_0,x)=\hat{\delta}(z_0,y)$$
-> $R_M$ verfeinert $R_L:\quad x~R_M~y\Rightarrow\forall w:\hat{\delta}(z_0,xw)=\hat{\delta}(z_0,yw)\Rightarrow x~R_L~y$
-> $\forall$ Äquivalenzklasse $C$ gilt $C\in R_M\Rightarrow C\in R_L$

## Aussage:
- Eine Sprache $L\subseteq\Sigma^*$ ist genau dann [[../Typ-3|regulär]], wenn der *Index der Äquivalenzrelation* $R_L$ *endlich* ist
	-> Index von $R_L:$ Die Anzahl der Äquivalenzklassen in $R_L$ für  $\forall w\in L$

## Eigenschaften:
- Für den eindeutig bestimmten, [[Minimalautomat|minimalen]] [[Deterministischer Endlicher Automat|DFA]] $M_0=(V,\Sigma,\delta,z_0,E)$ gilt: $|V|=$ Index von $R_L$
	-> *Im Allgemeinen* existiert kein eindeutig bestimmter, minimaler [[Nichtdeterministischer Endlicher Automat|NFA]] für eine gegebene [[../Typ-3|reguläre Sprache]]

## Beispiele:
- $L=\{a^n\mid a\text{ ist eine Quadratzahl}\}:$
	-> Zwei verschiedene unär kodierte Quadratzahlen $a^r,a^s,s\neq r$ mit $r,s\in\mathbb{N}$ liegen immer in unterschiedlichen Äquivalenzklassen, da immer $\exists x\in\Sigma^*$, sodass $a^rx\in L,$ aber $a^sx\notin L$
	-> $R_L$ hat einen unendlichen Index
- $L=\{x\in\{a,b\}^*\mid x\text{ enthält }abb\}:$
	-> $R_L$ hat den Index 4 mit $[\varepsilon],[a],[ab],[abb],$ da man an Wörter mit diesen Suffixen jeweils dieselben $x\in\Sigma^*$ hängen kann, damit die Kompositionen wieder $\in L$ sind
- $L=\{x\in\{a,b,c\}^*\mid|x|_a-|x|_b\equiv3\mod5\}:$
	-> $R_L$ hat den Index 5, da sich an $x,y\in\Sigma^*$ mit $|x|_a=|y|_a$ natürlich immer dieselbe Anzahl an $a$ Anhängen lassen, damit sie $\in L$ sind
	-> Falls $|x|_a\neq|y|_a$ gilt, stehen die Wörter auch nicht in Relation zueinander
