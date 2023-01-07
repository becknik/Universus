---
tags: uni theo-1 theoretical-cs automata chomsky
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Kellerautomat
  - PDA
  - Pushdown Automaton
linter-yaml-title-alias: Kellerautomat
date-of-creation: 2022-09-21
mod-date: 2022-10-31
---

# Kellerautomat
→ [[Deterministische Kellerautomaten|Deterministische Kellerautomaten]]

## Definition: #fc
- Definiert durch das *6-Tupel*:
$$M=(Z,\Sigma,\Gamma,\delta,z_0,\#)$$
- $Z:$ Die endliche, nicht-leere *Zustandsmenge*
- $\Sigma:$ Das endliche, nicht-leere *Alphabet*
	→ $Z\cap\Sigma=\emptyset$
- $\Gamma:$ Das endliche *Keller-/Bandalphabet*
	→ $Z\cap\Gamma=\emptyset$
- Die [[../Grundlegendes/Nichtdeterminismus|nichtdeterministische]] *Zustandsüberführungsfunktion* $$\delta:Z\times(\Sigma\cup\{\varepsilon\})\times\Gamma\rightarrow\mathcal{P}_e(Z\times\Gamma^{Stern})$$
	→ $\mathcal{P}_e:$ Eine endliche Teilmenge der potenzierten Menge
- $z_0:$ Der *Anfangszustand* $\in Z$
- $\#:$ Das *Kellerbottom-Symbol* $\in\Gamma\setminus\Sigma$
^1664631244236

## Konfiguration: #fc
$$k:Z\times\Sigma^{Stern}\times\Gamma^{Stern}$$
- Der Kellerautomat befindet sich in einem *Zustand* $z\in Z,$ …
	- … liest auf dem Eingabeband das den *vordersten Buchstaben* des Worts $w\in\Sigma^{Stern}$ und …
	- … peekt das *oberste Keller-Symbol* $A_m$ vom [[../../DSA/Datenstrukturen/Stack|Stack/ Kellerspericher]] $V=A_1A_2\dots A_m$
- *Konfigurationsübergänge*: Sei $$(z,\textbf{a}_\textbf{1}\dots a_n,A_1\dots A_m)$$ die aktuelle Konfiguration und $(z',B_1\dots B_k)\in\delta(z,a_1,A_1),$ dann resultiert daraus die Konfiguration $$(z',\textbf{a}_\textbf{2}\dots a_n,B_1\dots B_kA_2\dots A_m)$$
	→ Übergänge zwischen (zwei) Konfigurationen werden wieder mit $\vdash/\vdash^{Stern}$ angegeben
	→ $\varepsilon$-Übergänge: $(z,\textbf{a}_\textbf{1}\dots a_n,A_1\dots A_m)\vdash(z',\textbf{a}_\textbf{1}\dots a_n,B_1\dots B_kA_2\dots A_m)$
- Ein PDA akzeptiert durch *leeren Keller*: $$N(M)=\{w\in\Sigma^{Stern}\mid\exists z\in Z:(z_0,w,\#)\vdash^{Stern}(z,\textbf{ε},\varepsilon)\}$$
	→ Vergleiche mit [[Deterministische Kellerautomaten|DPDA]]
^1664631244245

## Eigenschaften #fc
- Ein [[../Automaten|Automat]] wie ein [[../3. Typ - REG/Nichtdeterministischer Endlicher Automat|NFA]], nur dass er einen zusätzlichen [[../../DSA/Datenstrukturen/Stack|Stack/ Kellerspeicher]] besitzt
- Akzeptiert durch einen *leeren Keller*, wenn die Eingabe zu dem Zeitpunk komplett gelesen wurde
	→ Akzeptierung durch einen Endzustand ist äquivalent (Beweis: in den Übungen)
- Es $\exists$ ein PDA $M$ für $L\subseteq\Sigma^{Stern}\Leftrightarrow L\in$ der Sprachklasse [[../Typ-2|CFL]]
	→ $O.B.d.A:\{L\mid \varepsilon\notin L\}$ (V.19 F.37.1)
^1664631244250

### Ein (nützlicher) Satz:
- Für den PDA $M$ mit $\forall z,z'\in Z$, $\forall w,w'\in\Sigma^{Stern}$ und $\forall V,V',Y\in\Gamma^{Stern}$ gilt: $$(v,w,V)\vdash^{Stern}(z',w'V')\Rightarrow(z,wx,VY)\vdash^{Stern}(z',w'x,V'Y)$$

### Umwandlungen in gleichwertige PDAs: #fc
- Jeder PDA $M$ kann in einen *gleichwertigen* PDA $M'$ umgewandelt werden, sodass $N(M)=N(M')$ gilt und $M'$ *nur einen Zustand* hat
- Jeder PDA kann so *umgewandelt* werden, dass er immer *nur ein Zeichen als Eingabe* liest (also in Echtzeit arbeitet)
	→ Folgt aus dem Beweis $\text{PDA}\Rightarrow\text{Typ-2}$
	→ Einen solchen PDA $M'$ erhält man durch $\text{PDA }M\Rightarrow\text{Grammatik }G\Rightarrow\text{CNF }G'\Rightarrow\text{PDA }M'$ (?)
^1667239830513

> *Ich verstehe nicht, was auf V.17 F.32.6 mit "gemäß Satz 1" gemeint ist*

## Vom PDA zur Grammatik:
- Gegeben: Ein PDA $M=(Z,\Sigma,\Gamma,\delta,z_0,\#),$ der $o.B.d.A.$ den Keller pro Schritt um maximal ein Symbol vergrößert
- Entwerfe $V=\{S\}\cup Z\times\Gamma\times Z,(p,A,q),$ sodass $M$ in $p$ das Kellersymbol $A$ liest, $q$ angenommen wird und die *Höhe des Kellers kleiner als zu Beginn ist* (?)
- Entwerfe $P:$
	1. $\forall z\in Z:(S\rightarrow(z_0,\#,z))\in P$
	2. $\forall a\in\Sigma\cup\varepsilon:(z',\varepsilon)\in\delta(z,a,A)\quad\Leftrightarrow\quad((z,A,z')\rightarrow a)\in P$
	3. $\forall a\in\Sigma\cup\varepsilon:(z_1,B)\in\delta(z,a,A)\quad\Leftrightarrow\quad((z,A,z')\rightarrow a(z_1,B,z'))\in P$
	4. $\forall a\in\Sigma\cup\varepsilon:(z_1,BC)\in\delta(z,a,A)\quad\Leftrightarrow\quad((z,A,z')\rightarrow a(z_1,B,z_2)(z_2,C,z'))\in P$

## Beispiele
- Siehe V.16 F.30.4 ff.
