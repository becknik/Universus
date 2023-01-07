---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Cantorsche Paarungsfunktion
linter-yaml-title-alias: Cantorsche Paarungsfunktion
date-of-creation: 2022-08-08
mod-date: 2022-10-19
---

# Cantorsche Paarungsfunktion

## Definition: #fc
- Sei $f:\mathbb{N}\rightarrow\mathbb{N}$ mit $f(n)=\binom{n}{2}$ mit $f(0)=0$ und $f(n+1)=f(n)+n$
- Sei $c$ die *bijektive*, *totale* und [[Modelle/Applikativ/Primitive Rekursion|primitiv rekursiv]] Funktion
$$c:\mathbb{N}^2\rightarrow\mathbb{N},c(x,y)\mapsto\binom{x+y+1}{2}+x$$
- $c$ wird zur *Kodierung von $k+1$-Tupeln* verwendet: $c_{k+1}(x_1,\dots,x_{k+1})=c(x_1,c_k(x_2,\dots,x_{k+1}))$
- Bildung von *Tripeln*: $c_3(x_1,x_2,x_3)=c_1(x_1,(c_2(x_2,x_3))$
- Umkehrfunktionen, die unmittelbar aus der *Bijektion* folgen:
	- $e(c(x,y))=x\quad\Leftrightarrow\quad e(n)=\max\{x\leq n\mid\exists y\leq n:c(x,y)=n\}$
	- $f(c(x,y))=y\quad\Leftrightarrow\quad f(n)=\max\{y\leq n\mid\exists x\leq n:c(x,y)=n\}$
^1660502533457
