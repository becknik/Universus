---
tags: uni dsa practical-cs algorithm search
cards-deck: Uni::Courses::DSA
complete: true
aliases: Binäre Suche
linter-yaml-title-alias: Binäre Suche
date: 2022-07-24
mod-date: 2022-09-05
---

# Binäre Suche

## Eigenschaften:
- Nutzt die [[../../Sortierverfahren|Sortierung]] und den *wahlfreien Zugriff* auf die Folge aus
	-> Funktioniert nur auf sortierten Daten, die [[Sequenzielle Suche|Sequenzielle Suche]] hingegen auch auf unsortierten
- Die ungünstigste Position befindet sich links der Mitte (?) oder am letzten Index der Folge
- Verwendet das [[../Muster/Divide And Conquer|Divide & Conquer]] Algorithmenmuster
- Der $\lceil$mittlere Eintrag$\rceil$ wird gewählt und überprüft, ob der gesuchte Wert kleiner oder größer als dieses Element ist
	-> Rekursives Wiederholen in der entsprechenden Hälfte, bis das gesuchte Element das mittlere Element ist

## Aufwand: #fc
| Fall                             | Vergleiche |
| -------------------------------- | ---------- |
| Bester Fall                      | 1          |
| Schlechtester Fall               | $\lceil\log n\rceil$   |
|                                  |            |
| Durchschnitt: Erfolgreiche Suche | $\log n$   |
| Durchschnitt: Erfolglose Suche   | $\log n$   |
^1658939325773

## Algorithmus: (rekursiv & iterativ) #fc
```
Method: BinarySearchRec (F, k, u, o) -> p
if u > o then
	return NO_KEY
m := (u + o) / 2;
if F[m] = k then
	return m
else if k < F[m] then
	return BinarySearchRec (F, k, u, m − 1);
else
	return BinarySearchRec (F, k, m + 1, o);
fi
```
```
Method: BinarySearch (F, k) -> p
u := 0, o := n − 1;
while u <= o do
	m := (u + o) / 2;
	if F[m] = k then
		return m
	else if k < F[m] then
		o := m − 1
	else u := m + 1
return NO_KEY
```
^1658939454606
