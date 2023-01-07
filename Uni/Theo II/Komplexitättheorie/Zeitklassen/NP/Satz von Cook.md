---
tags: uni theo-2 theoretical-cs complexity solvability
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Satz von Cook
linter-yaml-title-alias: Satz von Cook
date-of-creation: 2022-07-10
mod-date: 2022-10-24
---

# Satz von Cook

## Eigenschaften:
- Beweist die [[NP-Vollständigkeit|NP-Vollständigkeit]] von [[../../Probleme/Satisfiability|SAT]]
- Wurde zeitgleich von Levin bewiesen

## Beweis $SAT\in NP$:
- Sei $F$ eine Formel mit den Variablen $x_1,\dots,x_n$.
- [[NP/Guess and Check|Guess And Check-Algorithmus]]:
```
FOR i := 1 TO n DO
	Rate nichtdeterministisch x_i := TRUE/FALSE
ENDFOR;
IF A(F(x_1,\dots,x_n))=1 THEN ACCEPT ELSE REJECT ENDIF
```
→ $F\in SAT$ genau dann, wenn es eine nichtdeterministische Rechnung gibt, durch die $F=1$ gilt
→ Außerdem ist die nichtdeterminitische Rechnung $i\leq|F|$, die Rechenzeit durch eine TM also polynomial beschränkt

## Beweis [[NP-Härte|NP-Härte]] Von $SAT$:
- Sei $L \in NP$ beliebig
	→ $\exists$ [[../../../../Theo I/Turingmaschinen|nichtdeterministische TM]] $M$, die L akzeptiert und $\exists$ Polynom $p$, das die Laufzeit von $M$ beschränkt
- Da $M$ normiert ist: Definiere $M$ als Halbband-TM mit $E=\{z_a\},\forall\gamma\in\Gamma:$$\delta(z_a,\gamma\in\Gamma)=\{(z_a,\gamma,N)\}$
- Sei die Eingabe für $M~x = x_1,\dots,x_n\in\Sigma^{Stern}$.
- Gesucht: $x\in L\Leftrightarrow F\in SAT$
- $F = R \wedge A \wedge Ü_1 \wedge Ü_2 \wedge E, F$
→ (F25.4ff. oder S.152f.)
