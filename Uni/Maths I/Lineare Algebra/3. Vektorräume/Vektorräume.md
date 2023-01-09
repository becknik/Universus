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
mod-date: 2023-01-09
---

# Vektorräume

## Definition #fc
- Sei $K$ ein [[../2. Gruppen-Ringe-Körper/Körper|Körper]], dann ist der *Vektorraum* über $K$ (*$K$-Vektorraum*) definiert als eine
	- … Menge $V$ aus *Vektoren*, sodass $(V,+)$ eine [[../2. Gruppen-Ringe-Körper/Gruppen|abelsche Gruppe]] bildet,
	- … zusammen mit einer [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]] \$$$K\times V\rightarrow V,\quad(\lambda,v)\mapsto\lambda\cdot v$$ (= *Skalarmultiplikation*)
	→ Für die *Skalarmultiplikation* müssen die [[#Verktorraumaxiome auf $( lambda,v) mapsto lambda cdot v$ fc|Verktorraumaxiome]] gelten
	→ Elemente aus $K$ werden *Skalare* genannt
^1668377830921

## Verktorraumaxiome

### Definition ($(\lambda,v)\mapsto\lambda\cdot v$) #fc
1. Assoziativität: $\forall\lambda,\mu\in K,\forall v\in V:\quad(\lambda\cdot\mu)\cdot v=\lambda\cdot(\mu\cdot v)$
2. Distributivität: $\forall\lambda,\mu\in K,\forall v\in V:\quad(\lambda+\mu)\cdot v=\mu\cdot v+\lambda\cdot v$
3. Distributivität: $\forall\lambda\in K,\forall v,u\in V:\quad\lambda\cdot(v+u)=\lambda\cdot v+\lambda\cdot u$
4. Eins-Element für Vektoren: $\forall v\in V:\quad1\cdot v=v$
^1668377830931

## Eigenschaften #fc
- Für $v\in V$ gilt: $v\cdot0=0$
- $\forall\lambda\in K,v\in V$ gilt: $(−\lambda)v=−(\lambda v)=\lambda(−v)$
- Jeder Vektorraum besitzt ein [[Erzeugendensysteme|Basis]]
	→ Beweis über das [[Zornsche Lemma]] oder das [[Auswahlaxiom]] #TODO
^1668377840944

## Wichtige Beispiele

### $K^n:$ #fc
- Sei Menge der *Vektoren* $V=K^n$ (=$n$-Tupel), dann bildet sie einen [[Vektorräume|Vektorraum]] mit der
	- … *komponentenweisen Addition* und der
	- … Instanz der Skalarmultiplikation: $\lambda\cdot(x_1,\dots,x_n):=(\lambda x_1,\dots,\lambda x_n),\lambda\in K$
- Die Skalarmultiplikation entspricht der *zentrischen Streckung* eines Vektors/ Tupels $v\in V$ um den Faktor $\lambda$
^1668377840947

### Menge der reellen Funktionen #fc
- Sei $V:=\{f:\mathbb{R}\rightarrow\mathbb{R}\}$ die Menge aller reellen Abbildungen,
	- … die Addition als $(f+g)(t):=f(t)+g(t)$ und
	- … die Skalarmultiplikation als $(\lambda\cdot f)(t):=\lambda f(t)$ definiert
- [[Untervektorräume]]: Die einstelligen stetig wachsenden oder differenzierbaren Funktionen in $\mathbb{R}$
^1670110927886
