---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Lineare Gleichungssysteme
  - lineare Gleichungssysteme
  - lineares Gleichungssystem
  - LGS
  - Lösungsmenge
  - spezielle Lösung
  - homogene lineare Gleichungssysteme
  - homogenes lineares Gleichungssystem
linter-yaml-title-alias: Lineare Gleichungssysteme
date-of-creation: 2023-01-08
mod-date: 2023-01-09
---

# Lineare Gleichungssysteme
→ [[Gaußalgorithmus]]

## Definition #fc
- Sei $K$ ein [[../2. Gruppen-Ringe-Körper/Körper#Definition fc|Körper]], $m,n\in\mathbb{N}$ mit $1\leq i\leq m,1\leq j\leq n$
- Seien die Elemente $a_{ij},b_i\in K$ gegeben, so nennen wir $$\begin{align}a_{11}x_1+\dots+a_{1n}x_n&=b_1\\\vdots\qquad\qquad~&\quad~~\vdots\\a_{m1}x_1+\dots+a_{mn}x_n&=b_m\end{align}$$ ein *System* von $m$ *linearen Gleichungen* mit $n$ Unbekannten $x_1,\dots,x_n$
- Ein Gleichungssystem lässt sich auch verkürzt als [[../2. Gruppen-Ringe-Körper/Matrizen#Produkt fc|Matrixmultiplikation]] schreiben: $$Ax=b\quad\Longleftrightarrow\quad\begin{pmatrix}a_{11}&\cdots&a_{1n}\\\vdots&\ddots&\vdots\\a_{m1}&\cdots&a_{mn}\end{pmatrix}\begin{pmatrix}x_1\\\vdots\\x_n\end{pmatrix}=\begin{pmatrix}b_1\\\vdots\\b_m\end{pmatrix}$$
- Eine praktischere Darstellung eines LGS als *erweiterte [[../2. Gruppen-Ringe-Körper/Matrizen#Definition fc|Matrix]]* $(A|b)\in M_{m,n+1}(K)$ mit $A\in M_{m,n}(K)$ für einen gegebenes $x$-Tupel $\in K^n$ und $b\in K^m$ mit $$\left(\begin{array}{ccc|c}a_{11}x_1&\cdots&a_{1n}x_n&b_1\\\vdots&\ddots&\vdots&\vdots\\a_{m1}x_1&\cdots&a_{mn}x_n&b_n\end{array}\right)\overbrace{\leadsto}^{\text{Elementare Zeilenumformungen}\leadsto\text{Gauß}}\cdots$$
	→ $Ax=0$ bildet das zugehörige *homogene System*
^1673218899955

## Fachtermini
- *Homogenes System*: Es gilt $b_1=\dots=b_m=0$
- *Lösungsmenge*: $\mathcal{L}:=\{(x_1,\dots,x_n)\in K^n\mid\text{Alle Gleichungen sind simultan erfüllt}\}$
- *Spezielle Lösung*: $\xi\in\mathcal{L}$ für ein inhomogenes Systems $Ax=b,$ also so dass $A\xi=b$

## Eigenschaften

### [[#Fachtermini|Spezielle Lösung]] (2) #fc
- Sei $\xi$ gegeben für $Ax=b,$ also $A\xi=b,$ dann gilt:
	1. $\forall\eta\text{ mit }A\eta=b:\xi-\eta$ löst das zugehörige *homogene System* $Ax=0$
	2. Umkehrung: $\forall\nu\in K^n\text{ mit }A\nu=0:\xi+\nu$ löst das zugehörige *inhomogene LGS* $Ax=b$
^1673218899964

### Allgemein #fc
- Die *Lösungsmenge* $\mathcal{L}$ eines LGS' ist immer ein [[Affine Unterräume#Definition fc|affiner Unterraum]] der Form $\xi+\text{ker}(A)$ von $K^n$
	→ $\xi:$ [[Lineare Gleichungssysteme|spezielle Lösung]], $\text{ker}(A):$ [[../4. Lineare Abbildungen/Lineare Abbildungen|Kern der linearen Abbildung]] $K^n\to K^m,x\mapsto Ax$
> Hier wurde $\mathcal{L}$ willkürlich als Symbol für den Lösungsraum $L$ definiert
^1673219708733

## Homogene LGS

### Wichtige Eigenschaften (2) #fc
- Die *Lösungsmenge* eines homogenen Gleichungssystems $Ax=0$ entspricht dem [[../4. Lineare Abbildungen/Kern#Definition fc|Kern]] der linearen Abbildung ([[../2. Gruppen-Ringe-Körper/Matrizen#Produkt fc|Matrixmultiplikation]]) $$K^n\to K^m,\quad x\mapsto Ax$$
> Siehe auch [[../4. Lineare Abbildungen/Darstellende Matrizen#Beispiele fc|darstellende Matrix > Beispiele]]
- Die *Lösungsmenge* eines *homogenen linearen Gleichungssystems* ist immer auch ein [[../3. Vektorräume/Untervektorräume#Untervektorräume|Unterraum]] von $K^n$
	→ Der Nullvektor $\in K^n$ stellt die triviale Lösung eines homogenen GS dar
^1673218899967
