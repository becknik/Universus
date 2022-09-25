---
tags: uni theo-1 theoretical-cs chomsky
cards-deck: Uni::Courses::Theo-I
complete: true
aliases:
  - ε-Sonderregel
  - Epsilon-Sonderregel
linter-yaml-title-alias: ε-Sonderregel
date: 2022-09-15
mod-date: 2022-09-21
---

# ε-Sonderregel

## Definition:
-> Für eine [[../Grammatik|formale Grammatik]] $G$ ist die Regel der Form $(u,\varepsilon)$ nur dann $\in P$ zugelassen, wenn $\forall p\in P_G,p=(u',v):u\notin u'$
	-> Die Regel muss *vom Startsymbol* $S$ *"aufgerufen"* und darf sonst von *keiner anderen Regel* "aufgerufen" werden
