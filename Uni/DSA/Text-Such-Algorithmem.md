---
tags: uni dsa practical-cs algorithm text abstraction
cards-deck: Uni::Courses::DSA
completed: true
aliases: Text-Such-Algorithmen
linter-yaml-title-alias: Text-Such-Algorithmen
date-of-creation: 2022-07-26
mod-date: 2022-09-08
---

# Text-Such-Algorithmen
→ [[Text/Reguläre Audrücke|Reguläre Ausdrücke]]

## Vergleich #fc
| Algorithmus                                                             | Durchschnittliche Laufzeitkomplexität                               | Verwendete Informationen                 |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------- | ---------------------------------------- |
| [[Algorithmen/Muster/Brute Force\|Brute Force]]                         | $\Theta((n-m+1)*m)$                                       | -                                        |
| [[Algorithmen/Text/Knuth-Morris-Pratt\|Knuth-Morris-Pratt Algorithmus]] | $\mathbfcal{O}(n+m)$                                                | Positive Informationen                   |
| [[Algorithmen/Text/Boyer-Moore\|Boyer-Moore Algorithmus]]               | $\Theta(m)$ (=Verarbeitung) + $\Omega(\frac{n}{m})$ (=Matching)[^1] | negative, positive & Zusatzinformationen |
→ Boyer-Moore: Wenn $p$ nicht im Text vorkommt: $\mathbfcal{O}(n+m)$, sonst $\mathbfcal{O}(nm)\Rightarrow$ trotzdem lineare Laufzeit[^2]
^1658939379533
[^1]:[Wikipedia: Boyer-Moore](https://en.wikipedia.org/wiki/Boyer%E2%80%93Moore_string-search_algorithm)
[^2]:[Wikipedia: Boyer-Moore Performance](https://en.wikipedia.org/wiki/Boyer%E2%80%93Moore_string-search_algorithm#Performance)
