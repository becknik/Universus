---
tags: uni theo-1 theoretical-cs
cards-deck: Uni::Courses::Theo-I
completed: true
aliases: Reguläre Ausdrücke
linter-yaml-title-alias: Reguläre Ausdrücke
date-of-creation: 2022-09-20
mod-date: 2022-09-23
---

# Reguläre Ausdrücke
→ Für mehr Praxisbezug: [[../../DSA/Text/Reguläre Audrücke|DSA/.../RegEx]]

## Definition

### Syntax: #fc
- $\emptyset$ und $\varepsilon$ sind reguläre Ausdrücke
- $\forall a\in \Sigma$ ist $a$ ein regulärer Ausdruck
- Falls $\alpha$ und $\beta$ reguläre Ausdrücke sind, dann auch $\alpha\beta,(\alpha|\beta)$ und $(\alpha)^{Stern}$
^1664630989836

### Semantik: #fc
→ Die Zuordnung von jedem RegEx $\gamma$ zur Sprache $L(\gamma)\subseteq\Sigma^{Stern}$
- $L(\emptyset)=\emptyset,L(\varepsilon)=\varepsilon$
- $\forall a\in\Sigma:L(a)=\{a\}$
- $L(\alpha\beta)=L(\alpha)L(\beta),~L((\alpha|\beta))=L(\alpha)\cup L(\beta),~L((\alpha)^{Stern})=L(\alpha)^{Stern}$
^1664630989842

## Eigenschaften:
- Reguläre Ausdrücke sind ein weiteres Beschreibungsmittel für [[../Typ-3|reguläre Sprachen]]
	→ [[Satz von Kleene]]
