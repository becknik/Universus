---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Logspace-Reduktion
date-of-creation: 2022-08-12
mod-date: 2022-08-20
linter-yaml-title-alias: Logspace-Reduktion
---

# Logspace-Reduktion

## Definition: #fc
- Seien $A,B\subseteq\Sigma^{Stern}$ und $A,B$ logspace-reduzierbar, wenn $\exists f$ [[Platzklassen/Logspace-Transducer|logspace-berechenbare]] Funktion mit $\Sigma^{Stern}\rightarrow\Sigma^{Stern},$ so dass $x\in A\Leftrightarrow f(x)\in B$
	→ Notation: $A\leq_{\log} B$ oder $A\leq^{\log}_m B$
^1660859281072

## Eigenschaften: #fc
- Alles, was mit $\leq_p$ gezeigt wurde, lässt sich auch mit $\leq_{\log}$ zeigen
	→ [[Zeitklassen/NP|NP]] und [[Zeitklassen/P|P]] sind unter $\leq_{\log}$ abgeschlossen
	→ Falls $\leq_p$ und $\leq_{\log}$ übereinstimmen gilt [[Platzklassen/L|L]] = [[Zeitklassen/P|P]]
- Für $F\in\leq_{\log}$-reduzierbar$:DTIME(f)\in P$, da sich höchstens $c^{\log n}$ Konfigurationen auf dem Berechnungsband des [[Platzklassen/Logspace-Transducer|Logspace-Transducers]] ergeben, also $=n^{c'}$
	→ $\leq_{\log}$ verfeinert $\leq_p$
- *Transitivität*: $A\leq_{\log}B\wedge B\leq_{\log}C\Rightarrow A\log_{\log}C$ gilt nicht wie bei $\leq_p$, da $g\circ f$ aufgrund des Zugriffs auf das Ausgabebands von $g$, das polynomiell groß ist, auch polynomiell groß ist
	→ Man wendet *Recomputation*-Prinzip (F38.6) an um die Transitivität zu zeigen
^1660502862055
