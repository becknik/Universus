---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
complete: true
aliases: Untervektorräume
linter-yaml-title-alias: Untervektorräume
date: 2022-11-13
mod-date: 2022-11-13
---

# Untervektorräume

## Definition: #fc
- Sei $V$ ein $K$-[[Vektorräume|Vektorraum]], dann ist $U\subseteq V,U\neq\emptyset$ ein *Untervektorraum* von $V$, wenn folgende Bedingungen erfüllt sind:
	1. Abgeschlossenheit unter Addition: $\forall$ *Vektoren* $u,v\in U:u+v\in U$
	2. Abgeschlossenheit unter Multiplikation: $\forall v\in U\wedge\forall$ *Körperelemente* $\lambda\in K:\lambda u\in U$
^1668378392544

## Eigenschaften #fc
- $U$ ist ein Vektorraum $\Leftrightarrow$ $U$ ist ein [[Vektorräume|Vektorraum]] mit auf die Teilmenge eingeschränkter *Vektoraddition* und *Skalarmultiplikation*
- $\{0\}\subseteq V$ ist der kleinste Untervektorraum für jeden Vektorraum $V$
	-> Bei $V:=\{v\}$ durch die zweite Eigenschaft von Untervektorräumen $v\cdot0=0$ gelten muss
^1668378881394

### Vereinigung: #fc
- Sei $V$ ein [[Vektorräume|Vektorraum]] und $\{U_j\mid j\in J\}$ eine Menge von *Untervektorräumen* von $V$, dann ist $$\bigcap_{j\in J}U_j$$ wieder ein Untervektorraum von $V$
^1668379061495

## Beispiele
- Für $V:=\mathbb{R}^3$ ist die $xy$-Ebene $U:=\{(x,y,0)\mid x,y\in\mathbb{R}\}$ ein Unterraum
	-> Ist nicht-leer und abgeschlossen unter Addition und Multiplikation mit beliebigen Skalaren
- Für $V:=\mathbb{R}^2$ ist jede Gerade, die durch den Ursprung verläuft ein Unterraum
