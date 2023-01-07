---
tags: uni dsa practical-cs graph parallel
cards-deck: Uni::Courses::DSA
completed: true
aliases: Petri-Netze
linter-yaml-title-alias: Petri-Netze
date-of-creation: 2022-07-24
mod-date: 2022-09-13
---

# Petri-Netze

## Definition

### Variablen #fc
- $P = (S,T,E,A,M)$
- $S,T \neq \emptyset$
- $S \cap T = \emptyset$
- **A**usgangskanten: $A \subset S \times T$: **S**tellen $\longrightarrow$ **T**ransition
- **E**ingangskanten: $E \subset T \times S$: **T**ransition $\longrightarrow$ **S**tellen
- $M:S \rightarrow \mathbb{N}_0$: Start**m**arkierungen/ Tokens
- *Vorbereich der Transition*: $\bullet t=\{s\in S\mid(s,t)\in A\}$
- *Nachbereich der Transition*: $t\bullet=\{s\in S\mid(t,s)\in E\}$
^1656967985352

### **Schaltregel**: #fc
- Eine Transitions $t$ kann *schalten/ feuern*, wenn jede Eingangsstelle mindestens eine Marke enthält
- Beim Schaltvorgang wird aus jeder Stelle eine Marke entfernt und zu jeder Ausgangsstelle eine Marke hinzugefügt
	→ Markierungen dürfen *nicht aufgeteilt* werden
	→ Die *Kapazitäten von Ausgangsstellen* darf durch die Transition nicht verletzt werden
	→ Die Transitionen erzeugen so viele Markierungen, wie es Kanten gibt
^1663100996385

## Eigenschaften: #fc
- Ein Modell für *kommunizierende Prozesse*, basierend auf dem Konzept von *Nichtdeterminismus* und [[../../Theo I/3. Typ - REG/Deterministischer Endlicher Automat|DFAs]]
	→ Sind [[../Graphen/Gerichtete Graphen|gerichtete]], [[../Graphen/Bipartite Graphen|bipartite Graphen]] mit Zuständen (=Stellen)
- Wurde 1962 von *Carl Adam Petri* entwickelt
- Wird neben der Softwareentwicklung auch zur Beschreibung von Workflows, logischen Systemen und hardwarenaher Abläufe eingesetzt[^1]
^1657012929836

## Varianten: #fc
- *Bedingungs-Ereignis-Netz*: Stellen sind boolesche Variablen
- *Stellen-Transitions-Netz*: Stellen können *unsigned Integer-Werte* annehmen und *Kapazitäten* aufweisen
- *Höhere Petri-Netze*: Stellen sind Container für (strukturierte) Werte, also Werte, die selber mit zu ihrer Präsenz zusätzlichen Daten versehen sind
^1656968221313

## Beispiele für Kommunizierende Prozesse:
- *Client-Server-Anwendungen*
- *Produzenten-Verbraucher-Systeme*: Logistik-Anlagen
- *Agenten-Systeme*: Internet, Simulationen, Spiele
- OSs & GUIs

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021. S.170
