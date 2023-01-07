---
tags: uni dsa practical-cs graph flow
cards-deck: Uni::Courses::DSA
completed: true
aliases: Fluss
linter-yaml-title-alias: Fluss
date-of-creation: 2022-07-24
mod-date: 2022-09-03
---

# Fluss

## Definition: #fc
- Ein Fluss entspricht dem Graph der Flüsse zwischen den Knoten des [[Gewichteter Graph|gewichteten Graph]] $G$
- Die *Quelle* $s$ liefert beliebig viele Objekte pro Zeiteinheit und die *Senke* $t$ verbraucht diese
	→ Es muss in $G$ ein Pfad mit *nicht-negativen* Kanten von $s$ nach $t$ existieren
- Ein Fluss kann durch $val(G,F,s) = \sum_{u \in V} f(s,u)$ berechnet werden
^1658939237078

## Eigenschaften für Korrektheit: #fc
1. Der Fluss hält sich an die Kanten-Kapazitäten: $$f(u,v) \leq c(u,v)=\gamma((u,v)\in E)$$
	→ Restkapazität: $c_f(u,v) = c(u,v)-f(u,v)=c(v,u)+f(u,v)$
2. Konsistenz des Flusses: $$\forall(u,v)\in E:f(u,v)=-f(v,u)$$
3. Flusses bleibt erhalten: $$v\in V\setminus\{s,t\}:\sum_{u \in V} f(v,u) = 0$$
	→ Alle eingehenden Ströme werden zu ausgehenden Strömen
^1655040005940
