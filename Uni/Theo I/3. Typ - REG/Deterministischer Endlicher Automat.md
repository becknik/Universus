---
tags: uni theo-1 theoretical-cs automata chomsky
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Deterministischer Endlicher Automat
  - DEA
  - DFA
linter-yaml-title-alias: Deterministischer Endlicher Automat
date-of-creation: 2022-09-15
mod-date: 2022-10-31
---

# Deterministischer Endlicher Automat

## Definition: #fc
- Definiert durch das *5-Tupel*:
$$M=(Z,\Sigma,\delta,z_0,F)$$
- $Z:$ Die endliche *Zustandsmenge*
- $\Sigma:$ Die *endliche* Menge der *Alphabetssymbole*
	→ $\Sigma\cap Z=\emptyset$
- $z_0:$ Der *Startzustand* $\in Z$
- $F:$ Die Menge der *akzeptierenden Endzustände* $\subseteq Z$
- Die [[../Grundlegendes/Determinismus|deterministische]] *Zustandsüberführungsfunktion* $$\delta:Z\times\Sigma\rightarrow Z,\quad\delta(z\in Z,\sigma\in\Sigma)=z'\in Z$$
	→ $z$ und $z'$ müssen nicht zwingend verschiedene Zustände sein
^1664630729710

## Zustandsüberführung: #fc
- Die *verallgemeinerte Überführungsfunktion*: $\hat{\delta}:Z\times\Sigma^{Stern}\rightarrow Z:$
	- $\hat{\delta}(z,\varepsilon)=z\quad\forall z\in Z\quad$"Es passiert Nichts, wenn Nichts gelesen wird"
	- $\hat{\delta}(z,ax)=\hat{\delta}(\delta(z,a),x)\quad\forall z\in Z,a\in\Sigma,x\in\Sigma^{Stern}$
^1664630729718

## Eigenschaften: #fc
- Die vom DFA $M$ akzeptierte Sprache ist definiert als $T(M)=\{w\in\Sigma^{Stern}\mid\hat{\delta}(z_0,w)\in F\}$
- Jede von einem DFA akzeptierte Sprache $L$ ist eine [[../Typ-3|Typ-3 Sprache]]
	→ Beweis: DFA → Typ 3
- Wird häufig als markierter, [[../../DSA/Graphen/Gerichtete Graphen|gerichteter Graph]] dargestellt
	→ Dieser kann keine $\varepsilon$-Übergänge aufweisen
- Können durch einen einfachen [[../../DSA/Algorithmen/Muster/Backtracking|Backtracking-Algorithmus]] in [[Minimalautomat|Minimalautomaten]] umgewandelt werden
- Arbeitet in [[../../Theo II/Komplexitättheorie/Zeitklassen/TIME|Realzeit]], die [[Potenzmengenkonstruktion|Potenzmengenkonstruktion]] (ohne Tricks für Umwandlung von [[Reguläre Ausdrücke|regulären Ausdrücken]] in DEAs notwendig) fällt hingegen etwas aufwändiger aus
^1664630729721

## Theoreme:
- [[Satz von Rabin und Scott]]
