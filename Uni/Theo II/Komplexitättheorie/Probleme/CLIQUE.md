---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: CLIQUE
date-of-creation: 2022-07-10
mod-date: 2022-08-11
linter-yaml-title-alias: CLIQUE
---

# CLIQUE

## Definition: #fc
- *Gegeben*: Ein [[../../../DSA/Graphen/Ungerichtete Graphen|ungerichteter Graph]] $G = (V,E)$ und $k \in \mathbb{N}$
- Gesucht: Gibt es in $G$ eine Clique der Größe $k$ ? (im Buch: $\geq k$)
	→ *Clique*: $V'\subseteq V, \forall u,v\in V, u\neq v: (u,v)\in E$ Jedes Knoten-Paar einer Teilmenge von $E$ ist mit allen anderen Knoten dieser Teilmenge verbunden
^1664744001088

## Eigenschaften:
- $\text{CLIQUE}\in\text{NP}:$
```
Sei V = {v_1, ..., v_n}.
Wähle nichtdeterministisch n Bits a_1, ..., a_n.
Prüfe, ob {v_i ∊ V | a_i = 1} eine Clique der Größe ≥ k bildet.
Wenn ja: ACCEPT, andernfalls: REJECT
```

## Beweis Der [[../Zeitklassen/NP/NP-Härte|NP-Härte]]:
- Zu zeigen: [[3KNF-SAT|3KNF-SAT]] $\leq_p\text{CLIQUE}:$
- O.B.d.A. $F = (z_{11} \vee z_{12} \vee z_{13}) \wedge \dots \wedge (z_{m1} \vee z_{m2} \vee z_{m3})$ mit $z_{ij}\in\{x_1,x_2,\dots,z_n\}~\cup~$$\{\neg x_1,\neg x_2,\dots,\neg z_n\}$
	→ O.B.d.A.: Für weniger als 3 Literale können DC durch negierter Dopplung eingefügt werden
- Sei $k(F)=m\in\mathbb{N}$ die Größe der Clique von dem [[../../../DSA/Graphen/Ungerichtete Graphen|ungerichteten Graphen]] $G(F)$, wenn $G(F),$ wenn $F$ eine erfüllbare Formel ist: $F\mapsto(G(F),k(F))$
	- $V = \{(i,j)\mid 1\leq i\leq m\wedge 1\leq j\leq 3\}$
	- $E = \{\{(i,j),(p,q)\}\mid i\neq q\wedge z_{is}\not\equiv\neg z_{jq}\}$
	→ $\mathcal{A}(F)=1$ $\Leftrightarrow G(F)$ hat Clique der Größe $m$
- Wenn man zu jedem Knoten $(i,j)$ das Literal $z_{ij}$ identifiziert, dann kann $G(F)$ nur dann eine Clique der Größe $m$ haben, wenn $\mathcal{A}(F)=1$ gilt
	$\mathcal{A}(F)=1$
	$\Leftrightarrow \forall 1\leq i\leq m\max(z_{i,1},z_{i,2},z_{i,3})=1$
	$\Leftrightarrow$ es gibt Literale $z_{1,j_1},z_{2,j_2},\dots,z_{m,j_m}\quad j_i\in\{1,2,3\}:$ sind paarweise nicht Komplementär
	$\Leftrightarrow$ zugehörige Knoten sind Verbunden
	$\Leftrightarrow G(F)$ hat eine Clique der Größe $k$
→ Für mehr Details: (F.28.4ff.)
