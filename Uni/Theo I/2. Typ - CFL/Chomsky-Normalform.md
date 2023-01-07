---
tags: uni theo-1 theoretical-cs theorem chomsky
cards-deck: Uni::Courses::Theo-I
completed: true
aliases:
  - Chomsky-Normalform
  - CNF
linter-yaml-title-alias: Chomsky-Normalform
date-of-creation: 2022-09-20
mod-date: 2022-10-01
---

# Chomsky-Normalform
→ [[Syntaxbäume]]

## Definition: #fc
- Eine [[../Typ-2|Typ-2 Grammatik]] $G$ mit der Regelmenge $P$ ist in Chomsky-Normalform, wenn $$\forall(u,v)\in P:u\in V\wedge v\in V^2\cup\Sigma$$ gilt.
^1664631085986

## Satz: #fc
- Zu jeder [[../Typ-2|kontextfreien Grammatik]] $G$ mit $\varepsilon\notin L(G):\exists G'$ in Chomsky-Normalform, so dass $$L(G)=L(G')$$ gilt
^1664631085990

## Eigenschaften: #fc
- Jede Grammatik in [[Chomsky-Normalform|CNF]] erzeugt einen [[../../DSA/Bäume|Binärbaum]], wenn man von den letzten Schritten durch die Pseudo-Terminale mal absieht
	→ *Satz*: Wenn ein Binärbaum mindestens $2^k$ Knoten, dann existiert auch mindestens ein Pfad der Länge $k$
- Die Ableitungslänge für ein Wort der Länge $n$ ist genau $2n-1$
- Kann minimal Wörter der Länge 2 erzeugen
^1664631085992

## Algorithmus zur Überführung $\text{Typ-2}\Rightarrow\text{CNF}$: #fc
1. *Entferne alle Ring-Ableitungen*:
	 - *Ring-Ableitung*: Ableitungsregeln der Form $B_i\rightarrow B_{i+1}$ für $i=1,\dots,r-1$ mit $r\geq2$ und $B_r\rightarrow B_1$ sind $\in P$
		 → Diese sollen (wenn sie existieren) durch eine neue Variable $B$ ersetzt werden, durch eine neue Variable $B$, wobei $B\rightarrow B$ entfernt werden müssen
	 - Die Beziehungen zwischen den Variablen $V$ sind nun als [[../../DSA/Graphen/Gerichteter Azyklischer Graph|DAG]] darstellbar
2. *Ordne die Variablen*:
	- $A\rightarrow B$ darf nur $\in P$ sein, wenn $B$ in der Anordnung hinter $A$ kommt
	- Falls es zur Umordnung kommt, muss die *Satzmenge* $B\rightarrow X_1\mid\dots\mid X_n$ (iterativ) an die weiter vorne liegende Variable $A$ *weitergegeben* werden: $A\rightarrow Y_1\mid\dots\mid Y_m\mid X_1\mid\dots\mid X_n$
	 (→ Ausführung im [[../../DSA/Graphen/Gerichteter Azyklischer Graph|DAG]]: Stelle die Verbindungen zwischen Variablen in einem Graphen dar und entferne iterativ die Knoten mit dem Ausgangsgrad 0, um sie bei |V| beginnende durchzunummerieren
	→ Danach ist $V=\{A_1,\dots,A_n\}$ und es existieren nur Kanten $A_i\rightarrow A_j,$ wenn $i<j$ gilt)
3. *Setze Abkürzungen ein*:
	- *Entferne* bei $i=|V|$ beginnend, iterativ *sukzessive Regeln* $A_i\rightarrow A_j$, indem Terminale Ableitungen $A_j\rightarrow v_1\mid\dots\mid v_n$ auf ihre Vorgänger-Variablen $A_i$ übertragen werden ($A_i\rightarrow u_1\mid\dots\mid u_m\mid v_1\mid\dots\mid v_n$)
	- *Lösche* Regeln der Form$(A_i,A_j)$ aus $P$
4. *Führe Pseudo-Terminale* ein:
	- *Ersetze die Nicht-Terminale der Satzmenge* $v$ aus $(u,v)\in P$ mit $|v|\geq2$ Nicht-Terminale nach dem Schema $V_a\rightarrow a$
	→ Wenn $a,b\in\Sigma,v=ab,$ dann besteht $v$ nach der Durchführung des Schrittes aus $V_aV_b,$ $V_a,V_b\in V$ und $\{(V_a,a),(V_b,b)\}\subseteq P$
5. *Fächere die Satzmenge auf*:
	- Ersetze Regeln der Form $(A,C_1\dots C_{k\geq3})$ durch $\{(A,C_1D_1),(D_1,C_2D_2),\dots,(D_{k-1},C_{k-1}C_k)\}$
^1664631820723
