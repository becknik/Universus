---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Spann
  - Aufspann
linter-yaml-title-alias: Spann
date-of-creation: 2022-12-04
mod-date: 2023-01-09
---

# Spann

## Definition #fc
- Sei $V$ ein [[Vektorräume#Definition fc|Vektorraum]] und $M\subseteq V$ eine Teilmenge
- Der *Spann* oder *Aufspann* von $M$ ($span(M)$ geschrieben) sei definiert als die Schnittmenge aller [[Untervektorräume#Definition fc|Untervektorräume]] von $V$, die $M$ enthalten
	→ Der Spann von $M\subseteq V$ ist also der kleinste Untervektorraum von $V,$ der die Teilmenge $M$ enthält
	→ Es gilt stehts $M\subseteq\text{span}(M)$
^1670110880364

## Zusammensetzung aus [[Linearkombinationen#Definition fc|Linearkombinationen]] #fc
- Sei $V$ ein [[Vektorräume|Vektorraum]] und $M\subseteq V,$ dann besteht der *Spann* $\text{span}(M)\subseteq V$ aus allen [[Linearkombinationen]] $$\lambda_1v_1+\dots+\lambda_nv_n\text{
mit }n\in\mathbb{N}_0,v_1,\dots,v_n\in M,\lambda_1,\dots,\lambda_n\in K$$
	→ Es folgt: $\forall$ Vektor $v\in V:\quad\text{span}(\{v\})=\{\lambda v\mid\lambda\in K\}$
^1670110880374

## Eigenschaften #fc
- $\text{span}(\emptyset)$ ist als $\{0\}$ definiert
- Anstelle von $\text{span}(\{v\})$ schreibt man auch $Kv$
^1670110880376
