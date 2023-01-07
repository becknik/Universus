---
tags: uni dsa practical-cs algorithm sort
cards-deck: Uni::Courses::DSA
completed: true
aliases: MergeSort
linter-yaml-title-alias: MergeSort
date-of-creation: 2022-07-21
mod-date: 2022-09-11
---

# MergeSort

## Funktionsweise:
- Sortieren durch *rekursives Zerlegen* in *atomare Elemente* und daraufhin rückläufiges Zusammenfügen

## Eigenschaften #fc
- Der Algorithmus wurde ursprünglich zur Sortierung von *sehr großen Datensätzen* auf externen Speichermedien entworfen
- MergeSort setzt sich aus den Prozeduren *Split* und *Merge* zusammen
- MergeSort ist ein *nicht-adaptives* Sortierverfahren
	→ Der Aufwand für Merge-Sort ist unabhängig von der Eingabereihenfolge (Siehe [[../../Sortierverfahren|Sortierverfahren]])
- Der Algorithmus benötigt immer $n$ Zwischenspeicher
- Funktioniert *rekursiv* und *Out-of-Place*
	→ Hat hohen Ressourcenverbrauch
- Basiert auf dem [[../Muster/Divide And Conquer|Divide & Conquer]] Algorithmenmuster
^1650721930766

## Herleitung der Laufzeitkomplexität:[^1]
- Zusammenhang zwischen der Vergleiche $V_n$ und der Länge der Folg$n:V_n=2V_{\frac{n}{2}}+n$ für $n\geq2$ mit $V_1=0$
- Trick: Annahme $n=2^N$ gelte, dann gilt $V_{2^N}=2V_{2^{N-1}}+2^N\Leftrightarrow \frac{V_{2^N}}{2^N}= \frac{V_{2^{N-i}}}{2^{N-i}}+1$
	→ Letzteres so lange wiederholen, bis $i=N$
- $=\dots=\frac{V_{2^0}}{2^0}+\dots+1=N$ und da $n=2^N,$ folgt $N=\log_2n$
	→ $\frac{V_n}{n}=\log_2n\Leftrightarrow V_n=n\log_2n$

## Algorithmus: #fc
```
Method: MergeSort(F) → F_Sssss
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

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021.
