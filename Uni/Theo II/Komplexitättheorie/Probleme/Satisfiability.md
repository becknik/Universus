---
tags: uni theo-2 theoretical-cs decision-problem
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Satisfiability
  - SAT
date-of-creation: 2022-07-09
mod-date: 2022-08-13
linter-yaml-title-alias: Satisfiability
---

# Satisfiability

## Definition:
- Das Erfüllbarkeitsproblem der [[../../Logik/Aussagenlogik|Aussagenlogik]]
$$SAT:=\{w \in\text{festen }\Sigma\mid w\text{ kodiert eine erfüllbare Formel }F\}$$
- Oder: $SAT=\{F\mid F\text{ ist erfüllbare Formel}\}$
	→ In der angegebenen Formel ist $SAT$ ein *Entscheidungsproblem*
→ [[../Zeitklassen/NP/Satz von Cook|Satz von Cook]]

### Eigenschaften:
- $SAT\in$ [[../Zeitklassen/NP|NP]] ("einfach zu sehen")
- [[../Zeitklassen/NP/Satz von Cook|Satz Von Cook]]: $SAT$ ist [[../Zeitklassen/NP/NP-Vollständigkeit|NP-vollständig]]
- Die bekannten deterministischen $SAT$-Algorithmen haben die Komplexität von $2^{\mathcal{O}(n)}$, also kann jede $L\in NP$ durch $2^{p(n)}$ mit geeigneten $p$ abgeschätzt werden
	→ $NP\subseteq\bigcup_{\text{Polynom }p}TIME(2^{p(n)})$ ([[../Zeitklassen/EXPTIME|EXPTIME]])
