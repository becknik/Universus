---
tags: uni theo-2 theoretical-cs
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Satz Von Rice
linter-yaml-title-alias: Satz Von Rice
date-of-creation: 2022-07-03
mod-date: 2022-09-12
---

# Satz Von Rice

## Definition: #fc
- Sei $\mathcal{R}$ die Klasse der [[../Berechenbarkeit/Turing-berechenbar|Turing-berechenbaren]] Funktionen und $\mathcal{S} \subset \mathcal{R}$ *nicht-trivial* ($\Rightarrow S\neq\emptyset\wedge S\neq\mathcal{R}$), dann ist $$C(\mathcal{S}) = \{w~| ~M_w ~berechnet ~die ~Funktion ~\mathcal{S}\}$$ eine [[Entscheidbarkeit|unentscheidbar]] Menge
	→ *Triviale Eigenschaften*: Die Eigenschaft trifft immer oder nie zu
^1660502822930

## Eigenschaften: #fc
- Die Spracheigenschaften einer [[../../Theo I/Turingmaschinen|TM]] (die von einer TM erkannte Sprache hat eine Eigenschaft $x$) sind unentscheidbar
	→ Oder: *Jede nicht-triviale semantische Eigenschaft von Algorithmen ist [[../Entscheidbarkeit|unentscheidbar]]*[^1]
- Eine Eigenschaft ist genau dann *trivial*, wenn *jede oder keine* berechnete Funktion sie hat[^1]
	→ *Nicht-triviale* semantische Eigenschaften sind solche, die manche berechenbare Funktionen haben und manche eben nicht
- ! Die *nicht-trivialen Eigenschaften* sind im Einzelfall [[../Entscheidbarkeit|entscheidbar]], im Allgemeinen hingegen nicht[^1]
	→ $\not\exists$ ein allgemeiner Algorithmus, der z.B. die Korrektheit aller Algorithmen nachweist
- Die [[../Halteprobleme|Halteprobleme]] sind ein Spezialfall vom Satz von Rice
^1662934971025

## Beweis:
- Zu zeigen: $\overline{H_0} \leq C(\mathcal{S})$
- Fall 1:
- Sei $\Omega\in\mathcal{S}, q\in\mathcal{R}\setminus\mathcal{S}\text{ beliebig }, Q$ eine [[../../Theo I/Turingmaschinen|TM]] zur Berechnung von $q$ und $w$ ein beliebiges Wort
- Sei $M$ definiert als:
```
Eingabe: y
Simuliere M_w wird auf \varepsilon
Simuliere dann Q auf y
```
- $M = M_{w'}\text{ und }f(w)=w', f$ ist total und berechenbar
- $w\in \overline{H_0}\Rightarrow\quad M$ hält auf keinem Input $\Rightarrow\quad M_{w'} \text{ berechnet } \Omega$ $\Rightarrow\quad w'\in C(\mathcal{S})$
- $w\in H_0\Rightarrow\quad M$ arbeitet schließlich wie $Q$ auf jedem Input $\Rightarrow\quad M_{w'} \text{ berechnet } q$ $\Rightarrow\quad w'\notin C(\mathcal{S})$
- Fall 2: (F.16.7)
→ $\overline{H_0} \leq C(\mathcal{S})\wedge {H_0} \leq C(\mathcal{S})$ für jeweils $\Omega\in\mathcal{S}\wedge\Omega\notin\mathcal{S}$, also ist $C(\mathcal{S})$ unentscheidbar

## Beispiele:[^1] #fc
1. Ist die berechnete Funktion total/ undefiniert/ injektiv/ surjektiv/ bijektiv…?
2. Berechnen zwei Algorithmen dieselbe Funktion?
3. Ist ein gegebener Algorithmus korrekt?
	 → Berechnet er das gewünschte Ergebnis?
^1664742712312

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021.
