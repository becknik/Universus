---
tags: uni dsa practical-cs design-pattern
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Divide And Conquer
  - Divide & Conquer
  - D&C
linter-yaml-title-alias: Divide And Conquer
date-of-creation: 2022-07-19
mod-date: 2022-09-06
---

# Divide And Conquer

## Prinzip: #fc
- Das Problem wird *rekursiv* auf ein *identisches, separat berechenbares* Problem mit *kleinerer Eingabemenge* zurückgeführt
	→ "*Rekursive Rückführung*"
- Die resultierenden atomaren Teilprobleme werden gelöst und die entstandenen Teillösungen dann zu einer Gesamtlösung zusammengesetzt
	→ Jedes *Teilproblem soll von der selben Natur* wie das vorher Zerlegte sein, so dass es sich durch denselben Algorithmus lösen lässt
^1658258681785

## Algorithmus:
```
Method: D&C (P: problem)
…
if [P klein] then
	[explizite Lösung]
else 
	[Teile P auf in P_1, …, P_k];
	D&C (P_1);
	…;
	D&C (P_k);
	[Setze Lösung für P aus Lösungen für P_1, …, P_k zusammen]
fi
```

## Anwendung: #fc
- [[../Suche/Binäre Suche|Binäre Suche]]
- [[../Sortieren/QuickSort|QuickSort]], [[../Sortieren/MergeSort|MergeSort]]
- Spielpläne für Turniere (VL.22 F.40)
- Strassen-Algorithmus zur Matritzenmultiplikation
^1658939015229
