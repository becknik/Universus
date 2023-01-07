---
tags: uni theo-1 theoretical-cs chomsky formal-languages
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Typ-2
  - Typ-2 Grammatik
  - Typ-2 Sprache
  - CFL
  - Context-Free Languages
  - kontextfreie Sprache
  - kontextfreie Grammatik
linter-yaml-title-alias: Typ-2
date-of-creation: 2022-09-15
mod-date: 2022-09-25
---

# Typ-2

## Definition: #fc
- Eine [[Grammatik|Grammatik]] $G$, die die Kriterien für den Grammatik [[Typ-1]] und $$\forall(u,v)\in P\text{ mit }u\in V(\text{also }|u|=1)\text{ und }|v|\geq1$$ erfüllt, gehört dem 2. Typ der [[Chomsky-Hierarchie]] an
^1664630497663

## Eigenschaften: #fc
- Beschreiben unter anderem [[2. Typ - CFL/Korrekte Klammerausdrücke|Dyck-Wörter/ korrekte Klammerausdrücke]]
- Zu jeder Typ-2 Grammatik existiert eine äquivalente [[2. Typ - CFL/Chomsky-Normalform|CNF]] und [[2. Typ - CFL/Greibach-Normalform|GNF]]
- Alle Typ-2 Sprachen über $|\Sigma|=1$ sind bereits [[Typ-3|regulär]]
- [[2. Typ - CFL/Pumping Lemma für Typ-2|Pumping Lemma für Typ-2]]
- Für jede Typ-2 Grammatik $G~\exists$ [[2. Typ - CFL/Kellerautomat|PDA]] $M$ mit $L(G)=N(M)$
	→ $O.B.d.A:\{L\mid \varepsilon\notin L\}$ (V.19 F.37.1)
- [[2. Typ - CFL/Deterministische Kellerautomaten|DPDA]] $\Rightarrow\text{DCFL}\subsetneq\text{CFL}$
- Das [[Wortproblem|Wortproblem]] für Typ-2 lässt sich effizient durch den [[2. Typ - CFL/CYK-Algorithmus|CYK-Algorithmus]] entscheiden
^1664630497671

## Modelle: #fc
- [[2. Typ - CFL/Syntaxbäume|Syntaxbäume]]
- [[2. Typ - CFL/Backus-Naur-Form|Backus-Naur-Form]]
- [[2. Typ - CFL/Chomsky-Normalform|Chomsky-Normalform]]
- [[2. Typ - CFL/Greibach-Normalform|Greibach-Normalform]]
- [[2. Typ - CFL/Kellerautomat|Kellerautomat]]
^1664630497674

## Theoreme:
- [[2. Typ - CFL/Pumping Lemma für Typ-2|Pumping Lemma für Typ-2]]
> *Hier bin ich mir nicht sicher, ob das Typ-2 Pumping Lemma genauso wie das [[3. Typ - REG/Pumping Lemma für Typ-3|Pumping Lemma für Typ-3]] "leckt" und mehr Sprachen akzeptiert als CFL umfasst…*
- [[2. Typ - CFL/Chomsky-Normalform|Satz für die CNF]]
