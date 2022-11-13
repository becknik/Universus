---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
complete: true
aliases: Zahlenmengen
linter-yaml-title-alias: Zahlenmengen
date: 2022-11-02
mod-date: 2022-11-07
---

# Zahlenmengen

## Rationale Zahlen

### Konstruktion aus $\mathbb{Z}$ und $\mathbb{Q}$: #fc
- Man definiere die [[Logik-Mengenlehre-Relationen/Äquivalenzrelationen|Äquivalenzrelation]] $R$ über $A=\mathbb{Z\times N}$ mit $$R:=\{(n,m),(n',m')\in A\times A\mid nm'=n'm\}$$
- Man kürze $\mathcal{K}((n,m),R)$ ab als $n/m$ oder $\frac{n}{m}$
- Man definiere ein *vollständig gekürztes Paar* als $(n,m)\in A,$ für das $\not\exists k\in\mathbb{N},k>1:\quad n\mid k\wedge m\mid k$ gilt
	-> Man definiere $B:=\{(n,m)\in A\mid (n,m)\text{ ist vollständig gekürzt}\}$ als *Repräsentantensystm* der [[Logik-Mengenlehre-Relationen/Äquivalenzklassen|Äquivalenzklasse]]
-> Man definiert $\mathbb{Q}:=\mathcal{K}(A,R)$
^1667399525643

## Komplexe Zahlen

### Definition:
- $\mathbb{C}:=\{a\pm ib\}$
- Realteil $\Re((a,b))=a$
- Imaginärteil $\Im((a,b))=b$
- $1^2:=-1$

### Konjungierte komplexe Zahl:
- Zu jeder komplexen Zahl $z\in\mathbb{C}$ definiert man die zu $z$ komplex konjungierte Zahl   als $$\overline{z}:=(a,-b)=\Re(z)-i\Im(z)$$

## Kontiuumshypothese #fc
- Frage: Ist $\mathcal{P}(\mathbb{N})$ gleich mächtig zu $\mathbb{R}$?
^1667838948578
