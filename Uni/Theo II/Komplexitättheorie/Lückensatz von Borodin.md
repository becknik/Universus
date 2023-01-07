---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Lückensatz von Borodin
linter-yaml-title-alias: Lückensatz von Borodin
date-of-creation: 2022-08-12
mod-date: 2022-10-24
---

# Lückensatz von Borodin

## Definition: #fc
- Sei $r$ eine totale, [[Berechenbarkeit|berechenbare]] Funktion mit $\forall n:n\leq r(n)$
- Es $\exists$ effektiv eine totale, monotone Funktion $s:\mathbb{N}\rightarrow\mathbb{N}$ mit $n+1\leq s(n)$, so dass $$(D|N)(TIME|SPACE)(s)=(D|N)(TIME|SPACE)(r\circ s)$$ gilt
	→ *effektiv*: Aus der gegebenen [[../../Theo I/Turingmaschinen|TM]] für $r$ lässt sich eine TM für $s$ konstruieren, die keine Platzschranken einhält (sonst Widerspruch zum [[Hierarchiesätze|Hierarchiesätze]]
- "Es gibt Situationen, in denen wir mehr haben können, aber trotzdem nicht mehr können"
Beispiele: $r:n\mapsto 2^n\rightarrow DTIME(s)=DTIME(2^s)$
→ $s$ soll kein Polynom o.Ä. sein, sonst wäre $s$ konstruierbar
^1660503040608

## Beweis:
→ F35.2ff.
