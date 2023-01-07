---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases: Äquivalenzklassen
linter-yaml-title-alias: Äquivalenzklassen
date-of-creation: 2022-11-02
mod-date: 2022-11-07
---

# Äquivalenzklassen

## Definition
- Sei $M$ eine [[Mengenlehre|Menge]] und $R$ eine [[Relationen|Relation]] auf dieser, so ist die Menge der Äquivalenzklassen definiert als $$\{[x]\mid x\in M\}:\quad M=\bigcup_{x\in M}[x]$$
	→ Für zwei Äquivalenzklassen $[a],[b]:\quad[a]\cap[b]=\emptyset\vee[a]=[b]$

### Alternativ #fc
- Sei $R$ eine Äquivalenzrelation, dann ist $\mathcal{K}(a,R):=\{b\in M\mid(a,b)\in R\}\in\mathcal{P}(M)$ die *Äquivalenzklasse* von $a$
- Die Menge aller *Äquivalenzklassen* von Elementen in $A$ über $R$: $\mathcal{K}(A,R)=\{S\in\mathcal{P}(A)\mid\exists a\in A:S=\mathcal{K}(a,R)\}$
^1666213723274

## Repräsentantensystem #fc
- Eine Teilmenge $B\subseteq A$ heißt *Repräsentantensystem der Äquivalenzklasse*, wenn
	- $\forall a\in A:\exists^!b\in B:(b,a)\in R$ gilt, oder…
	- … $\bigcup_{b\in B}K(b,R)$ und in dieser Vereinigung alle Therme disjunkt sind
^1667398791343

## Restklassen #fc
- Als $R_m,m\in\mathbb{N}$ werden die *Restklassen*$\pmod m$ bezeichnet
	→ Wenn $m$ fest vorgegeben ist, wird die Restklasse von $n\in\mathbb{Z}$ als $\overline{n}$ bezeichnet, also $$\overline{n}=\{a\in\mathbb{Z}\mid m\text{ teilt }n-a\}=\{a\in\mathbb{Z}\mid a\pmod m=n\pmod m\}$$
- Für jedes $n\in\mathbb{Z}\exists^!r\in B:n\pmod m=r,$ also $n\in\overline{r}\wedge\overline{n}=\overline{r}$
	→ $\mathbb{Z}=\overline{0}\cup\overline{1}\cup\overline{2}\cup\dots\cup\overline{m-1},$ z.B. für $m=5:\mathbb{Z}=\overline{0}\cup\overline{1}\cup\overline{2}\cup\overline{3}\cup\overline{4}$
^1667413850273

### Eigenschaften

#### Lemma 4.11 #fc
- Sei $m\in\mathbb{N}$ dann bezeichnen wird die Restklasse von $n\in\mathbb{Z},n\pmod m$ als $\overline{n}.$
- Seien $a,b,c,d\in\mathbb{Z}$
- Wenn $\overline{a}=\overline{c}\wedge\overline{b}=\overline{d}$ gilt, dann folgt daraus $\overline{a+b}=\overline{c+d}$ und $\overline{ab}=\overline{cd}$
^1667413844946
