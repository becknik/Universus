---
tags: uni practical-cs syskon sync correctness
cards-deck: Uni::Courses::SysKon
complete: true
aliases: Bakery-Algorithmus
linter-yaml-title-alias: Bakery-Algorithmus
date: 2022-12-03
mod-date: 2022-12-03
---

# Bakery-Algorithmus
“I don't know how many people realize how remarkable this algorithm is.”
“When I showed him \[Anatol Holt\] the algorithm and its proof and pointed out its amazing property, he was shocked.”
“For a couple of years after my discovery of the bakery algorithm, everything I learned about concurrency came from studying it.”

## Annahmen: #fc
- Kommunikation über gemeinsame Variablen im RAM
- [[Atomizität]] bei Schreibe- und Leseoperationen
- [[../Sequenzielle Konsistenz|Sequenzielle Konsistenz]] beim Speicherzugriff
- Ein [[../Korrektheitskriterien|schwach fairer]] Scheduler
^1670104818394

## Algorithmus: #fc
```
	int[] number = int[n]
Procedure p_i:
loop:
	<Nicht kritischer Abschnitt>
	choosing[i] ← true;
	number[i] ← 1 + max(number);
	choosing[i] ← false;
	forall 𝑗 ∈ {0, …, n-1} mit j ≠ i do
		await (choosing[j] = false)
		await ((number[j] = 0) or number[j] > number[i])
	<Kritischer Abschnitt>
	number[i] ← 0
```
- Wenn `number[i] ← 1 + max(number);` nicht atomar ausgeführt wird, ist $p_i\neq p_j:number[i]=number[j]$ (nur *monoton-steigende* Folge) möglich
	-> Totale Ordnung (*strenge Monotonie*) durch Zuweisung nach Thread-ID des [[../OS|OSes]] aus dem TCB
^1670083636222
