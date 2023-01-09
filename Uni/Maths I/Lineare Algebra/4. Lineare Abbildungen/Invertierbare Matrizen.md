---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Invertierbare |Matrizen
  - invertierbar
  - Inverse
linter-yaml-title-alias: Invertierbare |Matrizen
date-of-creation: 2023-01-08
mod-date: 2023-01-09
---

# Invertierbare [[../2. Gruppen-Ringe-Körper/Matrizen|Matrizen]]

## Definition #fc
- Eine [[../2. Gruppen-Ringe-Körper/Matrizen|Matrix]] heißt invertierbar, wenn sie die [[Darstellende Matrizen#Definition fc|darstellende Matrix]] einer *bijektiven* Abbildung ist
- Die Darstellende Matrix ihrer Umkehrabbildung wird als $A^{-1}$ notiert und heißt *Inverse von A* oder *inverse Matrix*
> Siehe auch: [[../5. Lineare Gleichungssysteme/Inversen-Bildung#Funktionsweise fc|Inversen-Bildung]]
^1673214301939

## Eigenschaften #fc
- Nur quadratische [[../2. Gruppen-Ringe-Körper/Matrizen|Matrizen]] können invertierbar sein
- Aus [[Lineare Abbildungen#Satz 4.3.5|Satz 4.3.5|]] folgt, dass für eine invertierbare Matrix stehts $AA^{-1}=A^{-1}A=E$ gilt
- Seien $A,B\in M_n(K)$ und $A,B$ invertierbar, dann sind auch $AB, A^{-1}$ invertierbar und es gilt $(AB)^{-1}=A^{-1}B^{-1}$ und $(A^{-1})^{-1}=A$
^1673214301948

## Allgemeine Lineare Gruppe #fc
- Die [[../1. Logik-Mengenlehre-Relationen/Mengenlehre|Menge]] $GL_n(K):=\{A\in M_n(K)\mid A\text{ ist invertierbar}\}$ ist eine [[../2. Gruppen-Ringe-Körper/Gruppen#Definition fc|Gruppe]] mit der [[../2. Gruppen-Ringe-Körper/Matrizen#Produkt fc|Matrizenmultiplikation]] mit $E_n$ als *neutrales Element*
^1673214301951
