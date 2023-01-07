---
tags: uni theo-1 theoretical-cs automata algorithm
cards-deck: Uni::Courses::Theo-I
completed: true
aliases: Potenzmengenkonstruktion
linter-yaml-title-alias: Potenzmengenkonstruktion
date-of-creation: 2022-09-15
mod-date: 2022-09-20
---

# Potenzmengenkonstruktion

## Funktionsweise: #fc
- Gegeben: Ein [[Nichtdeterministischer Endlicher Automat|NFA]] $M$
- Gesucht: Ein zu $M$ gleichwertiger [[Deterministischer Endlicher Automat|DEA]]
1. Erstelle zu jedem $z,z'\subseteq Z$ mit $\forall x\in\Sigma,\delta(z,x)=z'$ im NFA einen Zustand $z$ und $z'$ mit entsprechenden gerichteten Kanten im DFA
	→ Zur Verdeutlichung, dass $z,z'$ Mengen sind, werden sie auch im DFA als solche notiert
^1664630935260

## Eigenschaften: #fc
- *Exponentieller Blow-Up*: $\exists$ [[Nichtdeterministischer Endlicher Automat|NFAs]] mit der Eigenschaft, dass jeder äquivalente DFA *exponentiell viele Zustände* haben muss
	→ Beispiel: Der NFA zu $L_k=\{xay\mid x,y\in\{a,b\}^{Stern}\wedge|y|=k-1\}$ hat $k+1$ Zustände, der zugehörige DFA hingegen $2^k$
^1664630943560
