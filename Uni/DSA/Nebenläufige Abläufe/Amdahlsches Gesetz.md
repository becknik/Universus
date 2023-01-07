---
tags: uni dsa practical-cs parallel theorem
cards-deck: Uni::Courses::DSA
completed: true
aliases: Amdahlsches Gesetz
linter-yaml-title-alias: Amdahlsches Gesetz
date-of-creation: 2022-07-27
mod-date: 2022-09-10
---

# Amdahlsches Gesetz

## Definition: #fc
- Beschreibt eine obere Grenze für die Beschleunigung von [[../Nebenläufige Abläufe|nebenläufige Abläufe]] durch mehrere Prozessoren
- Die Gesamtlaufzeit auf einem Prozessor: $T=t_{\text{sequential}}+t_{\text{parallelizable}}$
$$S(n)=\frac{T}{t_s+\frac{t_p}{n}}$$
- Grenze: $S(n \rightarrow \infty) = \frac{T}{t_S}$
- Der Name kommt aus der Industrie
^1658939290853
