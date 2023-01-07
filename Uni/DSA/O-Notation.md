---
tags: uni dsa practical-cs complexity
cards-deck: Uni::Courses::DSA
completed: true
aliases: O-Notation
linter-yaml-title-alias: O-Notation
date-of-creation: 2022-07-21
mod-date: 2022-09-13
---

# O-Notation
→ [[../Theo-III/Landau-Notationen]]

## Definition:

## Aufwand: #fc
- Definiert eine asymptotische obere Grenze für eine Funktion $f$, die durch eine bestimmte Art von *Rechenzeit-Operation* (z.B. Anzahl der Vergleiche, Speicherzugriffe, arithmetische Operationen) und den dabei *verbrauchten Speicherplatz* abgeschätzt wird
- Aufwandsfunktionen lassen sich in den seltensten Fällen exakt bestimmen und werden durch Analysemethoden wie "Aufwand im *schlechtesten Fall*" oder "Aufwand *im Mittel*" bestimmt
^1650913820879

## Vereinfachungen & Praxis: #fc
- Konstante Vorfaktoren können ignoriert werden
	→ Da $n$ i.d.R. recht klein ist, sollte Konstanten nicht komplett missachtet werden
- Man kann sich auf den höchsten Exponenten beschränken
	→ Algorithmen in exponentieller Laufzeit können aufgrund von einer geringeren Methoden-Komplexität & Compiler-Optimierungen für kleine Datensätze schneller als solche mit logarithmischer Laufzeit sein
	→ beispielsweise kann [[Algorithmen/Sortieren/InsertionSort|InsertionSort]] für kleine Eingabemengen schneller als [[Algorithmen/Sortieren/QuickSort|QuickSort]] sein
- Die Basis des Logarithmus' ist unerheblich
- Aussagen über die [[../Theo II/Komplexitättheorie/Zeitkomplexität|Zeitkomplexität]] werden durch Laufzeitumgebung/ virtuelle Maschine, Compiler, [[../../Softwareentwicklung/Programmiersprachen|Programmiersprache]], [[../Ro I/CPU/Befehlssatz Architektur|ISA]], Prozessor, [[../Ro I/Cache|Caches]], [[../Ro I/Speicher|Speicher]] (…) beeinflusst
^1650912521544

## Beispiele zu den "Komplexitätsklassen" #fc
| Aufwand                   | Problemklasse                                                                                                                                                      |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| $\mathbfcal{O}(1)$        | Zugriff auf eine [[Hashfunktionen\|Hashtabelle]], *wahlfreier Zugriff* auf Arrays, Zugriff aufs *erste Element* einer [[Datenstrukturen/Linked List\|Linked List]] |
| $\mathbfcal{O}(\log n)$   | Suche in *ausgeglichenen* [[Bäume\|Bäumen]], [[Algorithmen/Suche/Binäre Suche\|Binäre Suche]]                                                                      |
| $\mathbfcal{O}(n)$        | Suche in Texten, [[Algorithmen/Suche/Sequenzielle Suche\|Sequenzielle Suche]], syntaktische Analyse von Programmiersprachen mit "guter" Grammatik                  |
| $\mathbfcal{O}(n \log n)$ | [[Sortierverfahren]]                                                                                                                                               |
| $\mathbfcal{O}(n^k)$      | (einfache) Matritzen-Multiplikation                                                                                                                                |
| $\mathbfcal{O}(2^n)$      | [[../Theo II/Problemklassen\|Optimierungsprobleme]] wie optimale Schaltwerke, automatisches Beweisen im Prädikatenkalkül 1. Stufe                                  |
→ $\mathbfcal{O}(\infty)$ ist nicht korrekt für Programme, die nicht terminieren
^1650912830194
