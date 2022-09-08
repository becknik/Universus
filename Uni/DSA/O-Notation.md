---
tags: uni dsa practical-cs complexity
cards-deck: Uni::Courses::DSA
status: 
aliases: O-Notation
linter-yaml-title-alias: O-Notation
date: 2022-07-21
mod-date: 2022-09-02
---

# O-Notation
- [[Landau-Notationen]]

## Definition: #fc
- Definiert eine asymptotische obere Grenze für eine Funktion $f$ im Bezug auf ihre Rechenzeit oder den verbrauchten Speicherplatz
	-> Die zugehörigen Funktionen sind für genügend Große $n$ nur durch die Funktion $g(n)$ und die Konstante $c$ asymptotisch beschränkt
- Vereinfachungen sind durch das Rechnen in Größenordnungen möglich
^1650913820879

## Vereinfachungen & Praxis: #fc
- Konstante Vorfaktoren können ignoriert werden
	-> Da $n$ i.d.R. recht klein ist, sollte Konstanten nicht komplett missachtet werden
- Man kann sich auf den höchsten Exponenten beschränken
	-> Algorithmen in exponentieller Laufzeit können aufgrund von einer geringeren Methoden-Komplexität & Compiler-Optimierungen für kleine Datensätze schneller als solche mit logarithmischer Laufzeit sein
	-> beispielsweise kann [[Algorithmen/Sortieren/InsertionSort|InsertionSort]] für kleine Eingabemengen schneller als [[Algorithmen/Sortieren/QuickSort|QuickSort]] sein
- Die Basis des Logarithmus' ist unerheblich
- Aussagen über die [[../Theo II/Komplexitättheorie/Zeitkomplexität|Zeitkomplexität]] werden durch Laufzeitumgebung/ virtuelle Maschine, Compiler, [[../../Privat/Programmiersprachen|Programmiersprache]], [[../Ro I/CPU/Befehlssatz Architektur|ISA]], Prozessor, [[../Ro I/Cache|Caches]], [[../Ro I/Speicher|Speicher]] (…) beeinflusst
^1650912521544

## Beispiele zu den "Komplexitätsklassen" #fc
| Aufwand                   | Problemklasse                                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $\mathbfcal{O}(1)$        | Zugriff auf eine [[Hashfunktionen\|Hashtabelle]], wahlfreier Zugriff auf Arrays, Zugriff aufs erste Element einer [[Datenstrukturen/Linked List\|Linked List]] |
| $\mathbfcal{O}(\log n)$   | Suche in ausgeglichenen [[Bäume\|Bäumen]], [[Algorithmen/Suche/Binäre Suche\|Binäre Suche]]                                                                                |
| $\mathbfcal{O}(n)$        | Suche in Texten, [[Algorithmen/Suche/Sequenzielle Suche\|Sequenzielle Suche]], syntaktische Analyse von Programmiersprachen mit "guter" Grammatik                          |
| $\mathbfcal{O}(n \log n)$ | [[Sortierverfahren]]                                                                                                                                           |
| $\mathbfcal{O}(n^k)$      | (einfache) Matritzen-Multiplikation                                                                                                                            |
| $\mathbfcal{O}(2^n)$      | Viele Optimierungsprobleme                                                                                                                                     |
|                           |                                                                                                                                                                |
-> $\mathbfcal{O}(\infty)$ ist nicht korrekt für Programme, die nicht terminieren
^1650912830194
