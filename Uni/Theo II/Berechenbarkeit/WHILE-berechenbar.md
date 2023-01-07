---
tags: uni theo-2 theoretical-cs computability trait
cards-deck: Uni::Courses::Theo-II
completed: false
aliases: WHILE-berechenbar
linter-yaml-title-alias: WHILE-berechenbar
date-of-creation: 2022-08-06
mod-date: 2022-09-04
---

# WHILE-berechenbar
→ Identisch zur Definition von [[LOOP-berechenbar|LOOP-berechenbar]], nur mit $P \in$ [[WHILE|WHILE]]

## Eigenschaften: #fc
- [[Normalform-Theorem von Kleene]]
- Jedes WHILE-Programm kann durch ein [[GOTO|GOTO-Programm]] *simuliert* werden
- [[Church-Turing-These|Church-Turing-These]]: $WHILE=TM$
	→ [[Turing-berechenbar|Turing-berechenbar]]
- Eine [[Applikativ/µ-Rekursion|µ-rekursive]] Funktion ist WHILE-berechenbar
- Jede WHILE-berechenbare Funktion $f:\mathbb{N}^r\rightarrow\mathbb{N}$ ist [[Applikativ/Arithmetische Repräsentierbarkeit|arithmetisch repräsentierbar]]
- $\exists$ totale WHILE-berechenbare Funktionen, die nicht [[LOOP-berechenbar|LOOP-berechenbar]] sind
	→ Beispiel: [[Ackermann-Funktion|Ackermann-Funktion]]
^1660502726880

## Beweis - WHILE $\Rightarrow$ Arithmetisch repräsentierbar:
Die $(2k+2)$-stellige Funktion $F_P(M_0,\dots,m_k,n_0,\dots,n_k)$ soll genau dann wahr sein, wenn das Programm $P~\forall i$ mit $x_i=m_i$ startet und in $x_i=n_i$ stoppt
*Zuweisungen*: $F_P\equiv(n_0=m_0)\wedge\dots\wedge(n_{i-1}=m_{i-1})\wedge(n_i=m_j\pm c)$$\wedge(n_{i+1}=m_{i+1})\wedge\dots\wedge(n_k=m_k)$
*Hintereinanderausführungen*: $F_P=\exists w_0\exists w_1\dots\exists w_k~~F_Q(m_0,\dots,m_k,w_0,\dots,w_k)~\wedge$$F_R(w_0,\dots,w_k,n_0,\dots,n_k)$
*WHILE-Scheife*: Rechenteppich (?) (F22.1) !!!
→ Die "horizontalen Pünktchen" werden durch das [[Gödelprädikat|Prädikat G]] ersetzt !!!
