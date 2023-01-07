---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: false
aliases: FÄRBBARKEIT
date-of-creation: 2022-07-10
mod-date: 2022-08-11
linter-yaml-title-alias: FÄRBBARKEIT
---

# FÄRBBARKEIT

## Definition
- *Gegeben*: Ein ungerichteter Graph $G = (V,E)$ und $k \in \mathbb{N}$
- *Gesucht*: Gibt es eine *zulässige Färbung* mit $k$ Farben in $G$?
	→ Zulässige Färbung $\varphi: v \in V \rightarrow \{1,\dots,k\}$, $\forall (u,v) \in E: \varphi(u) \neq \varphi(v)$

## Eigenschaften:
- $\text{FÄRBBARKEIT}\in\text{NP}:$
```
Sei V = {v_1, ..., v_n}.
Wähle nichtdeterministisch n Werte a_1, ..., a_n ∊ {1, ..., k}.
Prüfe, ob \varphi mit \forall i:\varphi(v_i) = a_i eine zulässige Färbung bildet.
Wenn ja: ACCEPT, andernfalls: REJECT
```
- 3KNF-SAT $\leq_p$ 3-FÄRBBARKEIT $\rightarrow$ FÄRBBARKEIT ist NP-hart:
	- $F = (z_{11} \vee z_{12} \vee z_{13}) \wedge \dots \wedge (z_{m1} \vee z_{m2} \vee z_{m3})$
	- $V = \{u,x_1,\dots,x_n,\overline{x_1},\dots,\overline{x_n},v\} \cup \{a_j,b_j,c_j,y_j,z_j~|~1\leq j \leq \ m\}$
	- … Vorlesung 14
