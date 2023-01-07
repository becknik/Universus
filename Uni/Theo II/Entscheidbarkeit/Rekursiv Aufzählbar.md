---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Rekursiv Aufzählbar
  - RE
  - akzeptiert	
linter-yaml-title-alias: Rekursiv Aufzählbar
date-of-creation: 2022-07-03
mod-date: 2022-09-11
---

# Rekursiv Aufzählbar

## Definition: #fc
- $A\subseteq\Sigma^{Stern}$ ist genau dann *rekursiv aufzählbar*, wenn A = $\emptyset\wedge\exists f:\mathbb{N}\rightarrow\Sigma^{Stern}$ total und [[Berechenbarkeit|berechenbar]], sodass gilt:
$$A=\{f(n)\mid n\in \mathbb{N}\}$$
→ "Kommt nicht von Rekursion, sondern eher von [[../Berechenbarkeit|Berechenbarkeit]]"
^1660502812109

## Eigenschaften: #fc
- [[Rekursiv Aufzählbar]] $\text{RE}\subsetneq\text{R}$ Aufzählbar (hier muss $f$ nicht berechenbar sein)
	→ Zum Beispiel ist $\Sigma^{Stern}$ ist rekursiv aufzählbar, aber $\exists A\subsetneq\Sigma^{Stern}:A$ ist nicht rekursiv aufzählbar
- Semi-Entscheidbar $=\text{RE}$
	→ Beweis über [[Dove-Tailing|Dove-Tailing]] (F.14.5)
	- Die Klasse $\text{RE}$ entspricht der Klasse der [[../../Theo I/Typ-0|Typ-0 Sprachen]] und damit der Menge von [[../Entscheidbarkeit|semi-entscheidbarer]] Sprachen
- $\forall |A|<\infty:A\in$ Rekursiv aufzählbar[^1]
- $\text{RE}$-vollständige Probleme: [[../Halteprobleme|Halteprobleme]], [[Satz von Rice|Satz Von Rice]], [[../Komplexitättheorie/Probleme/Postsches Korrespodenzproblem|PCP]][^2]
- Entspricht der Menge von Sprachen, für die eine beliebige [[../../Theo I/Grammatik|Grammatik]] existiert
^1660502812117

[^1]:[Wikipedia: RE German](https://de.wikipedia.org/wiki/Rekursiv_aufz%C3%A4hlbare_Menge#Eigenschaften)
[^2]:[Wikipedia: RE-complete](<https://en.wikipedia.org/wiki/RE_(complexity)#RE-complete>)
