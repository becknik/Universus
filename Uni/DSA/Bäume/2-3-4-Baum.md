---
tags: uni dsa practical-cs tree indexstruct
cards-deck: Uni::Courses::DSA
complete: true
aliases:
  - 2-3-4-Baum
  - 2-3-4-Bäume
linter-yaml-title-alias: 2-3-4-Baum
date: 2022-07-22
mod-date: 2022-09-05
---

# 2-3-4-Baum

## Eigenschaften:
- Jeder innere Knoten beinhaltet bis zu *3 Schlüsselwerte* und weist entweder *2, 3, oder 4* ausgehende *Kanten* auf
- Die Verwaltung der Knoten mit unterschiedlichen Schlüsselanzahlen ist umständlich
	-> [[Rot-Schwarz-Baum]]

## Einfügen: #fc
- Die Einfügeposition wird gesucht
	-> Falls ein identischer Wert im Baum existiert, wird nicht eingefügt
- Die Such-Operation liefert den Blattknoten $b$
	-> *Vor dem Einfügen* wird die Datenstruktur-Invariante ausgeglichen:
	- Wenn $b$ ein 2- oder 3-Knoten ist, kann ohne Rücksicht auf Verluste eingefügt werden
	- Falls $b$ ein 4-Knoten ist, wird der *mittlere Schlüsselwert* *Bottom-Up* nach oben gezogen
^1652805423151
