---
tags: uni theo-1 theoretical-cs chomsky
cards-deck: Uni::Courses::Theo-I
complete: true
aliases:
  - Typ-1
  - Typ-1 Grammatik
  - Typ-1 Sprache
  - CSL
  - Context Sensitive Languages
  - kontextsensitive Sprache
  - nichtverkürzend
  - nichtverkürzende Grammaik
linter-yaml-title-alias: Typ-1
date: 2022-09-15
mod-date: 2022-09-23
---

# Typ-1

## Definition:
- Eine gültige, [[Grundlegendes/Grammatik|formale Grammatik]] $G$ mit $$\forall(u,v)\in P:|u|\leq|v|$$ ist gehört dem 1. Typ der [[Chomsky-Hierarchie]] an

## Eigenschaften:
- Für jede Satzform $v$ (für $P\ni(u,v)$, also der Struktur auf der rechten Seite der Übergangsrelation $\Rightarrow_G$) muss gelten, dass $|v|\geq1$
	-> Für das *neutrale Element* des freien [[Monoid|Monoids]] über $\Sigma,\varepsilon$, muss also gelten, dass $v\neq\varepsilon,$ da für dieses aufgrund der *neutralen Element-Eigenschaft* $|\varepsilon|=0$ gilt
- Das [[Wortproblem|Wortproblem]] ist für Typ-1 Sprachen [[../Theo II/Entscheidbarkeit|entscheidbar]]
- Die Klasse der von [[1. Typ - CSL/Linear beschränkte Turingmaschine|LBAs]] akzeptierten Sprachen entspricht der Sprachklasse $\text{CSL}$
	-> $O.B.d.A:\{L\mid \varepsilon\notin L\}$
	-> [[1. Typ - CSL/Linear beschränkte Turingmaschine|LBA-Problem]]

## Beweis der Entscheidbarkeit für $G\in$ Typ-1:
- Z.z.: $x\in T\Longleftrightarrow x\in L(G)$
- Hier genügt die Angabe eines Algorithmus:
```
INPUT sei x mit |x| = n, n > 0
Variable T := {S};
REPEAT
	T_1 := T;
	T := Abln (T_1)*
UNTIL (x ∊ T) OR (T = T_1);
IF x ∊ T THEN OUTPUT(1) ELSE OUTPUT(0);
```
$$\displaylines{\forall X: X\subseteq(V\cup\Sigma)^*\\ *Abl_n(X)=X\cup\{w\in(V\cup \Sigma)^*\mid |w|\leq n\text{ und }\exists y\in X:y\Rightarrow_G w\}}$$
-> Ein [[../Theo II/Komplexitättheorie/Zeitklassen/NP-Härte|NP-harter]] Algorithmus

## Modelle:
- [[1. Typ - CSL/Linear beschränkte Turingmaschine|(nichtdeterministischer) LBA]]

## Theoreme:
- [[../Theo II/Komplexitättheorie/Platzklassen/Satz von Immerman–Szelepcsényi|Satz von Immerman–Szelepcsényi]]

## Beispiele:
- $L=\{a^nb^nc^n\mid n\geq1\}$
	-> $L\notin$ [[Typ-2|CFL]]!