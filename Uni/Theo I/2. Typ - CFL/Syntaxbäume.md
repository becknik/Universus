---
tags: uni theo-1 theoretical-cs tree formal-languages
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Syntaxbäume
  - inheränt Mehrdeutig
linter-yaml-title-alias: Syntaxbäume
date-of-creation: 2022-09-15
mod-date: 2022-09-20
---

# Syntaxbäume

## Definition: #fc
- Eine Variante zur Darstellung einer *wesentlichen Ableitung* von [[../Typ-2|Typ-2-Grammatiken]]
- Sei $G=(V,\Sigma,P,S)$ eine [[../Grammatik|Grammatik]] und die zugehörige *Ableitung* $S\Rightarrow y\Rightarrow y'\dots\Rightarrow w\in\Sigma^{Stern}$ und $y=x_1x_2\dots x_r$ die durch die [[../Grammatik|Übergangsrelation]] von $S$ entstandene Satzform, dann ist $S$ der *Wurzelknoten des Syntaxbaumes* mit $r$ *direkten Nachkommenknoten* $x_1$ bis $x_r$
	→ Wenn $x_i\in\Sigma$ ist, dann ist $x_i$ ein Blattknoten des Baumes
	→ Wenn $x_i\in V$ ist, dann ist $x_i$ ein innerer Knoten des Baumes, welcher wiederum einen Teilbaum trägt und daher so wie oben für $x_i$ anstelle von $S$ definiert ist
^1664631318311

## Linksableitung: #fc
- Damit es für eine Ableitung nicht zu *unterschiedlichen Syntaxbäumen* kommt, kann man die Ableitungs-Reihenfolge festlegen
	→ Im Fall der *Linksableitung* wird die am weitesten links stehende Variable $\in V$ *als erstes* abgeleitet
	→ Die Zuordnung *Syntaxbaum* $\leftrightarrow$ *Linksableitung* ist eine 1:1 Entsprechung
- $x\in\Sigma^{Stern}$ ist genau dann $\in L(G)$, wenn eine Linksableitung für $x$ existiert
^1664631318351

## Mehrdeutigkeit: #fc
- *Mehrdeutige Grammatik*: $\exists w\in L(G):$ für $w$ gibt es zwei Syntaxbäume
- *Eindeutige Grammatik*: $\forall w\in L(G):\exists$ nur eine einzige Linksableitung (also auch nur einen Syntaxbaum)
- *Mehrdeutige Sprache*: $\hat{G}:=\{G\mid L(G)=L\}:\forall G\in \hat{G}$ ist $G$ *(inhärent) mehrdeutig*
	→ Ein Beweis für *inhärente Mehrdeutigkeit* einer Sprache ist schwierig und *im Allgemeinen unmöglich*
	→ Beispiel: $L=\{a^ib^jc^k\mid i=j\vee j=k\}$
^1664631318354

## Eigenschaften: #fc
- Bei beliebigen [[../Typ-2|Typ-2-Grammatiken]] kann es zu unübersichtlichen, "verzweigten" Ableitungsbäumen kommen
	→ Durch die Umwandlung der Grammatik in [[Chomsky-Normalform]] ist dem nicht mehr so
^1664631318356
