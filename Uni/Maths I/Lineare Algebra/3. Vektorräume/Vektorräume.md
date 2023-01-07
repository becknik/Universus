---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: false
aliases:
  - Vektorräume
  - Vektorraum
  - Vektorraumaxiome
linter-yaml-title-alias: Vektorräume
date-of-creation: 2022-11-13
mod-date: 2022-12-04
---

# Vektorräume

## Definition #fc
- Sei $K$ ein [[../2. Gruppen-Ringe-Körper/Körper|Körper]], dann ist der *Vektorraum* über $K$ - auch $K$-Vektorraum genannt - eine …
	- … Menge von *Vektoren* $V$ zusammen mit einer *Addition* $+,$ …
	- … sodass $(V,+)$ eine [[../2. Gruppen-Ringe-Körper/Gruppen|abelsche Gruppe]] bildet, etc.
	- zusammen mit einer "*Skalarmultiplikation*" genannten [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]] $$K\times V\rightarrow V,\quad(\lambda,v)\mapsto\lambda\cdot v$$
	→ Elemente aus $K$ werden *Skalare* genannt
^1668377830921

### Verktorraumaxiome auf $(\lambda,v)\mapsto\lambda\cdot v$ #fc
1. Assoziativität: $\forall\lambda,\mu\in K,\forall v\in V:\quad(\lambda\cdot\mu)\cdot v=\lambda\cdot(\mu\cdot v)$
2. Distributivität: $\forall\lambda,\mu\in K,\forall v\in V:\quad(\lambda+\mu)\cdot v=\mu\cdot v+\lambda\cdot v$
3. Distributivität: $\forall\lambda\in K,\forall v,u\in V:\quad\lambda\cdot(v+u)=\lambda\cdot v+\lambda\cdot u$
4. Eins-Element für Vektoren: $\forall v\in V:\quad1\cdot v=v$
^1668377830931

## Eigenschaften #fc
- Für $v\in V$ gilt: $c\cdot0=0$
- $\forall\lambda\in K,v\in V$ gilt: $(−\lambda)v=−(\lambda v)=\lambda(−v)$
- Jeder Vektorraum besitzt ein [[Erzeugendensystem|Basis]]
	→ Beweis über das [[Zornsche Lemma]] oder das [[Auswahlaxiom]] #TODO
^1668377840944

## Beispiele

### $K^n:$ #fc
- $V=K^n$ und $K=K$ bildet mit der komplementweisen Addition und der Skalarmultiplikation $$K\times V\rightarrow V,\quad\lambda\cdot(x_1,\dots,x_n):=(\lambda x_1,\dots,\lambda x_n)$$ einen der wichtigsten Vektorräume
^1668377840947

### Reelle Funktionen #fc
- Sei $V:=\{f:\mathbb{R}\rightarrow\mathbb{R}\}$ die Menge aller reellen Abbildungen, $(f+g)(t):=f(t)+g(t)$ die Addition und $(\lambda\cdot f)(t):=\lambda f(t)$ die Skalarmultiplikation auf dieser
	→ Betrachte beispielsweise die [[Untervektorräume]] von $f:\mathbb{R}\times\mathbb{R}$ aller stetig wachsender oder aller differenzierbaren Funktionen in $\mathbb{R}$
^1670110927886
