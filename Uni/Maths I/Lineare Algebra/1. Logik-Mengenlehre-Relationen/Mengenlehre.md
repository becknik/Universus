---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Mengenlehre
  - Menge
  - Kartesisches Produkt
  - Partitionierung
linter-yaml-title-alias: Mengenlehre
date-of-creation: 2022-10-18
mod-date: 2022-11-13
---

# Mengenlehre

## Definition
- Eine Menge ist eine *wohldefinierte Gesamtheit* von Objekten, den Elementen der Menge
	→ Wohldefiniertheit: "Entweder das Element ist drinnen oder nicht", die Eigenschaft muss aber nicht entscheidbar sein #TODO
- Die Aussage $x\in M$ ist genau dann wahr, wenn das Objekt $x$ ein Element der Menge $M$ ist

### Notationen #fc
- *Aufzählung*: $\mathbb{N}=\{1,2,3,4,\dots\}$
- *Aussonderung*: $H=\{n\in\mathbb{N}\mid n=2m,m\in\mathbb{N}\}$, allgemeiner $\{x\in M\mid P(m)\}\subseteq M$
^1666212014747

### Potenzmenge
- $Pot(M)=\{A\mid A\subseteq M\}$

### Mengenoperatoren
- *Schnittmenge*: $A\cap B:=\{x\in A\mid x\in B\}$
- *Vereinigung*: $A\cup B:=\{a\mid x\in A\vee x\in B\}$
- *Komplement*: $A^\complement$ oder $A\setminus B:=\{x\in A\mid x\notin B\}$

### Kartesisches Produkt
$$A_1\times A_2\times\dots\times A_n:=\{(a_1,a_2,\dots,a_n)\mid a_i\in A_i\text{ für }1\leqslant i\leqslant n\}$$
→ Die Menge an geordneten Paaren, auch *Tupel* genannt

## Eigenschaften
- Ein Element kann nicht doppelt in einer Menge auftreten
- Für jede Menge $A$ gilt $\emptyset\in A$

### Richard Dedekind #fc
- Sei $A$ ein nicht-leere Menge, dann ist $A$ unendlich groß, genau dann wenn $\exists B\subsetneq A:|A|=|B|$
^1667419513696

### Potenzmenge #fc
- Sei $A$ eine endliche Menge mit $|A|=n\in\mathbb{N},$ dann gilt $|\mathcal{P}(A)|=2^n$
	→ $2^n=(1+1)^n=\sum_{k=0}^n\binom{n}{k}1^k1^{n-k}=\sum_{k=0}^n\binom{n}{k}=\binom{n}{0}+\binom{n}{1}+\cdots+\binom{n}{n}$
^1668374916270

## Partitionierung
- Sei $M$ eine Menge, dann heißen alle *disjunkte, nicht-leere Teilmengen* von $M$ Partitionen von $M$

### Eigenschaften
- Die Partitionen einer Singleton Menge $\{M'\}$ ist immer $\{\{M'\}\}$
- *Triviale Partition* von $M':P=\{M'\}$
