---
tags: uni dsa practical-cs graph parallel
cards-deck: Uni::Courses::DSA
status: 
aliases: Petri-Netze
linter-yaml-title-alias: Petri-Netze
date: 2022-07-24
mod-date: 2022-09-08
---

# Petri-Netze

## Definition: #fc
- $P = (S,T,E,A,M)$
- $S,T \neq \emptyset$
- $S \cap T = \emptyset$
- $A \subset S \times T$: Stellen $\longrightarrow$ Transition
- $E \subset T \times S$: Transition $\longrightarrow$ Stellen
- $M:S \rightarrow \mathbb{N}_0$: Startmarkierungen/ Tokens
- **Schaltregel**:
	- Eine Transitions $t$ kann *schalten/ feuern*, wenn jede Eingangsstelle mindestens eine Marke enthält
	- Beim Schaltvorgang wird aus jeder Stelle eine Marke entfernt und zu jeder Ausgangsstelle eine Marke hinzugefügt
	-> Markierungen dürfen *nicht aufgeteilt* werden
	-> Die *Kapazitäten von Ausgangsstellen* darf durch die Transition nicht verletzt werden
	-> Die Transitionen erzeugen so viele Markierungen, wie es Kanten gibt
^1656967985352

## Eigenschaften: #fc
- Ein Modell für *kommunizierende Prozesse*, basierend auf dem Konzept von [[../../Theo I/DEA|DEAs]]
	-> Sind [[../Graphen/Gerichtete Graphen|gerichtete]], [[../Graphen/Bipartite Graphen|bipartite Graphen]] mit Zuständen (=Stellen)
- Wurde 1962 von *Carl Adam Petri* entwickelt
- Beschreibt *Nebenläufigkeit* und *nichtdeterministische Vorgänge*
^1657012929836

## Varianten: #fc
- *Bedingungs-Ereignis-Netz*: Stellen sind boolesch
- *Stellen-Transitions-Netz*: Integer-Werte an Stellen ($\leq$ Kapazität)
- *Höhere Petri-Netze*: Stellen sind Container für (strukturierte) Werte
	-> z.B. "gefärbte" Marken
^1656968221313

## Beispiele für Kommunizierende Prozesse:
- *Client-Server-Anwendungen*
- *Produzenten-Verbraucher-Systeme*: Logistik-Anlagen
- *Agenten-Systeme*: Internet, Simulationen, Spiele
- OSs & GUIs
