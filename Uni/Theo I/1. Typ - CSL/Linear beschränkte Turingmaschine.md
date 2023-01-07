---
tags: uni theo-1 theoretical-cs automata
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Linear beschränkte Turingmaschine
  - Linear beschränkter Automat
  - LBA
  - LBA-Problem
linter-yaml-title-alias: Linear beschränkte Turingmaschine
date-of-creation: 2022-09-10
mod-date: 2022-10-31
---

# Linear beschränkte Turingmaschine

## Definition: #fc
- Sei $\Sigma$ definiert als $\Sigma\cup\{\hat{a}\mid a\in\Sigma\},$ wobei $a$ das letzte Element der Eingabe ist
- Eine [[../Turingmaschinen|nichtdeterministische Turingmaschine]] $M$ ist *linear beschränkt*, wenn $\forall a_1,\dots,a_n\in\Sigma^+,~\forall\alpha,\beta\in\Gamma^{Stern},~z\in Z$ mit $\textbf{z}_\textbf{0}a_1\dots a_{n-1}\hat{a}_n~\vdash~\alpha\textbf{z}\beta:|\alpha\beta|=n$ gilt
	→ Eine linear beschränkte NTM verlässt niemals den *Platz der Eingabe*, und das ohne "in die Zukunft schauen zu können"
- Die von dem LBA akzeptierte Sprache sei definiert als
$$T(M)=\{a_1\dots a_n\in\Sigma^{Stern}\mid\exists z\in E:\textbf{z}_\textbf{0}a_1\dots a_{n-1}\hat{a}_n~\vdash~\alpha\bf{z}\beta\}$$
^1664631339761

## Eigenschaften: #fc
- Die Klasse der von einem LBA akzeptiert Sprachen ist gleich der der [[../Typ-1|Typ-1]] Sprachen
	→ $O.B.d.A:\{L\mid \varepsilon\notin L\}$
- Das noch offene *LBA-Problem*: Gilt $\text{LBA}=\text{DLBA}?$
	→ [[../../Theo II/Komplexitättheorie/Platzklassen/SPACE|DSPACE]](n) = [[../../Theo II/Komplexitättheorie/Platzklassen/NSPAC|NSPACE]](n)?
^1664631339769
