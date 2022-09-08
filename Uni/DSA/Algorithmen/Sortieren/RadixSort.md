---
tags: uni dsa practical-cs algorithm sort
cards-deck: Uni::Courses::DSA
status: unfinished
aliases: RadixSort
linter-yaml-title-alias: RadixSort
date: 2022-07-23
mod-date: 2022-09-02
---

# RadixSort
- Nicht-vergleichsbasiertes Sortierverfahren
- Wechsel zwischen Verteilungsphase und Sammelphase
- Stabil
- Out-of-place

## Eigenschaften:
- Zeitkomplexität Bewegt Sich Zwischen O(n) Und O(n^2)
- Speicherkomplexität Liegt Bei Out-of-place Implementierung In O(n)<br>-&gt; Bei Der Implementierung Nach Saake &amp; Sattler In O(1) möglich, Dadurch wächst Allerdings Die Komplexität Durch Verwendung Von Histogrammen Etc. Nicht unerheblich<br>- In Der Regel out-of-place<br>- Instabil (?)

## Funktiosweise :
- Die einzelnen Ziffern oder Alphabetszeichen der Folgeglieder werden iterativ von hinten nach vorne miteinander vergleichen und ihren Werten entsprechend in Tupel/ Arrays/ Teile im Array eingefügt<br>-&gt; Durch jeder Iteration verfeinern sich die Tupel in der Anzahl der Elemente, die jeweils denselben Suffix aufweisen
