---
tags: uni dsa practical-cs tree digital-tree indexstruct
cards-deck: Uni::Courses::DSA
completed: true
aliases: Präfix-Baum
linter-yaml-title-alias: Präfix-Baum
date-of-creation: 2022-07-24
mod-date: 2022-09-07
---

# Präfix-Baum
→ [[Digitalbäume|Digitalbäume]]

## Struktur: #fc
- Die *inneren Knoten* speichern die Anzahl der zu *überspringenden Indizes* bis zum nächsten unterschiedlichen Buchstaben und den zugehörigen Prä-/Infix
	→ [[Patricia-Baum|Patricia-Bäume]] speicher hingegen nur die Anzahl der übersprungenen Indizes
- Die Blattknoten beinhalten nur den entsprechenden Präfix ohne den Betrag der Indizes
	→ Bei Wörtern, die nur aus einem Präfix bestehen, wird eine $\varepsilon$-Kante zu einem $\varepsilon$ Blattknoten eingefügt
- Die Kanten speichern die sich unterscheidenden Alphabetszeichen
^1654726238132

## Eigenschaften:
- Werden zur Erstellung von Tag-Clouds verwendet
