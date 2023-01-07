---
tags: uni theo-2 theoretical-cs computability
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: GOTO
date-of-creation: 2022-08-06
mod-date: 2022-08-19
linter-yaml-title-alias: GOTO
---

# GOTO

## Syntax: #fc
- $x_i:=x_j\pm c$
	→ Zuweisungen werden genauso wie in [[LOOP|LOOP]] behandelt, nur dass zusätzlich zu jeder durchgeführten Operation ein Programmzähler hochgezählt werden muss, um den "*Prozedur-Abschnitt*" $M_i$ anzuzeigen
- $\text{GOTO }M_i$
- $\text{HALT}$
- $\text{IF }x_i=c\text{ THEN GOTO }M_j$
- *Programmstruktur*: $M_1:A_1; M_2:A_2; \dots;M_k:A_k$
^1660502742504

## Eigenschaften: #fc
- Jede [[../Turing-berechenbar|Turing-berechenbare]] Funktion ist GOTO-berechenbar (Beweis: V.9.2 ff.)
- Jedes GOTO-Programm kann durch ein [[WHILE|WHILE-Programm]] simuliert werden, das nur *eine einzige WHILE-Schleife enthält*
	→ Die WHILE-Schleife simuliert den *Programmzähler*
```
Wir simulieren M1 : A1; M2 : A2; ...; Mk : Ak durch:
	count := 1;
	WHILE count \neq 0 DO
		IF count = 1 THEN A'_1 END;
		IF count = 2 THEN A'_2 END;
		...
		IF count = k THEN A'_k END;
	END
wobei A' sich von A unterscheidet durch:
	x_j := x_l ± c; count := count + 1 //x_j:=x_l±c
	count := 0 //HALT
	count := n //GOTO M_n
	IF x_j = c THEN count := n //IF x_j = c THEN GOTO M_n
	ELSE count := count + 1 END
```
^1664742232240
