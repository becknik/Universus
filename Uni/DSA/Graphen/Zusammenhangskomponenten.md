---
tags: uni dsa practical-cs
cards-deck: Uni::Courses::DSA
status: 
aliases: Zusammenhangskomponenten
linter-yaml-title-alias: Zusammenhangskomponenten
date: 2022-07-23
mod-date: 2022-09-08
---

# Zusammenhangskomponenten

## Definitionen: #fc
- **Starke/Schwache Zusammenhangskomponente**: Ein Teilgraph, der stark/ schwach zusammenhängend ist und *nicht erweitert* werden kann
	-> Ein *maximaler zusammenhängender Teilgraph*
- **Zusammenhängender Teilgraph**: Jeder Knoten ist in irgendeiner Weise mit jedem anderen Knoten verbunden
	-> Wenn das für den Teilgraphen nicht gilt, zerfällt er in *nicht-zusammenhängende Zusammenhangskomponenten*
- **Stark zusammenhängender Teilgraph**: Ein [[Gerichtete Graphen|gerichteter Teilgraph]] ist stark zusammenhängend, wenn es von jedem Knoten verbindende Pfade in beide Richtungen gibt
	-> Atomare Knoten bilden auch *stark zusammenhängende Zusammenhangskomponenten*
- **Schwach zusammenhängender Teilgraph:** Ein gerichteter Graph ist schwach zusammenhängend, wenn der dazugehörige [[Ungerichteter Graph|ungerichtete Graph]] *zusammenhängend* ist und er nicht erweitert werden kann
^1658939265058
