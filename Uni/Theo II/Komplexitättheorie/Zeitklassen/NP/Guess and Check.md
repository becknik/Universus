---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
complete: true
aliases: Guess And Check
date: 2022-07-10
mod-date: 2022-08-14
linter-yaml-title-alias: Guess And Check
---

# Guess And Check

## Prinzip: #fc
- Oft sind [[NP|NP-Probleme]] formuliert wie: "Gibt es ein $z$, so dass die Eigenschaft $E(x,z)$ gilt?"
- Wenn die Länge von $z$ (in der Eingabelänge) polynomiell beschränkt und $E$ deterministisch in Polynomialzeit prüfbar ist, dann ist $E \in NP$
- Es kann eine nichtdeterministischer Algorithmus entworfen werden, der $z$ rät und dann prüft, ob $E$ lösbar ist
	-> Zum Beispiel: $z=$ erfüllende Belegung
	-> Für die meisten [[NP-Vollständigkeit|NP-vollständigen]] Probleme erfolgt der Nachweis, ob $\in NP$ nach dieser Art
Beispiele:
```
CLIQUE:
Sei V = {v_1, ..., v_n}.
Wähle nichtdeterministisch n Bits a_1, ..., a_n.
Prüfe, ob {v_i ∊ V | a_i = 1} eine Clique der Größe ≥ k bildet.
Wenn ja: ACCEPT, andernfalls: REJECT
```
```
FÄRBBARKEIT:
Sei V = {v_1, ..., v_n}.
Wähle nichtdeterministisch n Werte a_1, ..., a_n ∊ {1, ..., k}.
Prüfe, ob \varphi mit \forall i:\varphi(v_i) = a_i eine zulässige Färbung bildet.
Wenn ja: ACCEPT, andernfalls: REJECT
```
^1660771469328