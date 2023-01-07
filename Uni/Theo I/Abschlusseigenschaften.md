---
tags: uni theo-1 theoretical-cs chomsky abstraction formal-languages
cards-deck: Uni::Courses::Theo-I
completed: true
aliases: Abschlusseigenschaften
linter-yaml-title-alias: Abschlusseigenschaften
date-of-creation: 2022-09-20
mod-date: 2022-09-22
---

# Abschlusseigenschaften

## Tabelle: #fc
|                                            | $\cup$       | $\cap$       | $\overline{L}$ | $L\cdot\hat{L}$ | $L^{Stern}$        | $(L\cap L'\in\text{REG})\in$ Klasse von $L$ |
| ------------------------------------------ | ------------ | ------------ | -------------- | --------------- | ------------ | ------------------------------------------- |
| [[Typ-3\|REG]]                             | $\checkmark$ | $\checkmark$ | $\checkmark$   | $\checkmark$    | $\checkmark$ |                                             |
| [[2. Typ - CFL/Deterministische Kellerautomaten\|DCFL]] | [^1]         |              | $\checkmark$   |                 |              | $\checkmark$                                |
| [[Typ-2\|CFL]]                             | $\checkmark$ |              |                | $\checkmark$    | $\checkmark$ | $\checkmark$                                |
| [[Typ-1\|CSL]]                             | $\checkmark$ | $\checkmark$ | $\checkmark$[^2]   | $\checkmark$    | $\checkmark$ |                                             |
| [[Typ-0]]                                  | $\checkmark$ | $\checkmark$ | [^3]               | $\checkmark$    | $\checkmark$ |                                             |
^1664630674386

[^1]: Es fehlt die [[Grammatik|Grammatik-Beschreibung]]
[^2]: [[../Theo II/Komplexitättheorie/Platzklassen/Satz von Immerman–Szelepcsényi|Satz Von Immerman–Szelepcsényi]], Details (die mich nicht interessieren) auf V.20 F.39.4 ff. und V.21 F.40.1 ff.
[^3]: Folgt aus dem [[../Theo II/Halteprobleme|Halteproblem]]
