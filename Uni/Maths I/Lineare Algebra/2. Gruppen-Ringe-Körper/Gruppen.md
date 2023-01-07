---
tags: uni maths maths-1
cards-deck: Uni::Courses::Maths-I
completed: true
aliases:
  - Gruppen
  - Gruppenaxiome
  - abelsche Gruppe
  - symmetrische Gruppe
  - Untergruppen
linter-yaml-title-alias: Gruppen
date-of-creation: 2022-10-27
mod-date: 2022-11-02
---

# Gruppen

## Definition #fc
- Sei $G$ eine [[../1. Logik-Mengenlehre-Relationen/Mengenlehre|Menge]] mit einer Verknüpfung $G\times G\rightarrow G, (a,b)\mapsto a\ast b$ heißt Gruppe, wenn sie die *Gruppenaxiome* erfüllt:
	1. *Assoziativität*: $\forall a,b\in G: (a\ast b)\ast c=a\ast (b\ast c)$
		 → "unabhängig von der Reihenfolge der Rechenoperationen"
	2. Es existiert ein eindeutig bestimmtes *neutrales Element*: $e\in G:a\ast e=e\ast a=a$
	3. $\forall a\in G\exists b\in G:a\ast b=b\ast a=e$
		 → $(a\ast b)\ast(b'\ast a')=a\ast(b\ast b')\ast a'=(a\ast e)\ast a'=a\ast a'=e$
		 → Man schreibt $b$ dann auch als $a^{-1}$ oder $a'$
^1666884356965

### Untergruppen #fc
- Eine Teilmenge $H\subseteq G$ wird als Untergruppe von $G$ bezeichnet, wenn sie
	1. Abgeschlossenheit unter *Gruppenverknüpfung*: $\forall a,b\in H:a\ast b\in H$
	2. Abgeschlossenheit unter *Inversenbildung*: $\forall a\in H:a^{-1}\in H$
		 → Hieraus folgt, dass $e\in H,$ da $a\ast a^{-1}=e$
- *Triviale Untergruppe*: $\{e\}\subseteq G$
- *Echte Untergruppe*: Eine Gruppe $H\subsetneq G$
^1667208549578

### Abelsche/ Kommutative Gruppe #fc
- Zusätzlich zu den *Gruppenaxiomen* muss gelten:
	- *Kommutativität*: $\forall a,b\in G:a\ast b=b\ast a$
^1666884360854
