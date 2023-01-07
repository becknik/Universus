---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - 3KNF-SAT
  - 2KNF-SAT
date-of-creation: 2022-07-10
mod-date: 2022-08-11
linter-yaml-title-alias: 3KNF-SAT
---

# 3KNF-SAT

## Definition:
- *Gegeben*: Eine Formel $F$ in [[../../Logik/Normalformen|KNF]] mit maximal 3 Literalen pro Klausel
- *Gesucht*: Ist $F$ erfüllbar?

## Beweis Der [[../Zeitklassen/NP/NP-Härte|NP-Härte]]:
- Zu zeigen: [[Satisfiability|SAT]] $\leq_p \text{3KNF-SAT}$
- Ansatz: Umformung einer $SAT$-Formel in eine [[../../Logik/Belegung|erfüllbarkeits]]äquivalente $3KNF$-Formel über die Darstellung der [[../../Logik/Aussagenlogik|aussagenlogischen]] Teilformeln in einem Baum
1. Schiebe Negationen mit de Morgan zu den Blättern
2. Neue Variablen $(y_0,y_1,\dots)$ werden für jeden inneren Knoten (die nur noch aus Verknüpfungen bestehen) erzeugt
	→ $y_0$ für die Wurzel
3. Für jeden inneren Knoten $y_i$ wird eine 3KNF-Teilform $G_i$ mit den Nachfolgeknoten $y_j$ und $y_k$erstellt
	- Falls $y_i\Leftrightarrow y_j\wedge y_k:~$$G_i=(y_j \vee y_k \vee \neg y_i) \wedge (\neg y_j \vee y_k \vee \neg y_i )$$~\wedge (y_j \vee \neg y_k \vee \neg y_i) \wedge (\neg y_j \vee \neg y_k \vee y_i )$
	- Falls $y_i\Leftrightarrow y_j\vee y_k:~$$G_i=(y_j \vee y_k \vee \neg y_i) \wedge (\neg y_j \vee y_k \vee y_i)$$~\wedge (y_j \vee \neg y_k \vee y_i) \wedge (\neg y_j \vee \neg y_k \vee y_i)$
4. Für die inneren Knoten $y_0,y_1,\dots,y_r$ betrachten wir die Formel $H = G_0 \wedge G_2, \wedge \dots \wedge G_r$.
	→ $F'= H \wedge y_0$ ist eine Formel in 3KNF-Form, die genau dann eine erfüllende Belegung hat, wenn $F$ erfüllbar ist
- $\text{2KNF-SAT}\in P,$ da man die Klauseln in Schritt *3* weiter verkürzen kann
