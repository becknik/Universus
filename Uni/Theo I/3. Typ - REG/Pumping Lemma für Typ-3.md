---
tags: uni theo-1 theoretical-cs
cards-deck: Uni::Courses::Theo-I
complete: true
aliases:
  - Pumping Lemma für Typ-3
  - Lemma von Bar-Hillel
  - Iterationslemma
  - uvw-Lemma
linter-yaml-title-alias: Pumping Lemma für Typ-3
date: 2022-09-20
mod-date: 2022-09-20
---

# Pumping Lemma für Typ-3

## Definition:
- $\forall L\in \text{Typ-3}~\exists n\in\mathbb{N},$ mit dem $\forall x\in L$ mit $|x|\geq n$ in $x=uvw$ zerlegt werden kann, sodass Folgendes gilt:
	1. $|v|\geq1$
	2. $|uv|\leq n$
	3. $\forall i\geq0:uv^iw\in L$
- Soll nur für Wiederspruchsbeweise (Z.z.: $L\notin$ [[../Typ-3|REG]]) eingesetzt werden, da $$\text{Pumping Lemma}\setminus\text{REG}\neq\emptyset$$ (bezogen auf Sprachklasse) gilt

## Negation: (?)
- $\forall n\in\mathbb{N}~\exists x\in L$ mit $|x|\geq n,$ …
- … sodass jede Zerlegung $x=uvw,$ die die Bedingungen $|v|\geq1$ und $|uv|\leq n$ erfüllt, …
- … die Eigenschaft aufweist, dass für *mindestens ein* Wort $x_i=uv^iw$ gilt, sodass $x_i\notin L$

## Eigenschaften:
- Wird auch als *Iterationslemma*, $uvw$-Lemma oder *Lemma von Bar-Hillel* bezeichnet
- $\exists L\in\overline{\text{Typ-3}},$ deren *Nicht-Zugehörigkeit* nicht durch das *Pumping Lemma* beweisen werden kann…
	-> Jede Typ-3 Sprache erfüllt die Bedingungen des Pumping Lemma, aber $\exists L\in\text{Typ-3},$ die trotzdem die Aussage des Pumping Lemmas erfüllen
	-> Das Pumping-Lemma stellt also keine Charakterisierung von [[../Typ-3|REG]] dar
