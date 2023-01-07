---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Grapherreichbarkeitsproblem
  - GAP
date-of-creation: 2022-07-10
mod-date: 2022-08-18
linter-yaml-title-alias: Grapherreichbarkeitsproblem
---

# Grapherreichbarkeitsproblem

## Definition:
- *Gegeben*: Ein [[../../../DSA/Graphen/Gerichtete Graphen|gerichteter Graph]] $G=(V,E)$ und zwei Knoten $s,t\in V$
- *Gesucht*: Gibt es in $G$ einen Pfad von $s$ nach $t$ ?

## Eigenschaften:
- $GAP\in$ [[../Zeitklassen/P|P]]
- $GAP\in$ [[../Platzklassen/NL|NL]]
  → [[Satz von Savitch]]: $GAP \in DSPACE(\mathcal{O}(\log^2 n))$

## Algorithmus:
```
v := s;
WHILE v 6= t DO
	Wähle nichtdeterministisch w ∊ V mit (v, w) ∊ E ;
	v := w
ENDWHILE;
OUTPUT: Es existiert ein Weg von s nach t
```

## Beweis Der NL-Härte:
- Sei $A\in NL,$ dann gibt es eine logspace-beschränkte [[../../../Theo I/Turingmaschinen|NTM]] $M$ mit $L(M)=A$
- Jedem Input $w\in\Sigma^{Stern}$ wird eine Gap-Instanz $f(w)=(G,s,t)$ zugeordnet
- Sei $G=(V,E):$
	- $V=\{\alpha\mid$ ist Konfiguration von $M$ bei Eingabe $w$ mit $|\alpha|\leq\log(|w|)$
	- $E=\{\{\alpha,\beta\}\in V\times V\mid\alpha\vdash_M\beta\}$
	- $s=$ Die Anfangskonfiguration von $M$ bei der Eingabe $w$
	- $t=$ Eine akzeptierende Konfiguration von $M$
- Die Abbildung $w\rightarrow(G,s,t)$ kann leicht mit logarithmischen Platzaufwand berechnet werden
- $w\in A\Leftrightarrow f(w)\in GAP:$ Der Rechenweg von $M$ und der Weg im Graph $G$ stehen in 1:1 Korrespondenz
