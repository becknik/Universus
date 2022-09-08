---
tags: uni dsa practical-cs complexity maths
cards-deck: Uni::Courses::DSA
status: unfinished
aliases: Landau-Notationen
linter-yaml-title-alias: Landau-Notationen
date: 2022-07-21
mod-date: 2022-09-08
---

# Landau-Notationen

## Varianten: #fc
| Notation                 | Informelle Beschreibung                       | Formelle Beschreibung                                                                                   |                                             |
| ------------------------ | --------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| $f \in \mathbfcal{O}(g)$ | $f$ wächst nicht schneller als $g$            | $f(n) = \mathbfcal{O}(g(n))\Leftrightarrow\exists c,n_0, \forall n \geq n_0: f(n) \leq c\cdot g(n)$ | Asymptotische obere Schranke                |
| $f \in o(g)$             | $f$ wächst langsamer als $g$                  | $\exists C,x_0 > 0,\forall x > x_0:\|f(x)\| < C\cdot\|g(x)\|$                                             | Asymptotisch gegenüber $g$ vernachlässigbar |
| $f \in \Omega(g)$        | $f$ wächst nicht wesentlich langsamer als $g$ | $\exists c,x_0 > 0,\forall x > x_0: c\cdot\|g(x)\| \leq \|f(x)\|$                                          | Asymptotische untere Schranke               |
| $f \in \Theta(g)$        | $f$ wächst genauso schnell wie $g$            | $\exists c,C,x_0 > 0, \forall x > x_0: c\cdot\|g(x)\| \leq \|f(x)\| \leq C\cdot\|g(x)\|$                        | Asymptotisch scharfe Kante                  |
- $f \in \Theta(g): f \in \mathbfcal{O}(g) \wedge f \in \Omega(g)$
- $o(f) \subseteq \mathbfcal{O}(f)$
- $\Theta(f) = \mathbfcal{O}(f) \cap \Omega(f)$
^1650912605634

- [[O-Notation]]
- [Wikipedia](https://de.wikipedia.org/wiki/Landau-Symbole#Definition)(25.07.2022)
