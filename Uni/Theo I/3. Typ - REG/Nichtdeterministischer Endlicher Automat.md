---
tags: uni theo-1 theoretical-cs automata
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Nichtdeterministischer Endlicher Automat
  - NEA
  - NFA
linter-yaml-title-alias: Nichtdeterministischer Endlicher Automat
date-of-creation: 2022-09-15
mod-date: 2022-09-21
---

# Nichtdeterministischer Endlicher Automat

## Definition: #fc
- Definiert durch ein ähnliches *5-Tupel* wie beim [[Deterministischer Endlicher Automat|DFA]], mit den folgenden Unterschieden:
$$M=(Z,\Sigma,\delta,S,F)$$
- $S:$ Die *Menge der Startzustände* $\subseteq Z$
- Die [[../Grundlegendes/Nichtdeterminismus|nichtdeterministische]] *Zustands-Überführungsfunktion* $\delta:Z\times\Sigma\rightarrow\mathcal{P}(Z)$
	→ Das Bild der Funktion ist eine *Menge*, zwischen dessen Elementen der Automat "wählen" kann
^1664630917785

## Zustandsüberführung: #fc
- Die *Verallgemeinerte Überführungsfunktion*: $\hat{\delta}:Z\times\Sigma^{Stern}\rightarrow\mathcal{P}(Z):$
	- $\hat{\delta}(Z',\varepsilon)=z\quad\forall Z'\subseteq Z$ "es passiert Nichts, wenn Nichts gelesen wird"
	- $\hat{\delta}(Z',ax)=\bigcup_{z\in Z'}\hat{\delta}(\delta(z,a),x)\quad\forall z\in Z,a\in\Sigma,x\in\Sigma^{Stern}$
	→ Der Automat kann prinzipiell alle Zustände $z\in Z'$ annehmen und kann selbst entscheiden, welchen (="Nichtdeterminismus")
^1664630917788

## Eigenschaften: #fc
- Die vom NFA $M$ akzeptierte Sprache $T(M)=\{w\in\Sigma^{Stern}\mid\hat{\delta}(S,w)\cap F\neq\emptyset\}$
- Werden häufig als markierte, [[../../DSA/Graphen/Gewichteter Graph|gewichtete Graphen]] dargestellt
- Dürfen $\varepsilon$-Übergänge enthalten
^1664630926687

## Theoreme & Algorithmen:
- [[Satz von Rabin und Scott]]
- [[Potenzmengenkonstruktion]]
