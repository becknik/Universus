---
tags: uni theo-2 theoretical-cs computability abstraction
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Entscheidbarkeit
  - entscheidbar
  - unentscheidbar
  - entscheidet
  - REC
linter-yaml-title-alias: Entscheidbarkeit
date-of-creation: 2022-07-03
mod-date: 2022-10-24
---

# Entscheidbarkeit

## Definition: #fc
- Eine Menge $A$ ist *entscheidbar*, wenn ihre charakteristische Funktion $$\chi_A(w\in\Sigma^{Stern})=1,\text{ falls }w\in A,0 \text{ falls }w\notin A$$ [[Berechenbarkeit|berechenbar]] ist.
	→ $\chi_A$ muss *total* und [[../Maths I/Wohldefiniertheit|wohldefiniert]] sein
- Eine Menge $A$ ist *semi-entscheidbar*, wenn die (co-)semi-charakteristische Funktion $\chi_A'/\chi_\overline{A}'=1,\text{ falls }w\in A/w\notin A, \text{ sonst }\bot$ *berechenbar* ist
	→ Theo-I Terminus: Die Menge $A$ wird *akzeptiert*, wenn eine semi-charakteristische Funktion für $A$ existiert
	→ Semi-entscheidbare Sprachen liegen in [[Entscheidbarkeit/Rekursiv Aufzählbar|RE]], co-semi-entscheidbare in $co\text{RE}$
^1661250083685

## Eigenschaften:  #fc
- Entscheidbare Sprachen liegen in der [[Komplexitätsklassen|Komplexitätsklasse]] $\text{R}=\text{RE}\cap co\text{RE}$[^1]
- semi-entscheidbar $=$ [[Entscheidbarkeit/Rekursiv Aufzählbar|rekursiv aufzählbar]] $= \text{RE}$[^1]
	→ $L\in\text{R}\Rightarrow L\in\text{RE}$
- Die Struktur der unentscheidbaren Sprachen ist gut verstanden, die der entscheidbaren eher so "mittel-gut"
![[_Figures/Entscheidbarkeit-Sprachen-Skizze.png|250]]
^1662847113133

## Äquivalenzen Für $A\subseteq\Sigma^{Stern}$: #fc
- $A$ ist *semi-entscheidbar*
- $A$ ist [[Entscheidbarkeit/Rekursiv Aufzählbar|rekursiv aufzählbar]] = $A\in\text{RE}$
- $A$ ist vom [[../Theo I/Typ-0|Typ-0]]
- $A = T(M)$ für eine [[../Theo I/Turingmaschinen|TM]] M
- $\chi_A'$ ist berechenbar
- $A$ ist der Definitionsbereich einer [[Berechenbarkeit|berechenbaren Funktion]]
- $A$ ist der Wertebereich einer [[Berechenbarkeit|berechenbaren Funktion]]
	→ Beweis über [[Entscheidbarkeit/Dove-Tailing|Dove-Tailing]] zu [[Entscheidbarkeit/Rekursiv Aufzählbar|Rekursiv Aufzählbar]]
^1660502472006

[^1]:[Wikipedia: R](<https://en.wikipedia.org/wiki/R_(complexity)>) (23.08.2022)
