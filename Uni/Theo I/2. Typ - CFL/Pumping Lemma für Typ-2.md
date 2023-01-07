---
tags: uni theo-1 theoretical-cs theorem chomsky
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Pumping Lemma für Typ-2
  - uvwxy-Theorem
linter-yaml-title-alias: Pumping Lemma für Typ-2
date-of-creation: 2022-09-21
mod-date: 2022-10-31
---

# Pumping Lemma für Typ-2

## Definition: #fc
- $\forall L\in \text{Typ-2 }\exists n\in\mathbb{N},$ mit dem $\forall z\in L$ mit $|z|\geq n$ in $z=uvwxy$ mit $u,v,w,x,y\in\Sigma^{Stern}$ zerlegt werden kann, sodass Folgendes erfüllt ist:
	1. $|vx|\geq1\Rightarrow vw\neq\varepsilon$
	2. $|vwx|\leq n$
	3. $\forall i\geq0:uv^iwx^iy\in L$
- Wird wie das [[../3. Typ - REG/Pumping Lemma für Typ-3|Pumping Lemma für Typ-3]] für Widerspruchsbeweise (Z.z.: $L\notin$ [[../Typ-2|CFL]]) eingesetzt
	→ "Angenommen, $L\in\text{CFL},$ dann $\exists n$, sodass jedes $z\in L$ mit $|z|\geq n$ die obigen Bedingungen erfüllt"
^1664631275785

## Negation: #fc
- $\forall n\in\mathbb{N},\exists z\in L$ mit $|z|\geq n$ und alle Zerlegungen $z=uvwxy$ mit $|uxw|\leq n,|ux|\geq1$ mindestens ein $z_i=uv^iwx^iy$ existier, so dass $z_i\notin L$ gilt
^1664631275793

> *Keine Garantie, dass das stimmt…*

## Eigenschaften:
- Wird oft auch als $uvwxy$-Theorem bezeichnet

## Beweis-Schema: #fc
- Gegeben sei eine Grammatik $G$ in [[Chomsky-Normalform|CNF]] und der Ableitungsbaum für ein langes Wort
	→ Für eine genügend große Länge des Worts müssen sich Variablen auf mindestens einem Pfad im Baum wiederholen
^1664737163713

## Beispiele:
- VL.12 F.23.3 ff.
- VL.13 F.24.1
