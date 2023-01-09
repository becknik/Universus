---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Lineare Abbildungen
  - lineare Abbildung
  - linear
  - Rang
linter-yaml-title-alias: Lineare Abbildungen
date-of-creation: 2022-12-04
mod-date: 2023-01-09
---

# Lineare Abbildungen

## Definition #fc
- Seien $V,W$ [[../3. Vektorräume/Vektorräume#Definition fc|Vektorräume]] über demselben [[../2. Gruppen-Ringe-Körper/Körper|Körper]] $K,$ dann gilt:
- Eine [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]] $f:V\to W$ heißt *linear*, wenn sie die folgende Eigenschaften erfüllt:
	1. *Addititvität*: $$\forall v_1,v_2\in V:\quad f(v_1+v_2)=f(v_1)+f(v_2)=w\in W$$
	2. "Verträglichkeit mit der Skalarmultiplikation": $$\forall v\in V,\lambda\in K:\quad f(\lambda v)=\lambda f(v)\in W$$
- Zusammengefasst muss für eine lineare Abbildung also \$$$\forall v_1,v_2\in V,\lambda_1,\lambda_2\in K:\quad f(\lambda_1v_1+\lambda_2v_2)=\lambda_1f(v_1)+\lambda_2f(v_2)$$ gelten
^1670185338428

## Rang

### Definition #fc
- Als *Rang* einer [[Lineare Abbildungen#Definition fc|lineare Abbildung]] bezeichnet man die [[../3. Vektorräume/Dimensionen#Definition fc|Dimension]] ihres [[../1. Logik-Mengenlehre-Relationen/Abbildungen#Fachtermini|Bildes]]
	$$rk(f):=\text{dim}(\text{Bild}(f))$$
^1673207850516

## Typen von [[Lineare Abbildungen#Definition fc|Linearen]]/ [[../3. Vektorräume/Vektorräume#Definition fc|Vektorraum]]-\*Morphismen (6) #fc
- Für die lineare Abbildung $f:V\to W:f$ ist ein linearer/ Vektorraum-…
	- *Homo*morphismus
	- *Mono*morphismus $\Longleftrightarrow f$ ist [[../1. Logik-Mengenlehre-Relationen/Abbildungen#Injektivität fc|injektiv]]
	- *Epi*morphismus $\Longleftrightarrow f$ ist [[../1. Logik-Mengenlehre-Relationen/Abbildungen#Surjektivität fc|surjektiv]]
	- *Iso*morphismus $\Longleftrightarrow f$ ist *bijektiv*
		→ Man nennt $V$ und $W$ dann *isomorph* und schreibt $V\cong W$
	- *Endo*morphismus $\Longleftrightarrow W=V$
	- *Auto*morphismus $\Longleftrightarrow W=V\wedge f$ is *bejktiv*
^1673124789875

## Hilfssatz 4.1.5
- Seien $V,W$ [[../3. Vektorräume/Vektorräume|Vektorräume]] und $f:V\to W$ ein [[#Typen von Lineare Abbildungen Definition fc Linearen / ../3. Vektorräume/Vektorräume Definition fc Vektorraum - *Morphismen fc|Vektorraumisomorphismus]], dann ist $f^{-1}:W\to V$ [[Lineare Abbildungen#Definition fc|linear]] und ein Vektorraum*iso*morphismus

## Dimensionsformel #fc
- Sei $f:V\to W$ eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]] und $\text{dim}(V)<\infty,$ dann gilt: \$$$\text{dim}(V)=rk(f)+\text{dim}(\text{ker}(f))$$
	→ $rk=$ [[#Rang#Definition fc|Rang]] und $\text{ker}=$ [[Kern]]
^1673207850521

### Folgerung 4.2.5
- Sei $f:V\to W$ eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]] und $\text{dim}(V)=\text{dim}(W)<\infty,$ dann gilt, dass die *Abbildung* von $f$ genau dann [[../1. Logik-Mengenlehre-Relationen/Abbildungen|surjektiv]] ist, wenn sie [[../1. Logik-Mengenlehre-Relationen/Abbildungen|injektiv]] ist

### Satz 4.3.5
- Seien $f,g$ [[Lineare Abbildungen#Definition fc|lineare Abbildungen]] mit $g:V\to W,f:W\to X$ und gewählter [[../3. Vektorräume/Erzeugendensysteme#Basis fc|Basis]]
- Seien $A,B$ jeweils die [[Darstellende Matrizen|darstellende Matrizen]] von $f$ und $g,$ dann ist das Matrizenprodukt $A\cdot B$ die *darstellende Matrix* von $f\circ g$

## Beispiele
- $f:\mathbb{R}^2\to\mathbb{R},f(x,y)=2x-y$ ist eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]]:
	- *Additvität*: $f((x_1,y_1)+(x_2,y_2))=f(x_1+x_2,y_1+y_2)=2x_1+2x_2-y_1-y_2=f(x_1,y_1)+f(x_2,y_2)$
	- "Verträglichkeit mit dem *Skalarprodukt*": $f(\lambda x,\lambda y)=2\lambda x−\lambda y=\lambda f(x,y)$
- [[../2. Gruppen-Ringe-Körper/Matrizen#Produkt fc|Matrixmultiplikation]]
- Die Verkettung von linearen Abbildungen
- Sei $V$ der [[../3. Vektorräume/Vektorräume#Definition fc|Vektorraum]] der differenzierbaren reellen Funktionen $f:\mathbb{R}\to\mathbb{R},$ dann ist die Differentiation $f\mapsto f'$ ([[Ableitung]]) eine lineare Abbildung
	→ Es gilt: $(f+g)'=f'+g'$ und $(\lambda\cdot f)'=\lambda\cdot(f')$
