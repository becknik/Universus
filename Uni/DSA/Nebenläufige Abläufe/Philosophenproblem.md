---
tags: uni dsa practical-cs parallel problem
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Philosophen-Problem
  - Philosophenproblem
linter-yaml-title-alias: Philosophen-Problem
date-of-creation: 2022-07-05
mod-date: 2022-09-10
---

# Philosophen-Problem
![2022-07-05|150](https://upload.wikimedia.org/wikipedia/commons/7/7b/An_illustration_of_the_dining_philosophers_problem.png)

## Definition: #fc
"Fünf Philosophen, von 0 bis 5 durchnummeriert, leben in einem Haus, in dem der Tisch für sie gedeckt ist. Jeder Philosoph hat einen Platz am Tisch. Ihr einziges Problem - neben denen philosophischer Natur - besteht darin, dass eine sehr schwierige Art von Spaghetti (\*oder ein anderes nicht so einfach zu portionierendes Gericht) zur Mahlzeit bereitsteht, zu deren Verzehr man zwei Gabeln benötigt. Neben jedem Teller liegen jedoch nur zwei Gabeln bereicht, weshalb zwei Nachbarn nicht zur selben Zeit essen können."
~ *Edsger W. Dijkstra*, Hierarchical ordering of sequential processes, 1971
- Jeder Philosoph durchläuft einen Zyklus von Zuständen: denken → hungrig → essen → denken …
- Da die Philosophen die Gabeln nicht gleichzeitig aufnehmen können, kann ein *Deadlock* enstehen, da jeder Philosoph nur die rechte Gabel aufgenommen hat
	→ Gabeln können allerdings erst nach dem Essen zurückgegeben werden
→ Philosophen verhungern
^1658939296953

## Anwendung:
- Atomic-Instruktionen in [[RISC-V]]/anderen [[../../Ro I/CPU/Befehlssatz Architektur|ISAs]]
- Nebenläufige Abläufe in Programmen
→ Darstellung als [[Petri-Netze|Petri-Netze]]

## Algorithmen:
```
repeat
	denken;
	hungrig werden;
	nimm Gabel i;
	nimm Gabel (i + 1) % 5;
	essen;
	lege Gabel i zurück;
	lege Gabel (i + 1) % 5 zurück;
until false
```
```
repeat
	denken;
	hungrig werden;
	down(g_i);
	down(g_{(i + 1) % 5});
	essen;
	up(g_i);
	up(g_{(i + 1) % 5});
until false
```
→ Deadlocks sind möglich - für Deadlock-freie Lösung: (DSA VL20)
