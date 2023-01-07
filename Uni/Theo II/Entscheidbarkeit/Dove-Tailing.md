---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Dove-Tailing
linter-yaml-title-alias: Dove-Tailing
date-of-creation: 2022-07-03
mod-date: 2022-10-24
---

# Dove-Tailing

## Prinzip: #fc
- Annahme: $\exists$ Baum mit potentiell unendlich langen Pfaden
	→ Ein Einsatz der [[../../DSA/Graphen/Algorithmen/Breitensuche|Breitensuche]] würde kein Problem darstellen, die [[../../DSA/Graphen/Algorithmen/Tiefensuche|Tiefensuche]] hingegen schon
- Annahme: Der Baum besteht aus unendlich vielen potentiell unendlichen Programmen
	→ Weder die DFS, noch die BFS würde einen Fortschritt in allen Programmen garantieren
- Vorgehen:
	1. Schritt des 1. Programms wird ausgeführt
	2. Schritt des 1. Programms und 1. Schritt des 2. Programms werden ausgeführt
	3. Schritt des 1. Programms, 2. Schritt des 2. Programms und 1. Schritt des 3. Programms werden ausgeführt
	→ Es entsteht eine Schwalben-Schweif ähnliche Struktur
^1660502782405

## Algorithmus: #fc
```
Σ^*={w_1,w_2,...} längenlexikographisch anordnen
FOR i = 0,1,2,... DO
	Simuliere i Schritte von M_w auf Eingabe e(i)
	Kriterium
END
```
^1666645550265

## Beweis:
- Voraussetzungen:
	- $A \subseteq \mathbb{N}, A \neq \emptyset$
	- $a \in A$ beliebig und fest
	- $\chi_A'$ berechenbar
- Definition einer Funktion $f:\mathbb{N} \rightarrow \mathbb{N}$ mit $A = f(\mathbb{N})$
- $c(n,t)=m$
- $f(m) = n$, falls $\chi_A'(n)$ in höchstens $t$ Schritten terminiert und 1 ausgibt
	→ Für genügend große $t$ terminiert $\chi_A'(n \in A)$ nach maximal $t$ Schritten, d.h. für ein solches $t$ $f(c(n,t))=n$
- Sonst $f(m) = a$
	→ $f$ ist eine *totale Funktion*, für die $f(\mathbb{N}) \subseteq A \wedge A \subseteq f(\mathbb{N})$ gilt

### Quellen:
- [Wikipedia](<https://en.wikipedia.org/wiki/Dovetailing_(computer_science)>)(2022.08.08)
