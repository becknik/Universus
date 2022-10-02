---
tags: uni theo-1 theoretical-cs theorem chomsky
cards-deck: Uni::Courses::Theo-I
complete: true
aliases:
  - Greibach-Normalform
  - GNF
linter-yaml-title-alias: Greibach-Normalform
date: 2022-09-20
mod-date: 2022-09-21
---

# Greibach-Normalform
-> [[Syntaxbäume]]

## Definition: #fc
- Eine [[../Typ-2|Typ-2 Grammatik]] $G$ mit der Regelmenge $P$ ist in Greibach-Normalform, wenn $$\forall(u,v)\in P:u\in V\wedge v\in\Sigma V^{Stern}$$ gilt.
	-> Jede Regel geht in *ein Terminal* und danach eine beliebige Anzahl an *Nicht-Terminalen* über
^1664631195388

## Satz: #fc
- Zu jeder kontextfreien Grammatik $G$ mit $\varepsilon\notin L(G):\exists G'$ in Greibach-Normalform, so dass $$L(G)=L(G')$$ gilt
^1664631195391

## Eigenschaften: #fc
- Die Ableitungslänge für ein Wort der Länge $n$ ist genau $n$
^1664631195394

## Algorithmen:
- Algorithmus 1: Hat zum Zeil, dass $A_i\rightarrow A_j\beta$ nur für $i<j$ in $P$ vorkommen
	-> Dabei sei $V=\{A_i,\dots,A_m\}$
```
FOR i := 1 TO m DO
	FOR j := 1 TO i-1 DO
		FORALL (A_i, A_{j}α) ∊ P DO
			IF (A_j, β_1|...|β_r) alle A_j-Regeln in P THEN
				Nimm (A_i, β_{1}α|...|β_{r}α) zu P hinzu;
				Streiche (A_i, A_{j}α) aus P heraus;
			ENDIF
		ENDFORALL
	ENDFOR
	Entferne Linksrekursion bzgl. A_i;
ENDFOR
```
- Wie geht es wohl weiter? Siehe V.12 F.22 ff. 😜
