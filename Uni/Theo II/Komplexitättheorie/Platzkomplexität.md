---
tags: uni theo-2 theoretical-cs complexity abstraction
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Platzkomplexität
linter-yaml-title-alias: Platzkomplexität
date-of-creation: 2022-07-10
mod-date: 2022-10-24
---

# Platzkomplexität

## Definition: #fc
- $space_M: \Sigma^{Stern}\rightarrow\mathbb{N}$ ordnet einer [[../../Theo I/Turingmaschinen|DTM]] $M$ die Anzahl der maximal verwendeten Bandelemente auf einem Arbeitsband zu
- $A \in SPACE(f), f:\mathbb{N}\rightarrow\mathbb{N}$ bedeutet $$\exists T(M) = A \wedge \forall x: space_M(x) \leq f(|x|)$$
	→ Häufig ist die Schranke ein Polynom
- Bei *sub-linearen Platzklassen* geht man grundsätzlich von einem *separaten Eingabeband* aus, auf dem die Platzschranke nicht angewandt wird
	→ [[Platzklassen/Logspace-Transducer|Logspace-Transducer]]
^1660502877081

## Beziehungen

### Klassen: #fc
→ Von oben nach unten $\subseteq/\subsetneq$
- [[Platzklassen/PSPACE|PSPACE]] = $\text{IP}$
	→ [[Platzklassen/Satz von Savitch|Satz Von Savitch]]
- [[Platzklassen/SPACE|NSPACE]] $=\text{CSL}=\text{LBA}$
- [[Platzklassen/SPACE|DSPACE]]
- $\bigcup_{1\leq k}DSPACE(\log^kn) = \bigcup_{1\leq k}NSPACE(\log^kn)$
	→ [[Platzklassen/Satz von Savitch|Satz Von Savitch]]
- [[Platzklassen/NL|NL]]
- [[Platzklassen/L|L]]
^1660502877089

### Intern: #fc
- Sei $f: \mathbb{N} \rightarrow \mathbb{N},$ dann gilt:
1. DSPACE($O(f)$) = $DSPACE_{\text{1-Band}}(f)$
2. NSPACE($O(f)$) = $NSPACE_{\text{1-Band}}(f)$
^1660502877092

## Theoreme & Folgerungen: #fc
- [[Platzklassen/Satz von Savitch|Satz von Savitch]]
- [[Platzklassen/Satz von Immerman–Szelepcsényi|Satz von Immerman–Szelepcsényi]]
- Korollar aus der [[Platzklassen/Translationstechnik|Translationstechnik]]: $DSPACE(n)\subsetneq NSPACE(n)\Rightarrow L\subsetneq NL$
^1664743693685

## Referezen
- [[../../Theo I/1. Typ - CSL/Linear beschränkte Turingmaschine|LBA]] = [[../../Theo I/Typ-1|CSL]]
