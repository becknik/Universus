---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Lineare Unabhängigkeit
  - linear unabhängig
linter-yaml-title-alias: Lineare Unabhängigkeit
date-of-creation: 2022-12-04
mod-date: 2023-01-08
---

# Lineare Unabhängigkeit

## Definition #fc
- Gegeben seinen die Vektoren $v_1,\dots,v_n$ des [[Vektorräume|Vektorraums]] $V$
- Die Vektoren $v_1,\dots,v_n$ heißen *linear abhängig*, wenn sich der *Nullvektor* als nicht-triviale [[Linearkombinationen|Linearkombination]] der Vektoren $v_1,\dots,v_n$ darstellen lässt
	→ Aus der Menge der *Koeffizienten* $\lambda_1,\dots,\lambda_n$ muss es also mindestens einen Koeffizient $\lambda_j\neq0,$ sodass $\lambda_1v_1,\dots,\lambda_nv_n=0$ gefüllt ist
- Ansonsten sind $v_1,\dots,v_n$ *linear abhängig*
^1670172257009

### Verallgemeinerung auf $M\subseteq V$ #fc
- Sei $V$ ein [[Vektorräume|Vektorraum]] und $M\subseteq V,$ dann heißt $M$ *linear unabhängig*, wenn $\forall A\subseteq M$ mit $|A|<\infty,A=\{v_1,\dots,v_n\}$ die Vektoren $v_1,\dots,v_n$ *linear unabhängig* sind
	→ Andernfalls ist $M$ *linear abhängig*
^1670172737106

## Verhältnis zum Spann #fc
- Seien $v_1,\dots,v_n$ Vektoren eines [[Vektorräume|Vektorraums]]
- $v_1,\dots,v_n$ sind genau dann *linear unabhängig*, wenn $\forall s\in\text{span}(\{v_1,\dots,v_n\})$ gilt:
	- $s$ lässt sich als [[Linearkombinationen]] von $v_1,\dots,v_n$ mit *eindeutig bestimmten* Koeffizienten schreiben
	- Formal:
$$\text{span}\{v_1,\dots,v_n\}=Kv_1\oplus\dots\oplus Kv_n$$
^1670173439381

## Hilfssatz 3.5.5 zu Linearität einer linear unabhängigen Teilmenge $B$
- Sei $B\subseteq V$ *linear unabhängig*, $V$ ein [[Vektorräume|Vektorraum]] und $v\in V$ ein Vektor, dann gilt: $$B\cup\{v\}\text{ linear unabhängig}\quad\Leftrightarrow\quad v\notin\text{span}(B)$$

## Eigenschaften #fc
Aus der [[#Definition fc|Definition]] folgt: $\forall A\subseteq V,|A|=1,A=\{v\}:\quad v\neq0\Leftrightarrow A\text{ linear unabhängig}$
- $\forall$ Teilmenge einer linear unabhängigen Menge $M$ eines [[Vektorräume|Vektorraums]] $V$ ist wieder *linear unabhängig*
- $\emptyset$ ist linear unabhängig
^1670172960182
