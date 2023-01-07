---
tags: uni theo-2 theoretical-cs computability applicative
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: µ-Rekursion
linter-yaml-title-alias: µ-Rekursion
date-of-creation: 2022-08-08
mod-date: 2022-10-02
---

# µ-Rekursion

## Definition: #fc
- Sei $f:\mathbb{N}^{k+1}\rightarrow\mathbb{N}$, dann ist $\mu f$ definiert als $\mathbb{N}^k\rightarrow \mathbb{N}$ mit
$$\displaylines{\mu f(x_1,\dots,x_k)=\min(n\in \mathbb{N}\mid f(n,x_1,\dots,x_k)=0~\wedge\\\forall m<n:f(m,x_1,\dots,x_k)>0\Rightarrow f(m,x_1\dots,x_k)\neq\bot)}$$
	→ $\mu f=\bot,$ wenn entweder $\forall n:f(n,x_1,\dots,x_k)>0$ oder $\exists n:f(n,x_1,\dots,x_k)=\bot\wedge \forall m<n: f(m,x_1,\dots,x_k)>0$
^1660502724730

## Eigenschaften: #fc
- Die Klasse der $\mu$-rekursiven Funktionen ist die kleinste Funktionen-Klasse, die…
	- … die *Basisfunktionen enthält*
	- … abgeschlossen ist unter *Einsetzen*
	- … abgeschlossen ist unter [[Primitive Rekursion|primitive Rekursion]]
	- … abgeschlossen ist unter Anwendung des $\mu$-Operators
- Eine Funktion ist $\mu$-rekursiv, genau dann, wenn sie [[../../WHILE-berechenbar|WHILE-berechenbar]] ist
	→ Zu $P \equiv \text{ WHILE }x_i\neq0\text{ DO }Q\text{ END}$ gibt es die Funktion $g(m,y) = d_i(f(m,y))$, die den Wert von $x_i$ nach $m$ Schleifenabläufen liefert
	→ $\mu f$ liefert den ersten Zeitpunkt, zu dem $x_i=0$ gilt: $g_P(n)=f(\mu g(n),n)$
- [[../../Satz von Kleene|Satz von Kleene]]
^1664742180863
