---
tags: uni dsa practical-cs problem algorithm
cards-deck: Uni::Courses::DSA
completed: false
aliases: Maximum Subarray Problem
linter-yaml-title-alias: Maximum Subarray Problem
date-of-creation: 2022-07-19
mod-date: 2022-09-05
---

# Maximum Subarray Problem

## Prinzip:
- Finde die maximale Summe aller Elemente einer Teilsumme eines Arrays ganzer Zahlen

## Algorithmus mit [[../Algorithmen/Muster/Scanline|Scanline-Ansatz]]: #fc
```java
public static int maxSumScanline(int[] numbers) {
	int scanMax = 0;
	int bisMax = 0;
	for (int i = 0; i < numbers.length; i++) {
		if (scanMax + numbers[i] > 0)
			scanMax = scanMax + numbers[i];
		else
			scanMax = 0;
		bisMax = Math.max(bisMax, scanMax);
	}
	return bisMax;
}
```
→ Effiziente Lösung in $\mathbfcal{O}(n)$
^1658308911904
