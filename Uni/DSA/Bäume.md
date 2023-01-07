---
tags: uni dsa practical-cs tree indexstruct abstraction
cards-deck: Uni::Courses::DSA
completed: true
aliases:
  - Bäume
  - Baum
  - Pseudoknoten
  - Einwegbaum
  - voll
  - vollständig
linter-yaml-title-alias: Bäume
date-of-creation: 2022-07-22
mod-date: 2022-09-10
---

# Bäume
→ Zusammenhängende, azyklische [[Graphen|Graphen]]
→ [[Bäume/Traversierung|Traversierung]]

## Grundlegende Fachtermini: #fc
- *Kanten*
- *Wurzelknoten*
- *Kind-/ Elternknoten*
- *Innerer Knoten/ Blätter*
- $n$-ärer - $n=$ globale, maximale Anzahl an Kanten
- *Pfad* = Eine Folge von unterschiedlichen, zusammenhängenden Kanten
- *Niveau* (→ Zählung beginnt bei 0)
^1651408603108

## Fachtermini für Eigenschaften: #fc
- *Pseudoknoten*: Vereinfachung zum Testen auf Leerheit und null-Verweise
	→ Am rechten Knoten des Head-Nodes hängt der Wurzelknoten
- *voll*: Ein $n$-ärer Baum ist voll, wenn alle Knoten entweder 0 oder $n$ Kindknoten aufweisen
- *Vollständigkeit*: Alle Blattknoten eines vollständigen Baumes liegen auf demselben Niveau
- [[Bäume/Balancierter Baum|Ausgeglichener/ Balancierter Baum]]
- [[Bäume/Geordneter Baum|Geordneter Baum]]
- *Einwegbaum* $\Leftrightarrow$ [[Bäume/Mehrwegbäume|Mehrwegbaum]]
^1651408861452

## Vergleich: #fc
| Baum-Typ                                            | Kategorie                     | Ausgeglichen   | Eigenschaften                    |     |
| --------------------------------------------------- | ----------------------------- | -------------- | -------------------------------- | --- |
| [[Bäume/Suchbaum\|Suchbaum]]                        |                               | $\times$       | binär                            |     |
| Octree/ Quadtree                                    | Mehrwegbaum                   | $\times$       | quartär/ octär                   |     |
| [[Bäume/AVL-Baum\|AVL-Baum]]                        | Einwegbaum, Suchbaum          | $\checkmark$ | AVL-Kriterium                    |     |
| [[Bäume/2-3-4-Baum\|2-3-4-Baum]]                    | Mehrwegbaum, Suchbaum         | $\checkmark$   | 2-3-4-Knoten                     |     |
| [[Bäume/Rot-Schwarz-Baum\|RS-Baum]]                 | Einwegbaum, Suchbaum          | $\checkmark$  | Schwarztiefe, binärer 2-3-4-Baum |     |
| [[Bäume/B-Baum\|B-Baum]]                            | Mehrwegbaum, Suchbaum         | $\checkmark$   | B-Baum-Kriterium                 |     |
| [[Bäume/Tries-Baum\|Tries-Baum]]                    | [[Bäume/Digitalbäume\|Digitalbaum]] | $\times$       | Kante = Buchstabe                |     |
| [[Bäume/Patricia-Baum\|Patricia-Baum]]              | [[Bäume/Digitalbäume\|Digitalbaum]] | $\times$       | Knoten = Überspringen            |     |
| [[Bäume/Präfix-Baum]]                                     | [[Bäume/Digitalbäume\|Digitalbaum]] | $\times$       | Knoten = In-/Suf-/Präfix         |     |
| [[Bäume/Heap\|Heap]]                                | (vollständiger) Einwegbaum    | $\checkmark$   | Partielle Ordnung                |     |
| [[Graphen/Spann- & Wurzelbaum\|Spann-/ Wurzelbaum]] |                              | $\times$               |                                  |     |
^1652106009734
