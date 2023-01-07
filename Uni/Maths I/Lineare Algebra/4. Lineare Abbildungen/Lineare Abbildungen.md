---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Lineare Abbildungen
  - lineare Abbildung
linter-yaml-title-alias: Lineare Abbildungen
date-of-creation: 2022-12-04
mod-date: 2022-12-04
---

# Lineare Abbildungen

## Definition #fc
- Seien $V,W$ [[../3. Vektorräume/Vektorräume|Vektorräume]] über demselben [[../2. Gruppen-Ringe-Körper/Körper|Körper]] $K$
- Eine [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]] $f:V\to W$ heißt *linear*, wenn folgendes gilt:
	1. *Addititvität*: $\forall v_1,v_2\in V:\quad f(v_1+v_2)=f(v_1)+f(v_2)$
	2. "Verträglichkeit mit der Skalarmultiplikation": $\forall v\in V,\lambda\in K:\quad f(\lambda v)=\lambda f(v)$
→ Zusammengefasst: $$\forall v_1,v_2\in V,\lambda_1,\lambda_2\in K:\quad f(\lambda_1v_1+\lambda_2v_2)=\lambda_1f(v_1)+\lambda_2f(v_2)$$
^1670185338428

## Übliche Sprechweisen

### [[../3. Vektorräume/Vektorräume|Vektorraum]][[../../../Theo I/3. Typ - REG/Homomorphismus|homomorphismus]]/ linearer Homomorphismus #fc
- Für eine [[Lineare Abbildungen|lineare Abbildung]] $f:V\to W$
^1670186676053

### [[../3. Vektorräume/Vektorräume|Vektorraum]][[../../../Theo I/3. Typ - REG/Homomorphismus|monomorphismus]]/ linearer Monomorphismus #fc
- Für eine [[Lineare Abbildungen|lineare Abbildung]] $f:V\to W,$ die sich [[../1. Logik-Mengenlehre-Relationen/Abbildungen|injektiv]] verhält
^1670186676057

### [[../3. Vektorräume/Vektorräume|Vektorraum]][[../../../Theo I/3. Typ - REG/Homomorphismus|epimorphismus]]/ linearer Epimorphismus #fc
- Für eine [[Lineare Abbildungen|lineare Abbildung]] $f:V\to W,$ die sich [[../1. Logik-Mengenlehre-Relationen/Abbildungen|surjektiv]] verhält
^1670186676060

### [[../3. Vektorräume/Vektorräume|Vektorraum]][[../../../Theo I/3. Typ - REG/Homomorphismus|isomorphismus]]/ linearer Isomorphismus #fc
- Für eine [[Lineare Abbildungen|lineare Abbildung]] $f:V\to W,$ die sich [[../1. Logik-Mengenlehre-Relationen/Abbildungen|bijektive]] verhält
	→ Wenn ein *Vektorraumisomorphismus* zwischen zwei $K$-[[../3. Vektorräume/Vektorräume|Vektorräumen]] $V$ und $W$ existiert, sagt man die beiden Vektorräume sind *isomorph* ($V\cong W$)
^1670186676063

### [[../3. Vektorräume/Vektorräume|Vektorraum]][[../../../Theo I/3. Typ - REG/Homomorphismus|endomorphismus]]/ linearer Endomorphismus #fc
- Für eine [[Lineare Abbildungen|lineare Abbildung]] $f:V\to V$
^1670186970619

### [[../3. Vektorräume/Vektorräume|Vektorraum]][[../../../Theo I/3. Typ - REG/Homomorphismus|automorphismus]]/ linearer Automorphismus #fc
- Für eine [[Lineare Abbildungen|lineare Abbildung]] $f:V\to V,$ die sich [[../1. Logik-Mengenlehre-Relationen/Abbildungen|bijektiv]] verhält
^1670186973053

## Hilfssatz 4.1.5
- Seien $V,W$ [[../3. Vektorräume/Vektorräume|Vektorräume]] und $f:V\to W$ ein *Vektorraumhomomorphismus*, dann ist $f^{-1}:W\to V$ *linear* und ein Vektorraumhomomorphismus

## Kern #fc
- Sei $f:V\to W$ eine *lineare* [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]]
$$f^{-1}(\{0\})=\{v\in V\mid f(v)=0\}$$ besteht aus allen Vektoren, die auf den *Nullvektor* abgebildet werden
	→ Stellt den [[../2. Gruppen-Ringe-Körper/Gruppenhomomorphismus|Kern]] von $f$ dar und wird als $\text{ker}(f)$ notiert
^1670190701413

### Beziehung zu [[../3. Vektorräume/Vektorräume|Vektorräumen]] #fc
- Der *Kern* einer *linearen* [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]] $f:V\to W$ bildet einen [[../3. Vektorräume/Untervektorräume|Untervektorraum]] von $V$
- Das [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Bild]] von $f$ ist ein *Untervektorraum* von $W$
^1670190701416

### Eigenschaften #fc
- Eine *lineare Abbildung* ist genau dann [[../1. Logik-Mengenlehre-Relationen/Abbildungen|injektiv]], wenn der *Kern* nur aus dem *0-Vektor* bsteht
^1670190701419

## Beispiele

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
