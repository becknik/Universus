---
tags: uni theo-1 theoretical-cs abstraction complexity formal-languages chomsky
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Chomsky-Hierarchie
  - Sprachklassen
linter-yaml-title-alias: Chomsky-Hierarchie
date-of-creation: 2022-09-13
mod-date: 2022-09-20
---

# Chomsky-Hierarchie
![[_Figures/Chomsky-Hiarchie-Spachen-Überblick.png|400]]
[CC Carlos Camino, SS2020, source:](https://fmi.uni-stuttgart.de/files/ti/teaching/s20/ti2/erg/z06.pdf)

## Definition: #fc
- Die Klassifizierung orientiert sich an der Regelmenge der [[Grammatik|Grammatik]] $G$
  → Da jede Grammatik eine [[Formale Sprachen|formale Sprache]] beschreibt, wird die Klassifizierung auch auf Sprachklassen und nicht nur Grammatiken verwendet 
- Da es sich um eine Hierarchie handelt, gilt:$$\text{Typ-0}\subsetneq\text{Typ-1}\subsetneq\text{Typ-2}\subsetneq\text{Typ-3}$$
- [[Typ-0]]: *Beliebige* Grammatiken/ Allgemeine Phrasenstrukturgrammatiken
	→ Jede existierende Grammatik ist vom Typ-0
	→ [[../Theo II/Entscheidbarkeit/Rekursiv Aufzählbar|RE]]
- [[Typ-1]]: *Kontextsensitive*/*Nichtverkürzende* Grammatiken
	→ Definiert durch $(u,v)\in P$ wobei $|u|\leq|v|$ gilt
	→ Ab diese Klasse gilt die [[1. Typ - CSL/ε-Sonderregel|ε-Sonderregel]]
- [[Typ-2]]: *Kontextfreie* Grammatiken
	→ Definiert durch $G\in\text{CSL/Typ-1}$ und $(u,v)\in P_G$ wobei $u\in V_G$ ist
- [[Typ-3]]: *Reguläre*/ *Rechtslineare* Grammatiken
	→ Definiert durch $G\in\text{CFL/Typ-2}$ und $(u,v)\in P_G,$ wobei $v\in\Sigma\cup\Sigma V$ gilt
^1664630657037

## Eigenschaften:
- [[Abschlusseigenschaften]]
- [[Entscheidbarkeitsprobleme für Sprachklassen]]
- [[../Theo II/Unentscheidbare Probleme|Unentscheidbare Gammatik-Probleme]]
