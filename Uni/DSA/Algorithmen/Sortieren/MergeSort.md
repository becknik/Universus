---
tags: uni dsa practical-cs algorithm sort
cards-deck: Uni::Courses::DSA
complete: true
aliases: MergeSort
linter-yaml-title-alias: MergeSort
date: 2022-07-21
mod-date: 2022-09-06
---

# MergeSort

## Funktionsweise:
- Sortieren durch *rekursives Zerlegen* in *atomare Elemente* und daraufhin rückläufiges Zusammenfügen

## Eigenschaften #fc
- Der Algorithmus wurde ursprünglich zur Sortierung von *sehr großen Datensätzen* auf externen Speichermedien entworfen
- MergeSort setzt sich aus den Prozeduren *Split* und *Merge* zusammen
- MergeSort ist ein *nicht-adaptives* Sortierverfahren
	-> Der Aufwand für Merge-Sort ist unabhängig von der Eingabereihenfolge (Siehe [[../../Sortierverfahren|Sortierverfahren]])
- Der Algorithmus benötigt immer $n$ Zwischenspeicher
- Funktioniert *rekursiv* und *Out-of-Place*
	-> Hat hohen Ressourcenverbrauch
- Basiert auf dem [[../Muster/Divide And Conquer|Divide & Conquer]] Algorithmenmuster
^1650721930766

## Algorithmus: #fc
```
Method: MergeSort(F) -> F_Sssss
Falls |F| == 1:
	return F
Sonst:
	Teile F in F_1 (aufgerundeter Index) und F_2
	F_1 := MergeSort(F_1)  // F_1 ist nun sortiert oder einelementig
	F_2 := MergeSort(F_2)  // F_2 "
	return Merge(F_1,F_2
	// Merge-Prozedur: Die Elemente aus F_1 und F_2 werden iterativ verglichen und in F_S gefüllt
```
^1654702462157
