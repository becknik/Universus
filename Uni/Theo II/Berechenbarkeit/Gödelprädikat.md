---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: false
aliases: Gödelprädikat
linter-yaml-title-alias: Gödelprädikat
date-of-creation: 2022-09-01
mod-date: 2022-09-01
---

# Gödelprädikat

## Definition:
$$G(a,b,i,y)\Leftrightarrow y=a~mod(1+(i+1)\cdot b)$$
	→ Für $y$ zu erfüllende Bedingungen: $y\leq (i+a)b$ und $(a-y)$ ist durch $(1+(i+1)b)$ teilbar
- Darstellung unter Beachtung der Bedingungen: $G(a,b,i,y)$ gilt: $$\exists k(y+k=(i+1)\cdot b)\wedge\exists m(y=a-m\cdot(1+(i+1)\cdot b))$$
- $\forall(n_0,\dots,n_k)\in\mathbb{N}^{(k+1)<\infty},\exists a,b\in\mathbb{N},~\forall i\leq k:$
$$G(a,b,i,n_i)$$
	→ Für jede Wahl von $a,b$ und des Index $i\leq k$ existiert genau ein $x$ mit $G(a,b,i,x)$
	→ Der gesamte Vektor $(n_0,\dots,n_k$) lässt sich durch $a,b$ durch die Formel $G$ eindeutig rekonstruieren ($b=s!,s$ größter Wert der Folge (?))
- Aussage: $a,b$ repräsentieren eine Zahlenfolge, $y$ ist der Rückgabewert für $n_i$

## Beweis:
- $s:=\max\{k,n_0,\dots,n_k\}$
- $b:=s!$
- $\forall i\leq k:b_i:=1+(i+1)\cdot b$
- $b_i\equiv 1 \pmod m\quad\forall m\leq s$
	→ $b_i\neq b_j:ggT(b_i,b_j)=1$
→ Siehe F.21.4 für mehr Freude am Leben
