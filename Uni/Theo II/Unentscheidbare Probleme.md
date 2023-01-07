---
tags: uni theo-2 theoretical-cs abstraction computability
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Unentscheidbare Probleme
  - Unentscheidbare Gammatik-Probleme
linter-yaml-title-alias: Unentscheidbare Probleme
date-of-creation: 2022-08-13
mod-date: 2022-09-10
---

# Unentscheidbare Probleme

## Für zwei deterministisch kontextfreie Grammatik $G_1,G_2$:
→ [[../Theo I/2. Typ - CFL/Deterministische Kellerautomaten|DCFL]] $\subsetneq$ [[../Theo I/Typ-2|Typ-2]]
- Seien $L_1=L(G_1),L_2=L(G_2)$
1. *Leerheit des Schnitts*: $L_1 \cap L_2 = \emptyset?$
2. *Endlichkeit des Schnitts*: $|L_1\cap L_2|<\infty?$
3. *Kontextfreiheit des Schnitts*: $\exists G\in\text{CFL}$ mit $L(G) = L_1 \cap L_2?$
4. *Inklusion*: $L_1 \subseteq L_2?$
5. (*Äquivalenz*: $L_1 = L_2?$)
	 → Für $G_1,G_2\in\text{DCFL}$ ist diese Äquivalenz [[Entscheidbarkeit|entscheidbar]]
	→ *Beweis*: $\text{PCP}_{\{0,1\}}\leq$ Nicht-Leerheit des Schnitts (F.18.5 ff.)

## Für eine kontextfreie Grammatik $G$:
→ [[../Theo I/Typ-2|Typ-2]]
1. Ist $G$ *mehrdeutig*?
2. Ist $\overline{L(G)}$ *kontextfrei*?
3. Ist $L(G)/\overline{L(G)}\in\text{REG}?$
- *Folgerung*: Sei $G\in\text{CFL}$, $L$ eine [[../Theo I/Typ-3|reguläre Sprache]]. "Gilt $L(G) = L?$" ist unentscheidbar
	→ Das "Mischen" von Sprachen ist unentscheidbar
4. Ist $L(G)/\overline{L(G)}\in\text{DCFL}?$

## Mit einer kontextsensitiven Grammatik $G$:
→ [[../Theo I/Typ-1|Typ-1]]
1. *Leerheit*: $L(G)=\emptyset?$
2. *Endlichkeit*: $|L(G)|<\infty?$

## Weitere unentscheidbare Probleme:
- Die [[Halteprobleme]]
- Der [[Entscheidbarkeit/Satz von Rice|Satz Von Rice]]
- [[Komplexitättheorie/Probleme/Postsches Korrespodenzproblem|PCP]] über dem Alphabet $|\Sigma|\geq2$
- Der [[Berechenbarkeit/Gödelscher Unvollständigkeitssatz|Gödelsche Unvollständigkeitssatz]]
