---
tags: uni theo-2 theoretical-cs complexity
cards-deck: Uni::Courses::Theo-II
completed: false
aliases:
  - Reduktion
  - polynomialzeit Reduktion
linter-yaml-title-alias: Reduktion
date-of-creation: 2022-07-03
mod-date: 2022-09-10
---

# Reduktion

## Definition: #fc
- Sei $A \subseteq\Sigma^{Stern}$ und $B\subseteq\Gamma^{Stern}$
- Es gilt $A \leq B$, falls $\exists$ eine totale, [[Berechenbarkeit|berechenbare]] Funktion $f:\Sigma^{Stern}\rightarrow \Gamma^{Stern}$, sodass $$x \in A \Longleftrightarrow f(x) \in B$$
- *Aussage*: $A$ ist *höchstens gleich-schwierig* wie $B$, da $A$ auf $B$ *zurückgeführt* wird
	→ Wenn es also für $B$ ein *berechenbaren Algorithmus* gibt, so lässt sich über die Reduktion auch $A$ lösen.[^1]
- *Widerspruchsbeweis*: $H_0 \leq X\Rightarrow X$ ist unentscheidbar, denn falls ein Algorithmus mit $X$ existiert, dann muss $H_0$ auch lösbar sein…
^1660502381207

## Eigenschaften: #fc
- **Lemma**: Falls $A \leq B$ und $B$ [[Entscheidbarkeit|semi-/entscheidbar]] ist, dann ist auch $A$ semi-/entscheidbar:
	→ Da $\chi_B$ berechenbar ist, ist auch $\chi_B \circ f=\chi_B(f(\forall w\in\Sigma^{Stern}))=\chi_A(w)$ berechenbar
- $A \leq_p B \wedge B \in$ [[Komplexitättheorie/Zeitklassen/P|P]] $\Longrightarrow A\in\text{P}$
	→ Gleiches gilt für $B\in$ [[Komplexitättheorie/Zeitklassen/NP|NP]]
^1660502381215

## Varianten:
- $f$ ist in [[Komplexitättheorie/Zeitklassen/NP|Polynomialzeit]] berechenbar: $A\leq_p B$
- [[Komplexitättheorie/Logspace-Reduktion|Logspace-Reduktion]]: $A\leq^{\log}_m B$
	→ Falls $\leq_P$ und $\leq_{\log}$ übereinstimmen sollten, gilt $L=\text{P}$
