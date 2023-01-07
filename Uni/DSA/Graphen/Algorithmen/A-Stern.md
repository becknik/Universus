---
tags: uni dsa practical-cs algorithm graph
cards-deck: Uni::Courses::DSA
completed: true
aliases: A*
linter-yaml-title-alias: A*
date-of-creation: 2022-07-23
mod-date: 2022-09-16
---

# A*

## Eigenschaften: #fc
- Der $A^*$-Algorithmus nutzt Heuristiken (z.B. Manhattan-Heuristik, Luftlinie) um den kürzesten Weg zum Ziel zu schätzen
	→ *Informierte Suche* "lenkt" die Richtung
- Der $A^*$-Algorithmus ist immer *optimal effizient* für eine *konsistente* Heuristik
	→ $A^*$ ist *vollständig*, d.h. eine Lösung wird gefunden, wenn sie existiert
	- **Zulässige Heuristik**:
	Sie darf die *Kosten nicht überschätzen*
	- **Konsistente/ Monotone Heuristik**:
	Dreiecksungleichung: Die Heuristik darf die Kosten nicht überschätzen (*zulässig*) $\wedge$ der geschätzte Wert $h(u) \leq$ $(g(u)~ \text{des Nachbarn} +~ h(u) \text{des Nachbarn})$
- $g(u)$: Die bisherigen Kosten von Startknoten bis zum Knoten $u$
- $h(u)$: Die geschätzten Kosten von $u$ bis zum Zielknoten
- $f(u) = g(u)+h(u)$: Die Kosten vom Startknoten bis zum Ziel
^1653941330565

## Funktionsweise: #fc
- Jeder Knoten $u$ bekommt die *folgende Attribute* zugewiesen:
	- $f(u) = g(u)+h(u)$: Die Kosten vom Startknoten bis zum Ziel
	- $g(u)$: Die bisherigen Kosten von Startknoten bis zum Knoten $u$
	- $h(u)$: Die geschätzten Kosten von $u$ bis zum Zielknoten
- $\forall v \in V: v \in \{ \text{CLOSED},\text{OPEN},\text{WHITE}\}$:
	- $\text{OPEN}$: Alle Knoten, zu denen bereits ein (nicht optimaler) Weg gefunden wurde
	- $\text{CLOSED}$: Knoten, zu denen schon der kürzeste Weg bekannt ist
		→ Werden nicht mehr betrachtet
	- $\text{WHITE}$: Noch nicht betrachtete Knoten
- Notation nach der Vorlesung: $$\displaylines{\text{OPEN}=<(~v_1,h(v_1),g(v_1)~),\dots,(~v_n,h(v_n),g(v_n)~)>,v_i\in V\newline}$$
1. Die Menge $\text{OPEN}$ wird mit dem Startknoten $s$ initialisiert, $\text{CLOSED}=\emptyset$
- Wiederhole, bis $\not\exists$ Knoten mehr $\in\text{OPEN}$:
	2. Betrachte den Knoten $v\in\text{OPEN}$ mit dem geringsten $f$-Wert
		 → Wenn $v$ dem gesuchten Knoten entspricht: `return v`
	3. Berechne $\forall$ an $v$ angrenzenden Knoten $u_{i\in\mathbb{N}}$, die $\notin\text{CLOSED}$ sind, den $g$- und $f$-Wert
		 → $g(u_i)=g(v)+\gamma((v,u_i)\in E)\rightarrow f(u_i)=g(u_i)+h(u_i)$
	4. für die Knoten $u_i,$ deren berechneter $f$-Wert *kleiner* als der Momentane ist oder die $\in\text{WHITE}$/ bisher noch nicht betrachtet wurden, werden die $g$- und $f$-Werte aktualisiert
		 → Falls $u_i\notin\text{OPEN}:$ Füge $u_i$ zu $\text{OPEN}$ hinzu
	5. Verschiebe $v$ aus $\text{OPEN}$ nach $\text{CLOSED}$
^1653940664083

## Algorithmus: #fc
```
Method: A*-Suche (G, start ∊ V, destination ∊ V)
PriorityQueue OPEN := [];
Liste CLOSED := [];
OPEN.enqueue(start);
while !OPEN.isEmpty() do
	// nextNode := angrenzender Knoten mit kleinsten f-Wert
	nextNode := extractMinimal(OPEN)
	if nextNode = destination then
		return WegGefunden;
	fi;
	expand(next);
	CLOSED.enqueue(next);
od;
return WegNichtGefunden;
```
```
Method: expand (u ∊ V)
for each v ∊ Successor(u) && v ∉ CLOSED do
	new_f := g(u) + γ(u, v) + h(v);
	if v ∊ OPEN && new_f ≥ f(v) then 
		continue;
	else // (f(v alter Pfad) > new_f) ∨ (v ∊ WHITE ∪ OPEN)
		Predecessor(v) := u;
		Aktualisiere f- und g-Wert von v;
		if v ∉ OPEN then
			OPEN.enqueue(v);
		fi;
	od;
end;
```
^1662563285940
