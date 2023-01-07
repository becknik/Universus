---
tags: uni dsa practical-cs struct graph abstraction
cards-deck: Uni::Courses::DSA
completed: true
aliases: Datenstrukturen für Graphen
linter-yaml-title-alias: Datenstrukturen für Graphen
date-of-creation: 2022-07-24
mod-date: 2022-09-03
---

# Datenstrukturen für Graphen

## Varianten: #fc
- Allgemeine Annahme: Knoten sind konsistent durchnummeriert
- [[Graphen/Datenstrukturen/Kantenliste|Kantenliste]]
- [[Graphen/Datenstrukturen/Knotenliste|Knotenliste]]
	→ Beide eignen sich vor Allem zum Speichern von unveränderlichen Graphen
- [[Graphen/Datenstrukturen/Adjazenzmatrix|Adjazenzmatrix]]
- [[Graphen/Datenstrukturen/Adjazenzliste|Adjazenzliste]]
→ Transformationen zwischen den Datenstrukturen liegt zwischen $\mathbfcal{O}(n+m)$ & $\mathbfcal{O}(n²)$
^1658939355232

## Komplexitäten: #fc
| Operationen     | Kantenliste            | Knotenliste          | Adjazenzmatrix                             | Adjazenzliste                             |
| --------------- | ---------------------- | -------------------- | ------------------------------------------ | ----------------------------------------- |
| Kante einfügen  | $\mathbfcal{O}(m)$[^1] | $\mathbfcal{O}(n+m)$ | $\mathbfcal{O}(1)$                         | $\mathbfcal{O}(n)$                        |
| Kante löschen   | $\mathbfcal{O}(m)$     | $\mathbfcal{O}(n+m)$ | $\mathbfcal{O}(1)$                         | $\mathbfcal{O}(1)$/$\mathbfcal{O}(n)$[^3] |
| Knoten einfügen | $\mathbfcal{O}(1)$     | $\mathbfcal{O}(n+m)$ | $\mathbfcal{O}(n)$/$\mathbfcal{O}(n²)$[^2] | $\mathbfcal{O}(n)$                        |
| Knoten löschen  | $\mathbfcal{O}(m)$     | $\mathbfcal{O}(n+m)$ | $\mathbfcal{O}(n)$/$\mathbfcal{O}(n²)$[^2] | $\mathbfcal{O}(n+m)$                      |
→ $m = \|E\|, n = \|V\|$
- In der Realität werden z.B. noch Atribute benötigt, um den Fortschritt eines Algorithmus zu speichern
[^1]: Durch die Prüfung auf mögliche Doppelung - die notwendig ist
[^2]: Wenn die Matrix umkopiert werden soll/muss - nicht immer notwendig
[^3]: Nur in $\mathbfcal{O}(n)$ falls für die sekundären Listen [[Datenstrukturen/Linked List|Linked Lists]] zum Einsatz kommen
^1655395946601
