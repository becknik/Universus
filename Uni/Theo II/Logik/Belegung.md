---
tags: uni theo-2 theoretical-cs logic 
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Belegung
  - passend
  - Modell
  - erfüllbar
  - gültig
  - semqntisch Äquivalent
date-of-creation: 2022-08-05
mod-date: 2022-08-13
linter-yaml-title-alias: Belegung
---

# Belegung
→ [[Aussagenlogik|Aussagenlogik]]
→ [[Schöning's Spiegelungsprinzip|Spiegelungsprinzip]]

## Definition: #fc
- Belegung/ Assignment: $\mathcal{A}:D \rightarrow \{0,1\}, D \subseteq \{A_1,A_2,\dots\}$
	→ Durch eine Belegung erhält jede *atomare Formel* einen Wert
- $\mathcal{A}(F \wedge G) =$ Minimum von $F$ und $G$
- $\mathcal{A}(F \vee G) =$ Maximum von $F$ und $G$
- $\mathcal{A}(\neg F) = 1 - \mathcal{A}(F)$
^1661245562239

## Fachbegriffe: #fc
- Eine Belegung $\mathcal{A}$ ist **passend** zu einer Formel $F$:
	→ Alle in der $F$ vorkommenden $A_i \in D \text{ mit } \mathcal{A}: D \rightarrow \{0,1\}$
- Eine Belegung ist **Modell** für eine Formel $F$:
	→ $\mathcal{A}$ ist *passend* zu $F \wedge \mathcal{A}(F) = 1$
- Eine Formel $F$ ist **erfüllbar**:
	→ $\exists$ ein Modell für $F$
- $F$ ist eine *Tautologie* genau dann, wenn $F$ **gültig** ist:
	→ Gültigkeit: $\forall \mathcal{A}$, die zu $F$ passend sind gilt: $\mathcal{A}(F)=1$
- Zwei Formalen $F,G$ sind **semantische Äquivalent**:
	→ $\forall \text{ passenden } \mathcal{A}: \mathcal{A}(F)=\mathcal{A}(G) \Leftrightarrow F \equiv/\triangleq G$
→ Kleine Formeln lassen sich durch Wahrheitstafeln auf die genannten Eigenschaften in [[../Komplexitättheorie/Zeitklassen/EXPTIME|EXPTIME]] testen
^1661245562245
