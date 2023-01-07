---
tags: uni dsa practical-cs tree indexstruct
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - 2-3-4-Baum
  - 2-3-4-Bäume
linter-yaml-title-alias: 2-3-4-Baum
date-of-creation: 2022-07-22
mod-date: 2022-09-10
---

# 2-3-4-Baum

## Eigenschaften: #fc
- Jeder innere Knoten beinhaltet bis zu *3 Schlüsselwerte* und weist entweder *2, 3, oder 4* ausgehende *Kanten* auf
- Die Verwaltung der Knoten mit unterschiedlichen Schlüsselanzahlen ist umständlich
	→ [[Rot-Schwarz-Baum]]
- Die Baum-Invariante wird vor dem Einfügen eines neuen Knotens eingefügt[^1]
	→ Dies ist sicherlich auch von der Realisierung abhängig
^1662817200000

## Einfügen: #fc
- Die Einfügeposition wird gesucht
	→ Falls ein identischer Wert im Baum existiert, wird nicht eingefügt
- Die Such-Operation liefert den Blattknoten $b$
	→ *Vor dem Einfügen* wird die Datenstruktur-Invariante ausgeglichen:
	- Wenn $b$ ein 2- oder 3-Knoten ist, kann ohne Rücksicht auf Verluste eingefügt werden
	- Falls $b$ ein 4-Knoten ist, wird der *mittlere Schlüsselwert* *Bottom-Up* nach oben gezogen
^1652805423151

[^1]:Sandro Speth bei einer Hörsaal-Übung
