---
tags: uni theo-1 theoretical-cs chomsky formal-languages decision-problem abstraction
cards-deck: Uni::Courses::Theo-I
completed: true
aliases: Entscheidbarkeitsprobleme für Sprachklassen
linter-yaml-title-alias: Entscheidbarkeitsprobleme für Sprachklassen
date-of-creation: 2022-09-20
mod-date: 2022-10-02
---

# Entscheidbarkeitsprobleme für Sprachklassen

## Tabelle: #fc
|                                                               | Wortproblem      | Leerheit         | Endlichkeit      | Äquivalenz       | Schnitt          |
| ------------------------------------------------------------- | ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
| [[Typ-3\|Typ-3/REG]]                                          | $\checkmark$[^1] | $\checkmark$[^2] | $\checkmark$[^3] | $\checkmark$[^4] | $\checkmark$[^5] |
| [[2. Typ - CFL/Deterministische Kellerautomaten\|DCFL]]       | "                | "                | "                | $\checkmark$[^9] | $\times$         |
| [[Typ-2\|Typ-2/CFL]]                                          | $\checkmark$[^6] | $\checkmark$[^7] | $\checkmark$[^8] | $\times$         | $\times$         |
| [[Typ-1\|Typ-1/CSL]]                                          | $\checkmark$[^0] | $\times$         | $\times$         | $\times$         | $\times$         |
| [[../Theo II/Entscheidbarkeit/Rekursiv Aufzählbar\|Typ-0/RE]] | $\times$         | $\times$         | $\times$         | $\times$         | $\times$         |
^1664630660487

[^0]: Direkt zu beginn der Vorlesung ([[Typ-1|hier]])
[^1]: Dank [[3. Typ - REG/Deterministischer Endlicher Automat\|DFAs]] in Echtzeit möglich
[^2]: Prüfe Erreichbarkeit im [[../DSA/Graphen|Graphen]] des DFAs, oder [[3. Typ - REG/Pumping Lemma für Typ-3|Pumping Lemma für Typ-3]]
[^3]: Suche ein erreichbaren Zyklus im Graphen des DFAs, von dem aus ein Endzustand erreichbar ist
[^4]: Durch [[Abschlusseigenschaften]] ist L_1 ∩ L_2 = ∅ entscheidbar
[^5]: L_1 = L_2 ⇔ (L_1 ∩ kompl(L_2)) ∪ (kompl(L_1) ∩ L_2) oder Isomorphie im [[3. Typ - REG/Minimalautomat|Minimalautomat]]
[^6]: [[2. Typ - CFL/CYK-Algorithmus|CYK-Algorithmus]], wenn $G$ in [[2. Typ - CFL/Chomsky-Normalform|CNF]] vorliegt
[^7]: [[2. Typ - CFL/Pumping Lemma für Typ-2|Pumping Lemma für Typ-2]], oder ein Markierungsalgorithmus mit produktiven Variablen
[^8]: [[2. Typ - CFL/Pumping Lemma für Typ-2|Pumping Lemma für Typ-2]]
[^9]: Géraud Sénizergues - seit 20 Jahren beweisen und gefeiert, trotzdem existiert noch kein einfacher Beweis…

### Markierungsalgorithmus mit produktiven Variablen:
1. Markiere $\{A\in V\mid(A,w\in\Sigma^{Stern})\in P\}$
2. Wiederhole, solange Markierungen hinzukommen:
	- Markiere $\{A\in V\mid(A,\beta\in (\text{markiert}(V)\cup\Sigma)^{Stern})\in P$
3. Gebe $LEER$ aus, wenn $S$ nicht markiert ist

### Gleichheit mit $L\in$ [[Typ-3|REG]]:
- *Gegeben*: $L\in$ [[2. Typ - CFL/Deterministische Kellerautomaten|DCFL]], $L'\in\text{REG}$
- *Frage*: $L=L'?$
→ Umformung: $L=L'\Leftrightarrow L\subseteq L'\vee L'\subseteq L\Leftrightarrow L\cap\overline{L'}=\emptyset\wedge L'\cap\overline{L}=\emptyset$
