---
tags: uni theo-1 theoretical-cs theorem
cards-deck: Uni::Courses::Theo-I
complete: false
aliases:
  - Pumping Lemma für Typ-2
  - uvwxy-Theorem
linter-yaml-title-alias: Pumping Lemma für Typ-2
date: 2022-09-21
mod-date: 2022-09-21
---

# Pumping Lemma für Typ-2

## Definition:
- $\forall L\in \text{Typ-2 }\exists n\in\mathbb{N},$ mit dem $\forall z\in L$ mit $|z|\geq n$ in $z=uvwxy$ mit $u,v,w,x,y\in\Sigma^*$ zerlegt werden kann, sodass Folgendes erfüllt ist:
	1. $|vx|\geq1\Rightarrow vw\neq\varepsilon$
	2. $|vwx|\leq n$
	3. $\forall i\geq0:uv^iwx^iy\in L$
- Wird wie das [[../3. Typ - REG/Pumping Lemma für Typ-3|Pumping Lemma für Typ-3]] für Wiederspruchsbeweise (Z.z.: $L\notin$ [[../Typ-2|CFL]]) eingesetzt
	-> "Angenommen, $L\in\text{CFL},$ dann $\exists n$, sodass jedes $z\in L$ mit $|z|\geq n$ die obigen Bedingungen erfüllt"

## Negation: !!!

## Eigenschaften:
- Wird oft auch als $uvwxy$-Theorem bezeichnet

## Beweis-Schema:
- Gegeben sei eine Grammatik $G$ in [[Chomsky-Normalform|CNF]] und der Ableitungsbaum für ein langes Wort
	-> Für eine genügend große Länge des Worts (?) müssen sich Variablen auf mindestens einem Pfad im Baum wiederholen

## Beispiele: !!!
- VL.12 F.23.3 ff.
- VL.13 F.24.1
