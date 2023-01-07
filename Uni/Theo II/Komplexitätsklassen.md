---
tags: uni theo-2 theoretical-cs complexity abstraction chomsky formal-languages
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Komplexitätsklassen
linter-yaml-title-alias: Komplexitätsklassen
date-of-creation: 2022-07-10
mod-date: 2022-10-24
---

# Komplexitätsklassen
→ [[Komplexitättheorie/Zeitkomplexität|Zeitkomplexität]], [[Komplexitättheorie/Platzkomplexität|Platzkomplexität]]

## Definition:
- [[../Theo I/Formale Sprachen|Formale Sprachen]] entsprechen *Mengen von Problemen*
![[_Figures/Chompsky-Hirarchie-Halteprobleme.png|Carlos z07]]
[CC Carlos Camino, SS2020, source:](https://fmi.uni-stuttgart.de/files/ti/teaching/s20/ti2/erg/z07.pdf)

## Große offene Probleme:
- $\text{NSPACE}(n) =\text{DSPACE}(n)?$
- *P-NP-Problem*: $\text{NP}=\text{P}?$

## Beziehungen: #fc
→ Von oben nach unten $\subseteq/\subsetneq$
- [[../Theo I/Typ-0|Typ-0]] = $\text{R}=\text{RE}\cap co\text{RE}$
- $\text{EXPTIME}$
- [[Komplexitättheorie/Platzklassen/PSPACE|PSPACE]] $= \bigcup_{k \geq 1}\text{DSPACE}(n^k)=\bigcup_{k\geq 1} \text{NSPACE}(n^k)$
- [[Komplexitättheorie/Zeitklassen/NP|NP]] $= \bigcup_{k \geq 1}\text{NTIME}(n^k)\quad\mid\quad co\text{NP}:=\{L\subseteq\Sigma^{Stern}\mid\overline{L}\in\text{NP}\}$
- $co\text{NP}\cap\text{NP}$
- [[Komplexitättheorie/Zeitklassen/P|P]] $= \bigcup_{k \geq 1}\text{DTIME}(n^k)$[^1]
- [[Komplexitättheorie/Platzklassen/NL|NL]] $=\text{NSPACE}(\log n)$[^1]
- [[Komplexitättheorie/Platzklassen/L|L]] $=\text{DSPACE}(\log n)$[^1]
[^1]: Als lösbar betrachtet
- Probleme in [[Komplexitättheorie/Zeitklassen/NP|NP]], [[Komplexitättheorie/Platzklassen/PSPACE|PSPACE]], [[Komplexitättheorie/Zeitklassen/EXPTIME|EXPTIME]] und [[Entscheidbarkeit/Rekursiv Aufzählbar|RE]] werden als nicht lösbar betrachtet
![[_Figures/Komplexitätsklassen-Beziehungen.png]]
[source:GitHub SerenGTI, GNU GLP3](https://github.com/SerenGTI/Theo_Inf/blob/master/Klausurzettel%20Theo%202/graph.png)
^1660502369712

### Nicht-/Determinismus: #fc
- $\forall f:\mathbb{N}\rightarrow\mathbb{N}$ mit $\forall n:n\leq f(n):$
$$\text{DTIME}(f)\subseteq\text{NTIME}(f)\subseteq\text{DSPACE}(f)$$
- $\forall f:\mathbb{N}\rightarrow\mathbb{N}$ mit $\forall n:\log n\leq f(n):$
$$\text{DSPACE}(f)\subseteq\text{NSPACE}(f)\subseteq\text{DTIME}(2^{\mathbfcal{O}(f)})$$
- Folgerungen:
	- $\text{L}\subseteq\text{NL}\subseteq\text{P}=\text{DSPACE}(2^{\mathbfcal{O}(\log n)})$
	- $\text{P}\subseteq\text{PSPACE}\subseteq\text{DTIME}(2^{\mathbfcal{O}(n^k)})=\text{EXPTIME}$
	- $\text{CSL}=\text{LBA}=\text{NSPACE}(n)\subseteq\text{DTIME}(2^{\mathbfcal{O}(n)})$
^1660502369715
