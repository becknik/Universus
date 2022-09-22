---
tags: uni theo-1 theoretical-cs
cards-deck: Uni::Courses::Theo-I
complete: true
aliases:
  - Backus-Naur-Form
  - BNF
linter-yaml-title-alias: Backus-Naur-Form
date: 2022-09-03
mod-date: 2022-09-15
---

# Backus-Naur-Form

## Definition

### Syntax:
-> Die Produktionsregel-Menge $P$ einer [[../Grundlegendes/Grammatik|formale Grammatik]] in anderem Syntax:
- *Nicht-Terminale*: $\langle\text{linkeSeite}\rangle ::= \langle\text{NichtTerminal}_1\rangle\mid\langle\text{NichtTerminal}_2\rangle\mid\dots\mid\langle\text{NichtTerminal}_n\rangle$
- *Terminalsymbole*: $\langle \text{Ziffer}\rangle ::= 1|2|3|4|5|6|7|8|9|0$
- *Bedingungen*: $\langle\text{auswahl}\rangle ::=\text{ falls }\langle\text{bedingung}\rangle\text{ dann }\langle\text{block}\rangle$

### Theo-Syntax:
- Der *obsolete* Theo-Style: $A::=\beta_1\mid\dots\mid\beta_n$ für $\{(A,\beta_1),(A,\beta_n)\}\subseteq P$
	-> Anstelle vom missglückten Klon-Walross-Operator $::=$ wird $\rightarrow$ verwendet
- *Erweiterte BNF*:
	- $A::=\alpha[\beta]\gamma$ für $A::=\alpha\gamma$ und $A::=\alpha\beta\gamma$ oder im [[../../DSA/Text/Reguläre Audrücke|RegEx Syntax]]: $\alpha\beta?\gamma$ 
	- $A::=\alpha\{\beta\}\gamma$ für $\alpha\beta^*\gamma$ (im *RegEx Syntax*)

## Eigenschaften:
- Bildet (auch in der nicht erweiterten Form) die Sprachklasse [[../Typ-2|CFL]] ab
- Wird insbesondere zur Festlegung der Syntax von Programmiersprachen verwendet[^1]
- Es existieren Erweiterungen wie die *EBNF* mit Elementen aus [[../../DSA/Text/Reguläre Audrücke|Reguläre Ausdrücken]] oder die *ABNF* für Syntaxdefinitionen in Internetnormen[^1]

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021.
