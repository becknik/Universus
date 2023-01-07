---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Gruppenhomomorphismus
  - Kern
linter-yaml-title-alias: Gruppenhomomorphismus
date-of-creation: 2022-10-31
mod-date: 2022-11-07
---

# Gruppenhomomorphismus

## Definition #fc
- Eine Abbildung auf zwei [[Gruppen]] $F,G$ durch die [[../1. Logik-Mengenlehre-Relationen/Abbildungen|Abbildung]] $F:G\rightarrow H$ heißt *Gruppenhomomorphismus*, wenn $$\forall a,b\in G:\quad f(ab)=f(a)f(b)$$ gilt
^1667212708981

### Kern #fc
- Sei $f:G\rightarrow H$ ein *Gruppenhomomorphismus* und sei $e$ das neutrale Element in $H$, dann wird $$\text{ker}(f):=f^{-1}(\{e\})=\{g\in G\mid f(g)=e\}$$ als *Kern* von$f$ bezeichnet
^1667212712232

## Eigenschaften #fc
- Ein Gruppenhomomorphismus $f:G\rightarrow H$ bildet das neutrale Element von $G$ auf das neutrale Element von $H$ ab
- $ker(f)$ und $Bild(f)$ sind [[Gruppen|Untergruppen]] von $G$ bzw. $H$
^1667213271239
