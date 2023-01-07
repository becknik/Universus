---
tags: uni dsa practical-cs algorithm text
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Boyer-Moore
  - BM
linter-yaml-title-alias: Boyer-Moore
date-of-creation: 2022-07-24
mod-date: 2022-09-07
---

# Boyer-Moore
→ [[../../Text-Such-Algorithmem|Text-Such-Algorithmen]]

## Eigenschaften: #fc
- Vergleich starten am *n.* Index des Patterns
- Nutzt *positiven* sowie *negativen Informationen* des vorherigen Vergleichs:
→ **Good-Suffix-** oder **Match-Heuristik**: Informationen lassen sich aus dem Muster selbst herleiten (*shift*-Tabelle)
- Berücksichtigt auch die *Zusatzinformationen* aus dem vorherigen Vergleich
→ **Bad-Character-** oder **Occurrence-Heuristik**: Muster und Text werden benötigt (*Last*-Tabelle)
- *shift*-Tabelle: Enthält die sichere Verschiebedistanz für jeden *Suffix des Musters*
- *last*-Tabelle: Speichert für *jedes Zeichen im Text* die sichere Verschiebedistanz
^1655836926373

## Tabellen-Strukturen: #fc
- *last*-Tabelle:
	- $last[c\in\Sigma] = \max\{-1,j\mid p_j=c\}$ für $p=c_0,\dots,c_{m-1},c_i\in\Sigma$
- *suffix*-Tabelle:
	- Für jeden Präfix von $1,\dots,|p|$ wird geprüft, wie viele Zeichen sein Suffix mit dem Suffix des Patterns $p$ übereinstimmt
		→ Die Prüfung des Suffix des erzeugten Präfix unterscheidet sich (abgesehen vom Startindex des erzeugten Präfixes) also dadurch zum [[Knuth-Morris-Pratt|KMP-Algorithmus]], dass der Vergleich zum Suffix und nicht zum Präfix des unmodifizierte Patterns $p$ erfolgt
- *shift*-Tabelle:
	- Es wird eine $(m+2)\times m$ Matrix initialisiert
	- Die Ergebnisse der Präfixfunktion auf $[m-1..1]$ werden in der *oberen Dreiecksmatrix* festgehalten
		→ In der Untersten Zeile wird ein Wildcard eingesetzt
	- Für jede $i.$ Ausgabe der Suffixfunktion auf $[m-1..1]$ auf $p$ wird die *erste markierte Zeile* in die Tabelle übernommen, dessen Suffix bis zu $i$ nicht mit dem Suffix der 0. Zeile (=$p$) übereinstimmt
		→ Spalten werden *missachtet*, wenn sie aktuell nicht (mehr) markiert sind (ausgenommen der 1. Iteration)
		→ Spalten, die kürzer als $i$ sind und nach der $i.$ Iteration immer noch markiert sind, werden zur Wildcard
		→ Wenn alle übrigen, markierten Suffixe mit $p$ übereinstimmen, füllt die nächste Wildcard den Index der *shift*-Tabelle
	- Die Zeilen, die mit dem aktuellen Suffix der 0. Spalte übereinstimmenden, oder Wildcards werden *bis zur aktuellen Spalte gefärbt*
- **Endgültige Verschiebedistanz** bei einem Misfit von $p[j]$ mit $text[i]\in\Sigma$: $i:=i+\max(shift[j],j-last[text[i]])$
	→ Oder: Verrücke Muster um $\max\{\text{Index}- last[\text{Zusatzinformation}], shift[\text{negative Information}]\}$
Beispiel:
![GitHub](https://raw.githubusercontent.com/jarnnk/UNIversus/main/Uni/DSA/Algorithmen/Text/_Figures/Beispiel%20Boyer-Moore%20Tabellen.png)
^1655839590887

## Beispiel 2:
| chars     | a   | v   | w   | x   | y   | z   |
| --------- | --- | --- | --- | --- | --- | --- |
| $last[c]$ | -1  | -1  | -1  | 4   | 5   | 6   |

| i          | 0   | 1   | 2   | 3   | 4   | 5   | 6   |
| ---------- | --- | --- | --- | --- | --- | --- | --- |
| $p[i]$     | x   | x   | y   | z   | x   | y   | z   |
| $shift[i]$ | 7   | 7   | 7   | 3   | 7   | 7   | 1   |
![[_Figures/Beispiel Boyer-Moore Anwendung.png]]
