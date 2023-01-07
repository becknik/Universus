---
tags: uni theo-2 theoretical-cs computability applicative
cards-deck: Uni::Courses::Theo-II
completed: false
aliases:
  - Arithmetische Repräsentierbarkeit
date-of-creation: 2022-08-09
mod-date: 2022-08-21
linter-yaml-title-alias: Arithmetische Repräsentierbarkeit
---

# Arithmetische Repräsentierbarkeit

## Definition: #fc
- Die Funktion $f:\mathbb{N}^k\rightarrow\mathbb{N}$ ist arithmetisch repräsentierbar, wenn es eine $(k+1)$-stellige arithmetische Formel $F$ gibt, so dass $$F(n_1,\dots,n_k,m)\Leftrightarrow f(n_1,\dots,n_k)=m$$ gilt
^1660076491419

## Beispiele: #fc
→ Nicht vergessen, die Korrektheit zu beweisen
- *Addition*: $F_1(x, y , z) \Leftrightarrow ((x + y ) = z)$
- *Multiplikation*: $F_2(x, y , z) \Leftrightarrow ((x\cdot y ) = z)$
- *Floor-Division*: $F_3(x,y,z)\Leftrightarrow \exists r[(x=y\cdot z+r)\wedge\exists w(r+w+1=y)(//\triangleq r<y)]$
- *Modulo*: $F_4(x,y,z)\Leftrightarrow\exists m[(x=y\cdot m+z)~\wedge\exists w(z+w+1=y)]$
- *Dekrement*: $F_5(x,y)\Leftrightarrow(y+1=x)\vee((x=0)\wedge(y=0))$
- *Subtraktion*: $F_6(x,y,z)\Leftrightarrow(y+z=x)(//\triangleq z=x-y)\vee((z=0)~\wedge~\exists w(x+w=y)(//\triangleq x\leq y))$
- *Less-Equals*: $F_7(x,y,z)\Leftrightarrow\exists z((x+z)=y)$
- *Exponentialfunktion*: $\exists a,b:G(a,b,0,1)\wedge G(a,b,y,z)\wedge\forall i((y−1<i)\vee\exists c,d:G(a,b,i,c)\wedge G(a,b,i+1,d)\wedge(c\cdot x= d))$
	→ [[../../Gödelprädikat|Gödelprädikat]]
	→ Für ein geeignetes $k$ existiert die Folge $n_0,\dots,n_k$, so dass $n_0=1,n_y=z$ und $\forall i<y:x\cdot n_i=n_{i+1}$
	→ Für eine solche Folge ist aber "offensichtlich" $n_i=x^i$ und wegen $G(a,b,y,z)$ folgt $x^y=n_y=z$
^1660076491425
