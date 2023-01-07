---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases: Zahlenmengen
linter-yaml-title-alias: Zahlenmengen
date-of-creation: 2022-11-02
mod-date: 2022-11-07
---

# Zahlenmengen

## Rationale Zahlen $\mathbb{Q}$

### Konstruktion aus $\mathbb{Z}$ und $\mathbb{N}$ #fc
- Sie $R$ eine [[1. Logik-Mengenlehre-Relationen/Äquivalenzrelationen|Äquivalenzrelation]] über $A$ mit $A=\mathbb{Z\times N}$ und $$R:=\{(n,m),(n',m')\in A\times A\mid nm'=n'm\}$$
- Anstelle von $\mathcal{K}((n,m),R)$ notiert man $a\in R$ als $n/m$ oder $\frac{n}{m}$
- Definition eines *vollständig gekürztes Paar* als $(n,m)\in A,$ für das $\not\exists k\in\mathbb{N},k>1:\quad n\mid k\wedge m\mid k$ gilt
	→ Sei $B:=\{(n,m)\in A\mid (n,m)\text{ ist vollständig gekürzt}\}$ das *Repräsentantensystem* von $R$
$$\mathbb{Q}:=\mathcal{K}(A,R)$$
^1667399525643

## Komplexe Zahlen

### Definition
- $\mathbb{C}:=\{a\pm ib\}$
- Realteil $\Re((a,b))=a$
- Imaginärteil $\Im((a,b))=b$
- $1^2:=-1$

### Konjungierte komplexe Zahl
- Zu jeder komplexen Zahl $z\in\mathbb{C}$ definiert man die zu $z$ komplex konjungierte Zahl als $$\overline{z}:=(a,-b)=\Re(z)-i\Im(z)$$

## Kontiuumshypothese #fc
- Frage: Ist $\mathcal{P}(\mathbb{N})$ gleich mächtig zu $\mathbb{R}$?
^1667838948578
