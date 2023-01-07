---
tags: uni dsa practical-cs algorithm complexity abstraction
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Sortierverfahren
  - instabil
  - stabil
  - out-of-place
  - in-situ
  - in-place
  - adaptiv
  - nicht adaptiv
linter-yaml-title-alias: Sortierverfahren
date-of-creation: 2022-07-21
mod-date: 2022-09-11
---

# Sortierverfahren

## Grundlegende Kategorisierung: #fc
- *Internes* Verfahren $\Leftrightarrow$ *Externes* Verfahren
	→ Sortieren den Datensatz auf dem *internen [[../Ro I/Speicher/DRAM|Hauptspeicher]]*
	→ Sortieren auf einem *externen* Speichermedien oder in großen Datenbanksystemen
- *Stabilität* $\Leftrightarrow$ *Instabilität*
	→ Stabilität: Beim Sortieren von Daten-Kompositionen wird die *relative Reihenfolge bei identischen Schlüsseln* beibehalten
- *In-Situ* $\Leftrightarrow$ Out-of-Place
	→ In-Situ: Die Platzkomplexität ist unabhängig von der Anzahl zu sortierender Elemente, meistens konstant
- *Adaptiv* $\Leftrightarrow$ *Nicht-adaptiv*[^1]
	→ Nicht-adaptiv: Die Zeitkomplexität hängt nicht von der Reihenfolge der Eingabedaten ab
	→ Hier schneiden [[Algorithmen/Sortieren/BubbleSort|BubbleSort]] und [[Algorithmen/Sortieren/InsertionSort|InsertionSort]] sehr gut ab
^1650720381789

## Komplexitäten & Stabilität #fc
| Verfahren                                              | Vergleiche: **Best**      | Vergleiche: **Mid**                                          | Vergleiche: **Worst**                                    | **Stabilität**      | In-/ Out-of-Place | Muster       |
| ------------------------------------------------------ | ------------------------- | ------------------------------------------------------------ | -------------------------------------------------------- | ------------------- | ----------------- | ------------ |
| [[Algorithmen/Sortieren/SelectionSort\|SelectionSort]] | $\mathbfcal{O}(n²)$       | $\Theta(\frac{n(n+1)}{2}) \rightarrow \mathbfcal{O}(n²)$     | $\mathbfcal{O}(n²)$                                      | $\times$            | In                | -            |
| [[Algorithmen/Sortieren/InsertionSort\|InsertionSort]] | $\Theta(n-1)$             | $\Theta(\frac{n(n-1)}{4}) \rightarrow \mathbfcal{O}(n²)$     | $\Theta(\frac{n(n-1)}{2}) \rightarrow \mathbfcal{O}(n²)$ | $\checkmark$        | In                | Inkrementell |
| [[Algorithmen/Sortieren/BubbleSort\|BubbleSort]]       | $\mathbfcal{O}(n)$        | $\Theta(\frac{n²}{2}) \rightarrow \mathbfcal{O}(n²)$         | $\Theta(\frac{n²}{2}) \rightarrow \mathbfcal{O}(n²)$     | $\checkmark$        | In                | Brute Force  |
| [[Algorithmen/Sortieren/MergeSort\|MergeSort]]         | $\mathbfcal{O}(n \log n)$ | $\mathbfcal{O}(n \log n)$                                    | $\mathbfcal{O}(n \log n)$                                | $\checkmark$        | Out               | D&C          |
| [[Algorithmen/Sortieren/QuickSort\|QuickSort]]         | $\mathbfcal{O}(n \log n)$ | $\approx\Theta(1,386 n\log n)\approx\mathbfcal{O}(2n\log n)$ | $\mathbfcal{O}(n²)$                                      | $\times$            | In                | D&C          |
| [[Algorithmen/Sortieren/HeapSort\|HeapSort]]           | $\mathbfcal{O}(n \log n)$ | $\mathbfcal{O}(n \log n)$ / $\Theta(\frac{3n}{2} \log n)$    | $\mathbfcal{O}(n \log n)$                                | $\times$            | In                | -            |
| [[Algorithmen/Sortieren/RadixSort\|RadixSort]]         |                           | $l\cdot n$                                                   |                                                          | $\checkmark/\times$ | In/Out            | Histogramm   |
| [[Algorithmen/Sortieren/ShellSort\|ShellSort]]         |                           |                                                              |                                                          |                     |                   |              |
→ MergeSort ist *nicht-adaptiv*
→ [[../Theo-III/Landau-Notationen|Landau-Notationen]], [[O-Notation]]
^1654716929581

[^1]: [Wikipedia](https://de.wikipedia.org/wiki/Sortierverfahren) (25.07.2022)
