---
tags: uni theo-1 theoretical-cs automata formal-languages
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Deterministische Kellerautomaten
  - DPDA
  - DCFL
linter-yaml-title-alias: Deterministische Kellerautomaten
date-of-creation: 2022-09-21
mod-date: 2022-10-02
---

# Deterministische Kellerautomaten

## Definition: #fc
- Definiert durch das *7-Tupel*:
$$M=(Z,\Sigma,\Gamma,\delta,z_0,\#,F)$$
- Entspricht im Groben einen [[Kellerautomat|PDA]], bei dem die *Überführungsfunktion* $\delta$ als $$\forall a\in\Sigma,z\in Z,A\in\Gamma:\quad|\delta(z,a,A)|+|\delta(z,\varepsilon,A)|\leq1$$ definiert ist und der in einem *Endzustand akzeptiert*: $$N(M):=\{x\in\Sigma^{Stern}\mid\exists z\in F,V\in\Gamma^{Stern}:(z_0,x,\#)\vdash^{Stern}(z,\varepsilon,V)\}$$
^1664631135086

## Eigenschaften: #fc
- Definiert die Sprachklasse $\text{DCFL}$ als $L\subseteq\Sigma^{Stern}:\exists\text{PDA }N(M)\text{ mit }N(M)=L$
- [[Typ-3|REG]] $\subsetneq\text{DCFL}:$ Ein [[3. Typ - REG/Deterministischer Endlicher Automat|DFA]] ist ein DPDA, der seinen Keller nicht nutzt
$$\text{REG}\subsetneq\text{DCFL}\subseteq\text{CFL}$$
	→ Die Menge der unmarkierten Palindrome ist $\in$ [[Typ-2|CFL]]$\setminus\text{DCFL}$
- Die [[../Formale Sprachen|Sprache]] der markierte Palindrome $L=\{w\#w^R\mid w\in\Sigma^{Stern}\},\#\notin\Sigma,\#\notin w$ liegen in $\text{DCFL}$
- Beschreibt die Klasse der Sprachen, die sich durch [[LR(k) Grammatik]]en erzeugen lassen
	→ Hier existiert scheinbar ein Algorithmus $\in\mathbfcal{O}(n)$
^1664631135091
