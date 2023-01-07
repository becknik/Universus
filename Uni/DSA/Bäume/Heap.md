---
tags: uni dsa practical-cs tree struct indexstruct
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Heap
  - Prioritätswarteschlange
linter-yaml-title-alias: Heap
date-of-creation: 2022-07-22
mod-date: 2022-09-10
---

# Heap

## Eigenschaften: #fc
- Heaps sind abgeschwächt [[../Bäume|vollständiger]] Binärbäume
	→ Das unterste Niveau ist von links nach rechts aufgefüllt
- **Partielle Ordnung**: Der Schlüssel jedes innere Knoten ist kleiner oder gleichgroß wie der seine Kindknoten (Min-Heap)
	→ Heaps sind keine [[Suchbaum|Suchbäume]]!
	→ Eignet sich für die Realisierung von *Prioritätswarteschlangen* oder für den [[../Algorithmen/Sortieren/HeapSort|HeapSort-Algorithmus]]
- Ähneln strukturell einem Stammbaum im Allgäu (Danke, Sandro)
- Die Knotenmenge des Heaps wird nach [[Traversierung|Levelorder]] indexiert
	→ Die Position eines Elternknotens: $\lfloor \frac{j}{2}\rfloor$
	→ Die Position der beiden Kindknoten: $2j(+1)$
^1652813088229

## Aufbau der Partiellen Ordnung: #fc
- Die Durchsickern-Operation wird auf den Indizes $0$ bis $\lceil\frac{n}{2}\rceil$ ausgeführt
	→ Das aktuell ausgewählte Element $e_j$ sickert immer in die Richtung des Elements $\text{min}(e_{2j}, e_{2j+1}) < e$
^1652127107165

## Einfügen in den Heap: #fc
- Wenn das Array bis zum Index $n$ belegt ist, wird das neue Element an der Stelle $n+1$ eingefügt
- Dann wird die Durchsicker-Operation *Bottom-Up* auf dem Index $\lfloor \frac{n+1}{2}\rfloor$ angewandt
^1662408046937

## Versickern-Algorithmus: #fc
```java
private static void persolate(Comparable f[], int index)
	int i = index + 1;
	int j = 2 * i;
	while (j <= last) { // Das Element hat ein linkes Kind
		if (j < f.length() - 1) // Das Element hat ein rechtes Kind
			if (f[j-1].compareTo(f[j]) > 0) {
				j++; // f[j]= min{ f[j], f[j+1] }
			}
		if (f[i-1].compareTo(f[j-1]) > 0) {
			swap(f, i-1, j-1);
			i = j;
			j = 2 * i;
		}
		else {
			break;
		}
	}
```
- Es wird mit `index + 1` gearbeitet, da das erste Element an `f[0]` steht und daher die Bestimmung der Kinder (`j=2*0=0` oder `j=2*0+1=1`) für dieses Feld keinen Sinn ergeben würde
	→ Daher lieber `j=2*(0+1)=2` oder `j=2*(0+1)+1=3`, dann der Zugriff auf `f[i-1]==f[0]` und `f[j-1]==f[1]` oder `f[j-1]==f[2]`
^1662222397122
