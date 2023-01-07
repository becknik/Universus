---
tags: uni dsa practical-cs indexstruct hash
cards-deck: Uni::Courses::DSA
completed: true
aliases: Hashfunktionen
linter-yaml-title-alias: Hashfunktionen
date-of-creation: 2022-07-24
mod-date: 2022-10-20
---

# Hashfunktionen

## Definition & Eigenschaften: #fc
- Eine Hashfunktion $S$ ist die *Abbildung aller Objektschlüssel* auf ein Array der Größe $p$
	→ $p$ sollte eine *große Primzahl* sein, die nicht nahe einer Zweierpotenz liegt
- $h: K \rightarrow S,\quad \text{z.B. }S=\{0,\dots,p-1\}$
	→ $S$ muss nicht aus Integer-Zahlen bestehen
- Die Bildmenge von $h$ muss *surjektiv* und ungefähr *gleichverteilt* sein, um Kollisionen zu vermeiden
	→ Gleichverteilung: $\forall 0 \leq m < p: |S_m=\{s \in S ~|~ f(s)=m\}| \approx \frac{|S|}{p}$
	→ Nicht *injektiv*, da die Bildmenge (meistens) kleiner als die Eingabemenge ist
- Die Funktion $h(s)$ sollte sich möglichst schnell berechen lassen
	→ Beispiel: $\heartsuit~h(s\in S)= s\pmod p~\heartsuit$ oder das [[Hashing/Multiplikationsverfahren|Multiplikationsverfahren]]
^1656414000461

## Varianten: #fc
- [[Hashing/Offenes Hashing|Offenes Hashing]]
- [[Hashing/Geschlossenes Hashing|Geschlossenes Hashing]]
- [[Hashing/Dynamisches Hashing|Dynamisches Hashing]]
^1656966568945
