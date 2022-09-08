---
tags: uni dsa practical-cs algorithm
cards-deck: Uni::Courses::DSA
status: 
aliases: Euklidischer Algorithmus
linter-yaml-title-alias: Euklidischer Algorithmus
date: 2022-07-24
mod-date: 2022-09-02
---

# Euklidischer Algorithmus

## Eigenschaften:
- Ein Verfahren, um den [[Gemeinsamen Größten Teiler]] von $z_1,z_2\in\mathbb{Z}$ zu ermitteln

## Algorithmus: #fc
```
Method: modernEuclid (a, b) -> ggT(a, b)
x := a; y := b;
if y = 0 then
	return x
else
	return modernEuclid (y, x mod y)
```
^1662149110713