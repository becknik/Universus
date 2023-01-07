---
tags: uni theo-2 theoretical-cs computability applicative
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Primitive Rekursion
date-of-creation: 2022-08-07
mod-date: 2022-08-21
linter-yaml-title-alias: Primitive Rekursion
---

# Primitive Rekursion

## Definition

### Basis-Funktionen: #fc
- *Konstante Funktionen*: $c^k_i:\mathbb{N}^k\rightarrow\mathbb{N},(x_1,\dots,x_k)\mapsto i$
- *Projektionen*: $\pi^k_i: \mathbb{N}^k\rightarrow\mathbb{N}, \pi^k_i(x_1,\dots,x_i,\dots,x_k)\mapsto x_i$
- Die *Inkrement-Funktion*: $s:\mathbb{N}\rightarrow\mathbb{N},x\mapsto x+1$
^1664742055960

### Rekursive Funktionen: #fc
- Funktionen, die aus primitiv rekursiven Funktionen bestehen:
	→ Seien $g,l\in\mathbb{N}$ beliebig primitiv rekursive Funktionen, mit $g:\mathbb{N}^l\rightarrow\mathbb{N}$ und $h_1,\dots,h_l:\mathbb{N}^k\rightarrow\mathbb{N}$, dann ist auch ihre *Komposition* $g(h_1,\dots,h_l): \mathbb{N}^k → \mathbb{N},(x_1,\dots,x_k)\mapsto g(h_1(x_1,\dots,x_k),\dots, h_l(x_1,\dots,x_k))$ primitiv rekursiv
- Funktionen, die aus primitiver Rekursion aus primitiv rekursiven Funktionen $g:\mathbb{N}^k\rightarrow\mathbb{N}$ und $h:\mathbb{N}^{k+2}\rightarrow\mathbb{N}$ entstehen:
	- Falls $n=0:f(0,x_1,\dots,x_k)=g(x_1,\dots,x_k)$
	- Sonst: $f(n+1,x_1,\dots,x_k)=h(f(n,x_1,\dots,x_k),n,x_1,\dots,x_k)$
	→ Alternativ: $rec(g,h)(0,x_1,\dots,x_k)=g(x_1,\dots,x_k)$ und $rec(g,h)(n+1,.x_1,\dots,x_k)=h(rec(g,h)(n,x_1,\dots,x_k)(x_1,\dots,x_k))$
^1660502635830

## Eigenschaften:
- Eine Funktion ist genau dann [[../../LOOP-berechenbar|LOOP-berechenbar]], wenn sie primitiv rekursiv ist
- Jede primitiv rekursive Funktion ist total

## Beispiele: #fc
→ Angenommen, $f(x_1,\dots,x_k)$ ist primitiv rekursiv
- *Identifikation von Variablen*: $g(x_1,\dots,x_{k-1})=f(x_1,\dots,x_{k-1},x_{k-1})$
- *Fiktive Variablen*: $g(x_1\dots,x_k,x_{k+1)}=f(x_1,\dots,x_k)$
- *Variablen vertauschen*: $g(x_1,\dots,x_k)=f(x_1,\dots,x_{k-2},x_{k-1})$
- *Maximum*: $\max(x,y)=(x-y)+y$
- *Addition*: $rec(\pi^1_1,s(\pi^3_1))$
- *Multiplikation*: $rec(c^1_0,add(\pi^3_1,\pi^3_3))$
- *Dekrement*: $rec(c^0_0,\pi^2_2)$
	→ $rec(g,h)(0,x_1,\dots,x_k)=g(x_1,\dots,x_k)$
- *Multiplikation*: $rec(\pi^1_1,dec(\pi^3_1))(\pi^2_2,\pi^2_1)$
	→ $rec(g,h)(n+1,.x_1,\dots,x_k)=h(rec(g,h)(n,x_1,\dots,x_k)(x_1,\dots,x_k))$
^1660502641133
