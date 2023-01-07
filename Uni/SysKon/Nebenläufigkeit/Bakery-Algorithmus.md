---
tags: uni practical-cs syskon sync correctness
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Bakery-Algorithmus
linter-yaml-title-alias: Bakery-Algorithmus
date-of-creation: 2022-12-03
mod-date: 2023-01-03
---

# Bakery-Algorithmus
“I don't know how many people realize how remarkable this algorithm is.”
“When I showed him \[Anatol Holt\] the algorithm and its proof and pointed out its amazing property, he was shocked.”
“For a couple of years after my discovery of the bakery algorithm, everything I learned about concurrency came from studying it.”

## Annahmen #fc
- [[../Atomizität|Atomizität]] im Schreiben auf gemeinsame primitive Variablen
- [[../Synchronisation/Sequenzielle Konsistenz|Sequenzielle Konsistenz]] bei Speicherzugriffen
- [[../Korrektheitskriterien|Schwach faires]] [[../Betriebssystem/Scheduling|Scheduling]]
^1670104818394

## Algorithmus #fc
```
const int number[]{};
---
Procedure p_i:
loop:
	<Nicht kritischer Abschnitt>
	choosing[i] ← 1;
	number[i] ← 1 + max(number);
	choosing[i] ← 0;
	forall 𝑗 ∈ {0, …, n-1} mit j ≠ i do
		await (choosing[j] == 0)
		await ( (number[j] == 0) || ((number[j],j) >> (number[i])) )
	<Kritischer Abschnitt>
	number[i] ← 0
```
- Wenn `number[i] ← 1 + max(number);` nicht atomar ausgeführt wird, ist $p_i\neq p_j:number[i]=number[j]$ (nur *monoton-steigende* Folge) möglich
	→ Totale Ordnung (*strenge Monotonie*) durch Zuweisung nach Thread-ID des [[../OS|OSes]] aus dem TCB
^1670083636222
