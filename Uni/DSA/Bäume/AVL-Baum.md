---
tags: uni dsa practical-cs tree indexstruct
cards-deck: Uni::Courses::DSA
completed: true
aliases: AVL-Baum
linter-yaml-title-alias: AVL-Baum
date-of-creation: 2022-07-22
mod-date: 2022-09-02
---

# AVL-Baum

## Eigenschaften: #fc
- **AVL-Kriterium**: In jedem Knoten wird der Betrag der Referenz der Höhe des linken und rechten Teilbaums $\in \{-1,0,1\}$ gespeichert
	→ Wurde 1962 von den russischen Mathematikern *Adelson-Velskii* und *Landis* aufgestellt
- Die Überprüfung des Kriteriums erfolgt beim Einfügen und Löschen *Bottom-Up*
	→ Ausgleich über *(Doppel-)Rotation(en)*
- Höhe eines AVL-Baums mit $n$ Knoten: $\log(n+1) \leq Höhe_{AVL}(n) \leq 1,44\log(n+2)-0,328\Rightarrow\mathbfcal{O}(\log n)$
^1652105852791
