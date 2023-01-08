---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Lineare Abbildungen
  - lineare Abbildung
  - linear
  - Kern einer linearen Abbildung
  - Basis einer linearen Abbildung
  - Rang einer linearen Abbildung
linter-yaml-title-alias: Lineare Abbildungen
date-of-creation: 2022-12-04
mod-date: 2023-01-08
---

# Lineare Abbildungen

## Definition #fc
- Seien $V,W$ [[../3. Vektorräume/Vektorräume|Vektorräume]] über demselben [[../2. Gruppen-Ringe-Körper/Körper|Körper]] $K$
- Eine [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]] $f:V\to W$ heißt *linear*, wenn folgendes gilt:
	1. *Addititvität*: $\forall v_1,v_2\in V:\quad f(v_1+v_2)=f(v_1)+f(v_2)=w\in W$
	2. "Verträglichkeit mit der Skalarmultiplikation": $\forall v\in V,\lambda\in K:$$f(\lambda v)=\lambda f(v)\in W$
- Zusammengefasst muss also gelten: $$\forall v_1,v_2\in V,\lambda_1,\lambda_2\in K:\quad f(\lambda_1v_1+\lambda_2v_2)=\lambda_1f(v_1)+\lambda_2f(v_2)$$
^1670185338428

### Rang #fc
- Als *Rang* einer [[Lineare Abbildungen#Definition fc|lineare Abbildung]] bezeichnet man die [[../3. Vektorräume/Dimensionen#Definition fc|Dimension]] ihres [[../1. Logik-Mengenlehre-Relationen/Abbildungen#Fachtermini|Bildes]]
	$$rk(f):=\text{dim}(\text{Bild}(f))$$
^1673207850516

## Typen von [[Lineare Abbildungen#Definition fc|Linearen]]/ [[../3. Vektorräume/Vektorräume#Definition fc|Vektorraum]]-\*Morphismen (6) #fc
- Für $f:V\to W:$ linearer/ Vektorraum-…
	- *Homo*morphismus: Eine lineare Abbildung
	- *Mono*morphismus: Eine [[../1. Logik-Mengenlehre-Relationen/Abbildungen#Injektivität fc|injektive]] lineare Abbildung
	- *Epi*morphismus: Eine [[../1. Logik-Mengenlehre-Relationen/Abbildungen#Surjektivität fc|surjektive]] lineare Abbildung
	- *Iso*morphismus: Eine *bijektive* lineare Abbildung
		→ Man nennt $V$ und $W$ dann *isomorph* und schreibt $V\cong W$
	- *Endo*morphismus: Eine lineare Abbildung $f:V\to V$
	- *Auto*morphismus: Eine *bejktive* lineare Abbildung $f:V\to V$
^1673124789875

## Hilfssatz 4.1.5
- Seien $V,W$ [[../3. Vektorräume/Vektorräume|Vektorräume]] und $f:V\to W$ ein [[#Typen von Lineare Abbildungen Definition fc Linearen / ../3. Vektorräume/Vektorräume Definition fc Vektorraum - *Morphismen fc|Vektorraumisomorphismus]], dann ist $f^{-1}:W\to V$ [[Lineare Abbildungen#Definition fc|linear]] und ein Vektorraum*iso*morphismus

## Kern

### Definition #fc
- Sei $f:V\to W$ eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]], dann definiert \$$$f^{-1}(\{0\})=\{v\in V\mid f(v)=0\}$$ den [[../2. Gruppen-Ringe-Körper/Gruppenhomomorphismus|Kern]] dieser Abbildung
→ Der Kern besteht aus allen Vektoren, die auf den *Nullvektor* abgebildet werden
- Der Kern der linearen Abbildung $f$ wird als $\text{ker}(f)$ notiert
^1670190701413

### Eigenschaften (3) #fc
- Der *Kern* einer [[Lineare Abbildungen#Definition fc|lineare Abbildung]] $f:V\to W$ bildet einen [[../3. Vektorräume/Untervektorräume|Untervektorraum]] von $V$
- Das [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Bild]] einer *lineare Abbildung* $f:V\to W$ stellt ein *Untervektorraum* von $W$ dar
- Eine *lineare Abbildung* ist genau dann [[../1. Logik-Mengenlehre-Relationen/Abbildungen|injektiv]], wenn der *Kern* nur aus dem *0-Vektor* besteht
^1670190701419

## Dimensionsformel #fc
- Sei $f:V\to W$ eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]] und $\text{dim}(V)<\infty,$ dann gilt: \$$$\text{dim}(V)=rk(f)+\text{dim}(\text{ker}(f))$$
	→ $rk=$ [[#Rang fc|Rang]] und $\text{ker}=$ [[#Kern]]
^1673207850521

### Satz 4.3.5
- Seien $f,g$ [[Lineare Abbildungen#Definition fc|lineare Abbildungen]] mit $g:V\to W,f:W\to X$ und gewählter [[../3. Vektorräume/Erzeugendensystem#Basis fc|Basis]]
- Seien $A,B$ jeweils die *darstellenden Matrizen* von $f$ und $g,$ dann ist das Matrizenprodukt $A\cdot B$ die *darstellende Matrix* von $f\circ g$

### Folgerung
- Sei $f:V\to W$ eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]] und $\text{dim}(V)=\text{dim}(W)<\infty$ dann gilt, dass die *Abbildung* von $f$ genau dann [[../1. Logik-Mengenlehre-Relationen/Abbildungen|surjektiv]] ist, wenn sie [[../1. Logik-Mengenlehre-Relationen/Abbildungen|injektiv]] ist

## Beispiele
- $f:\mathbb{R}^2\to\mathbb{R},f(x,y)=2x-y$ ist eine [[Lineare Abbildungen#Definition fc|lineare Abbildung]]:
	- *Additvität*: $f((x_1,y_1)+(x_2,y_2))=f(x_1+x_2,y_1+y_2)=2x_1+2x_2-y_1-y_2=f(x_1,y_1)+f(x_2,y_2)$
	- "Verträglichkeit mit dem *Skalarprodukt*": $f(\lambda x,\lambda y)=2\lambda x−\lambda y=\lambda f(x,y)$

### [[../2. Gruppen-Ringe-Körper/Matrizen|Spaltenvektoren]] #fc
- $f:K^n\to K^m$ ist *linear*
	→ *Additivität* folgt aus dem *Distributivgesetz*
	→ *Verträglichkeit mit der Skalarmultiplikation* folgt aus der Definition der *Matrixmultiplikation*
^1670186696099

### Differentiation: $f\mapsto f'$ #fc
- Sei $V$ der [[../3. Vektorräume/Vektorräume|Vektorraum]] der *differenzierbaren* reelen Funktionen $f:\mathbb{R}\to\mathbb{R},f\mapsto f'$
- $f$ ist eine *lineare [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]]*, denn es gilt $(f+g)'=f'+g'$ und $(\lambda\cdot f)'=\lambda\cdot(f')$
^1670186696102

### Verkettung von linearen Abbildungen #fc
- Seien $f:V\to W,g:W\to X$ lineare [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildungen]] und $v_1,v_2\in V,\lambda_1,\lambda_2\in K,$ dann folgt $$g(f(λ_1v_1+λ_2v_2))=g(λ_1g(v_1)+λ_2g(v_2))=λ_1g(f(v_1))+λ_2g(f(v_2))$$
^1670186696104
