---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Äquivalenzrelationen
  - Äquivalenzklassen
linter-yaml-title-alias: Äquivalenzrelationen
date-of-creation: 2022-10-19
mod-date: 2022-11-02
---

# Äquivalenzrelationen
→ [[Relationen]]

## Definition #fc
- Eine [[Relationen|Relation]] $R$ auf $M\times M$ über der Menge $M$ heißt *Äquivalenzrelation*, wenn folgende Eigenschaften für sie erfüllt sind:
	1. *Reflexivität*: $\forall a\in M:a\sim a$
	2. *Symmetrie*: $\forall a,b\in M:a\sim b\Rightarrow b\sim a$
	3. *Transitivität*: $\forall a,b,c\in M:(a\sim b\wedge b\sim c)\Rightarrow a\sim c$
^1666213723271

### Umkehrung #fc
- Sei $\{M_j\mid j\in J\}$ eine *disjunkte* Zerlegung der Menge $M$, so ist durch $$x\sim y\quad\Leftrightarrow\quad\exists j\in J:x,y\in M_j$$ eine Äquivalenzrelation auf $M$ definiert
→ *Disjunkt*: $\forall k\neq j:M_j\cap M_k=\emptyset\wedge M=\bigcup_{j\in J}M_j$
^1666213723276

### Ordnungsrelation #fc
- Ist eine [[Relationen]] $R$ *reflexiv*, *anti-symmetrisch* und *transitiv*, so ist $R$ eine *Ordnungrelation*
	→ *Anti-Symmetrie*: Für $a,b\in M,R\subseteq R\times R$ gilt: $a\sim b\wedge b\sim a\Rightarrow a=b$
^1666882337830
