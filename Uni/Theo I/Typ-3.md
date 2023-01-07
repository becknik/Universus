---
tags: uni theo-1 theoretical-cs chomsky formal-languages
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Typ-3
  - Typ-3 Grammatik
  - Typ-3 Sprache
  - REG
  - reguläre Sprache
  - reguläre Grammaik
linter-yaml-title-alias: Typ-3
date-of-creation: 2022-09-15
mod-date: 2022-09-20
---

# Typ-3

## Definition:

## Definition: #fc
- Eine [[Grammatik|formale Grammatik]] $G$, die die Kriterien für den Grammatik [[Typ-2]] erfüllt und für die $$\forall(u,v)\in P:v\in \Sigma\cup\Sigma V$$ erfüllt ist, gehört dem 3. Typ der [[Chomsky-Hierarchie]] an
	→ Die von der Grammatik erzeugte [[Formale Sprachen|formale Sprache]] liegt in der dazugehörigen Sprachklasse
^1664630493774

## Eigenschaften: #fc
- [[Syntaxbäume]] von Typ-3 Grammatiken sind nutzlos
	→ Typ-3-Sprachen sind nicht *inhärent mehrdeutig*, da $\forall L\in \text{Typ-3 }\exists$ [[3. Typ - REG/Deterministischer Endlicher Automat|DFA]] $M$, den man in eine eindeutige Grammatik umwandeln kann
- Jede Typ-3-Sprache kann durch einen [[3. Typ - REG/Nichtdeterministischer Endlicher Automat|NFA]] beschrieben werden
	→ $O.B.d.A:\{L\mid \varepsilon\notin L\}$ (V.19 F.37.1)
	→ Beweis: Typ-3 → NFA
	→ [[3. Typ - REG/Deterministischer Endlicher Automat|DFA]] = [[3. Typ - REG/Nichtdeterministischer Endlicher Automat|NFA]] = [[Typ-3|REG]] = Typ-3 (bezogen auf *Sprachklassen*)
- Reguläre Sprachen haben eine große Bedeutung (in der Informatik)
	→ [[3. Typ - REG/Reguläre Ausdrücke|Reguläre Ausdrücke]], [[../DSA/Nebenläufige Abläufe/Petri-Netze|Petri-Netze]], …
- $\forall L\in\text{REG}:$ Das [[3. Typ - REG/Syntaktisches Monoid|Syntaktisches Monoid]] von $L$ ist endlich und $L$ ist durch ein *endliches* [[Monoid|Monoid erkennbar]]
^1664630493778

## Modelle:
- [[3. Typ - REG/Deterministischer Endlicher Automat|DFAs]]/ [[3. Typ - REG/Nichtdeterministischer Endlicher Automat|NFAs]]
- [[3. Typ - REG/Reguläre Ausdrücke|Reguläre Ausdrücke]]

## Theoreme: #fc
- [[3. Typ - REG/Satz von Rabin und Scott|Satz von Rabin und Scott]]
- [[3. Typ - REG/Satz von Kleene|Satz von Kleene]]
- ([[3. Typ - REG/Pumping Lemma für Typ-3|Pumping Lemma für Typ-3]])
- [[3. Typ - REG/Myhill-Nerode|Myhill-Nerode Äquivalenz]]
^1666084274747
