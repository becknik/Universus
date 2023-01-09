---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Untervektorräume
  - Untervektorraum
  - Unterraum
linter-yaml-title-alias: Untervektorräume
date-of-creation: 2022-11-13
mod-date: 2023-01-09
---

# Untervektorräume
→ [[Vektorräume]]

## Definition #fc
- Sei $V$ ein $K$-[[Vektorräume#Definition fc|Vektorraum]], dann ist $U\neq\emptyset,U\subseteq V$ ein *Untervektorraum* von $V$, wenn
	- … für $\forall u\in U$ die *Abgeschlossenheit* unter der Addition $+$ gilt
	- … und die Abgeschlossenheit der Skalarmultiplikation $K\times U\to U$ gilt
- [[Vektorräume#Definition fc|Forward Definition]]:
	1. *Addition*: $\forall u,v\in U:u+v\in U$
	2. *Skalarmultiplikation*: $\forall v\in U\wedge\forall$ *Körperelemente* $\lambda\in K:\lambda u\in U$
→ Elemente $u\in U$ werden auch wieder als *Vektoren* bezeichnet
^1668378392544

## Eigenschaften #fc
- $U$ ist ein Vektorraum $\Leftrightarrow$ $U$ ist ein [[Vektorräume#Definition fc|Vektorraum]] mit auf die Teilmenge eingeschränkter *Vektoraddition* und *Skalarmultiplikation*
- $\{0\}\subseteq V$ ist der kleinste Untervektorraum für jeden Vektorraum $V$
	→ Bei $V:=\{v\}$ durch die zweite Eigenschaft von Untervektorräumen $v\cdot0=0$ gelten muss
- Die Vereinigung von Untervektorräumen ist im Allgemeinen kein Untervektorraum
	→ Gegenbeispiel: Die $x$- und $y$-Achse von $\mathbb{R}^2:(1,0),(0,1)\in (x-\text{Achse}\cup y-\text{Achse}),$ $(1,0)+(0,1)\notin"$
^1668378881394

### Schnittmenge #fc #TODO
- Sei $V$ ein [[Vektorräume#Definition fc|Vektorraum]] und $\{U_j\mid j\in J\}$ eine Menge von *Untervektorräumen* von $V$, dann ist $$\bigcap_{j\in J}U_j$$ wieder ein Untervektorraum von $V$
^1668379061495

## Beispiele
- Für $V:=\mathbb{R}^3$ ist die $xy$-Ebene $U:=\{(x,y,0)\mid x,y\in\mathbb{R}\}$ ein Unterraum
	→ Ist nicht-leer und abgeschlossen unter Addition und Multiplikation mit beliebigen Skalaren
	→ Für $V:=\mathbb{R}^2$ ist jede Gerade, die durch den Ursprung verläuft ein Unterraum

## Summe

### Definition #fc
- Seien $U_1,U_2,\dots,U_k$ [[Untervektorräume#Definition fc|Untervektorräume]] von $V,$ dann heißt der Untervektorraum $$\sum_{i=1}^kU_i:=\text{span}(\bigcup_{i=1}^kU_i)$$ *die Summe* der gegebenen Untervektorräume
^1670170794931

## Direkte Summe

### Definition #fc
- Seien $U_1,U_2,\dots,U_k$ [[Untervektorräume]] vom [[Vektorräume|Vektorraum]] $V,$ dann heißt ein Untervektorraum $U$ *direkte Summe* von $U_1,U_2,\dots,U_k,$ wenn sich jeder Vektor aus $U$ #TODO auf *genau eine* Weise als Summe darstellen lässt: $$U\ni u_1+u_2+\dots+u_n,\quad u_1\in U_1,u_2\in U_2,\dots,u_n\in U_n$$
	→ Dann schreibt man $U=U_1\oplus U_2\oplus\dots\oplus U_k$
^1670171232260

### Eigenschaften - "Genau dann, wenn" #fc
- Seien $U_1,U_2$ [[Untervektorräume#Definition fc|Untervektorräume]] von $V$
- Die Summe $U_1+U_2=U$ ist genau dann direkt, wenn folgendes für $U$ gilt:
	1. $U=U_1+U_2$
	2. $U_1\cap U_2=\{0\}$
^1670171633788

### Beispiele
- Seien $U_1:=\text{span}((1,0,0)),U_2:=\text{span}((0,1,0)),U_3:=\text{span}((1,1,0)),$ dann ist $U_1+U_2+U_3=\{(x,y,z)\in\mathbb{R}^3\mid z=0\}$
