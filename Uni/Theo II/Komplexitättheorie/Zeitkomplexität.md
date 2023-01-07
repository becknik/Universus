---
tags: uni theo-2 theoretical-cs complexity abstraction
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Zeitkomplexität
linter-yaml-title-alias: Zeitkomplexität
date-of-creation: 2022-07-09
mod-date: 2022-10-24
---

# Zeitkomplexität

## Definition: #fc
- $time_M: \Sigma \rightarrow \mathbb{N}$ ordnet einer [[../Berechenbarkeit/Modelle/Mehrband-Turingmaschine|deterministische Mehrband-Turingmaschine]] $M$ die Anzahl der Rechenschritte zu, die auf der Eingabe $x$ gemacht werden
	→ Die Verwendung von Merhband-TMs ergibt realistischere Komplexitätsfunktionen
- $\text{TIME}(f)$ oder $\text{TIME}(f(n))$ für eine Funktion $f: \mathbb{N} \rightarrow \mathbb{N}$ enthält alle Probleme A, für die eine TM M existiert mit $$T(M) = A\wedge\forall x: time_M(x) \leq f(|x|)$$
^1660502918255

## Beziehungen

### Klassen: #fc
→ Von oben nach unten $\subseteq/\subsetneq$
- [[Zeitklassen/NP|NP]] $= \bigcup_{\text{Polynom }p} NTIME(p)\mid coNP$
- $NP\cap coNP$
- [[Zeitklassen/P|P]] $:= \bigcup_{\text{Polynom }p}DTIME(p)$
	→ *P-NP-Problem*: Jeweils untereinander nicht sicher, ob $\subseteq$ oder $\subsetneq$
- [[Zeitklassen/TIME|NTIME]] $:=\bigcup_{g\in\mathcal{O}(f)}NTIME(g)=\bigcup_{c\in\mathbb{N}}NTIME(c\cdot f)$
- [[Zeitklassen/TIME|DTIME]] $:=\bigcup_{g\in\mathcal{O}(f)}DTIME(g)=\bigcup_{c\in\mathbb{N}}DTIME(c\cdot f)$
^1660502918263

### Intern: #fc
- Sei $f: \mathbb{N} \rightarrow \mathbb{N},$ dann gilt:
1. Falls $\exists \varepsilon > 0$ mit $\forall n:(1+\varepsilon)n\leq f(n)$, dann gilt:
$$DTIME(\mathcal{O}(f)) = DTIME(f)$$
2. Durch Anwendung von markierter Bandreduktion und Bandkompression gilt:
$$NTIME(\mathcal{O}(f)) = NTIME(f)$$
	→ Aber*: $DTIME(f(\mathcal{O}(n))\neq DTIME(f(n))$
3. Da $\exists P\in DTIME((1+\varepsilon)n):P\notin DTIME(n)$ gilt: $$DTIME(n) \neq DTIME(\mathcal{O}(n))$$
	→ Naiv: $DTIME(f)\subseteq DTIME_{1-Band}(f^2)$
^1660502918266

## Eigenschaften: #fc
- $DTIME$ ist gegen Komplement abgeschlossen, $NTIME$ nicht
^1664743565166

## Theoreme: #fc
- [[Zeitklassen/Satz von Hennie und Stearns|Satz von Hennie und Stearns]]
- [[Konstruierbarkeit|Zeitkonstruierbarkeit]]
- [[Hierarchiesätze|Zeithierarchiesatz]]
- [[Lückensatz von Borodin|Lückensatz von Borodin]]
- [[Translationssätze|Translationssatz für Zeitklassen]]
^1664743560144
