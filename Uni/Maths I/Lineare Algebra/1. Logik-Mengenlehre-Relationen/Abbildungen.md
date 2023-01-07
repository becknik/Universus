---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Abbildungen
  - Abbildung
  - injektiv
  - surjektiv
linter-yaml-title-alias: Abbildungen
date-of-creation: 2022-10-26
mod-date: 2022-11-07
---

# Abbildungen

## Definition #fc
- Seien $A$, $B$ *nicht-leere [[Mengenlehre|Mengen]]* und sei $F\subseteq A\times B$ eine [[Relationen]], dann heißt $F$ *Abbildung*, wenn $$\forall x\in A:\exists^! y\in B:(x,y)\in F$$ gilt
	→ Eine Abbildung kann als *Zuordnungsvorschrift* oder *[[Relationen|Relation]] mit speziellen Eigenschaften* betrachtet werden
^1666212014753

## Fachtermini
- *Wert*: $F(x):=\{b\in B\mid\exists a\in A:f(a)=b\}$
- *Bild*: $\text{Bild}(A)=f(A)$
- *Abbildung*: $x\mapsto y$
	→ Für eine Teilmenge $M\subseteq A$: $F(M):=\{y\in B\mid\exists e\in M:F(x)=y\}$
- *Graph* von $f$: $\mathcal{G}(f):=\{(a,f(a))\mid a\in A\}\subseteq A\times B$
- *Urbild*: $x\in A:F(x)=y$
	→ Für eine Teilmenge $N\subseteq B$: $F^{-1}(N):=\{x\in A\mid F(x)\in N\}$
- *Bild-*/ *Definitionsbereich*: Die Mengen $A$ / $B$

## Eigenschaften

### Surjektivität #fc
- Eine Abbildung $F:A\rightarrow B$ ist genau dann surjektiv, wenn $$\forall y\in B:|F^{-1}(\{y\})|\geq 1$$ erfüllt ist
	→ In anderen Worten: Für jedes $B'\subseteq B,|B'|=1$ besteht das Urbild aus mindestens einem Element
- Die Abbildung $F$ ist *nicht surjektiv*, wenn $\exists b\in B:|F^{-1}(b)|=0$ gilt
^1666789477605

### Injektivität #fc
- Eine Abbildung $F:A\rightarrow B$ ist genau dann *injektiv*, wenn $$\forall y\in B:|F^{-1}(\{y\})|\leq 1$$ erfüllt ist
	→ Anders ausgedrückt: Für jedes $B'\subseteq B,|B'|=1$ besteht das Urbild aus höchstens einem Element
- Die Abbildung $F$ ist *nicht injektiv*, wenn $\exists b\in B:|F^{-1}(b)|\geqslant 2$ gilt
^1666789477607

### Identfunktion
- $id_X:X\rightarrow X, x\mapsto x$

### Verkettung #fc
- Seien $F:A\rightarrow B$ und $G:B\rightarrow C$ zwei Abbildungen, so ist auch $F\circ G:A\rightarrow C,a\mapsto G(F(a))$ eine Abbildung
	→ *Kommutativität* ist nicht erfüllt: $F\circ G\neq F\circ G$
	→ *Assoziativität* ist erfüllt: $(G\circ H)\circ F=H\circ(G\circ F)$
^1667214407762

### Eineschränkung #fc
- Sei $f:M\rightarrow N$ eine Abbildung und $A\subseteq M$, dann ist die *Einschränkung* der Abbildung $f$ definiert als $$f|_A:A\rightarrow N,f|_A(a):=f(a)$$
^1666790294756

### Mächtigkeit und Verhältnis #fc
- Seien $A,B$ nicht-leere, endliche [[Mengenlehre|Mengen]] und $V=\{f:A\rightarrow B\}$ die Mengen aller [[Abbildungen]] auf $A\rightarrow B,$ so gilt
	- es gilt $|A|\leqslant|B|,$ wenn $\exists f'\in V\text{ mit }f'$ *injektiv*
	- es gilt $|A|\geqslant|B|$, wenn $\exists f'\in V\text{ mit }f'$ *surjektiv*
	- falls $|A| = |B|$ gilt $\exists f'\in V\text{ mit }f'$ *bijektiv*
^1667415783098

## Beispiel
- $\{(x,y)\in\mathbb{R}^2\mid y=x^2\}$
