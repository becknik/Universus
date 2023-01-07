---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Vertex Cover
date-of-creation: 2022-07-10
mod-date: 2022-08-14
linter-yaml-title-alias: Vertex Cover
---

# Vertex Cover

## Definition:
- *Gegeben*: Ein [[../../../DSA/Graphen/Ungerichtete Graphen|ungerichteter Graph]] $G=(V,E)$ und die Knotenüberdeckung $C \subseteq V$ mit $\forall \{u,v\} \in E: \{u,v\} \cap C \neq \emptyset$

## Beispiel für [[../../Problemklassen|Problemklassen]]:
1. Entscheidungsvariante: Existiert eine Knotenüberdeckung $C$ mit $|C| \leq k$ in $G$?
2. Berechnungsvariante: Berechne (falls vorhanden) die Knotenüberdeckung $C$ in $G$ mit $|C| \leq k$.
3. Optimierungsvariante: Berechne die minimale Knotenüberdeckung $C$ in $G$
→ Wie bei [[Traveling Salesman Problem]]: Wenn Variante 1. in Polynomialzeit lösbar ist, dann auch die Optimierungsvariante
→ *Selbstreduzierbarkeit*

## Algorithmus:
```
G_0 := G
Ermittle zuerst kopt (Hier ziemlich einfach...)
C_0 := ∅; k_0 := k_{opt};
FOR i := 1 TO n DO
	IF ∃ Knotenüberd. von G_{i-1} \steminus {v_i} mit k_{i-1}−1 Knoten
		THEN C := C ∪ {v_i}; k := k_{i-1}−1; G := G_{i-1} \setminus {v_i}
	ENDIF
ENDFOR
```
