---
tags: uni theo-2 theoretical-cs abstraction computability automata
cards-deck: Uni::Courses::Theo-I
complete: true
aliases:
  - Turingmaschinen
  - Turingmaschine
  - TM
  - deterministische Turingmaschine
  - DTM
  - nichtdeterministische Turingmaschine
  - NTM
linter-yaml-title-alias: Turingmaschinen
date: 2022-08-06
mod-date: 2022-09-23
---

# Turingmaschinen

## Definition: #fc
- Definiert durch das berühmt berüchtigte *7-Tupel*:
$$M = (Z,\Sigma,\Gamma,\delta,z_0,\square,F)$$
- $Z:$ Die endliche, nicht-leere *Zustandsmenge*
- $\Sigma:$ Das endliche *Eingabealphabet*
	-> $\Sigma\cap Z=\emptyset$
- $\Gamma:$ Das endliche *Bandalphabet*, für das $\Gamma\cap\Sigma=\emptyset,\Sigma\subseteq\Gamma$ gelten muss
- Die [[Grundlegendes/Determinismus|deterministische]] *Überführungsfunktion* $\delta:Z\times\Gamma\rightarrow Z\times\Gamma\times\{L,R,N\}$
	-> Die [[Grundlegendes/Nichtdeterminismus|nichtdeterministische]] Geschmacksrichtung: $\delta:Z\times\Gamma\rightarrow\mathcal{P}(Z\times\Gamma\times\{L,R,N\})$
- $z_0:$ Der *Startzustand* $\in Z$
- $\square:$ Das *Leersymbol* $\in\Gamma\setminus\Sigma$
- $F:$ Die Menge der *akzeptierenden Endzustände* $\subseteq Z$
^1664633878761

## Varianten: #fc
- [[Grundlegendes/Determinismus|Determinismus]] / [[Grundlegendes/Nichtdeterminismus|Nichtdeterminismus]]
	-> Jede nichtdeterministische TM kann durch eine deterministische simuliert werden (durch [[../DSA/Graphen/Algorithmen/Breitensuche|Breitensuche]]/[[../DSA/Algorithmen/Muster/Backtracking|Backtracking]] im Berechnungsbaum)
- [[1. Typ - CSL/Linear beschränkte Turingmaschine|Linear beschränkte Turingmaschine]]
- [[../Theo II/Berechenbarkeit/Modelle/Mehrband-Turingmaschine|Mehrband-Turingmaschine]]
^1664633878801

## Eigenschaften: #fc
- Ein *möglichst eingeschränktes* Modell eines Rechners
	-> Je einfacher ein Modell, desto leichter lassen sich mit ihm *Beweise führen*
- Äquivalenzen von Turingmaschinen
	- TMs sind äquivalent zum [[Lambda-Kalkül]], [[../../Softwareentwicklung/Algorithmenmodelle/Makov-Algorithmen|Makov-Algorithmen]], [[../../Softwareentwicklung/Algorithmenmodelle/Registermaschinen|Registermaschinen]] (?), …
	- Jede TM lässt sich über ein [[../Theo II/Berechenbarkeit/Modelle/GOTO|GOTO-Programm]] simulieren (V.05 F.9.2 ff.)
	-> Diese Liste könnte man ewig so weiter führen (-> [[../Theo II/Berechenbarkeit/Church-Turing-These|Church'sche These]])
- Die Eigenschaft [[../../Softwareentwicklung/Algorithmenmodelle/Turing-vollständig|Turing-Vollständigkeit]] für logische Systeme und Programmiersprachen
- Wichtige Sprachklassen mit Beziehung zu TMs: [[../Theo II/Entscheidbarkeit|REC]] und [[../Theo II/Entscheidbarkeit/Rekursiv Aufzählbar|RE]]
^1664633878804

## Konfiguration: #fc
- Eine Konfiguration $k\in\Gamma^{Stern}\times Z\times\Gamma^{Stern}$
- *Konfigurationsübergang*: $\delta(z,a)=(z',a',X)$ mit $z,z'\in Z,a,a'\in\Gamma,X\in\{L,R,N\}$
	-> Die TM $M$ liest das Zeichen Bandalphabetszeichen $a$ im Zustand $z,$ substituiert es dann durch $a',$ wechselt in den Zustand $z'$ und liest in diesem dann das Bandalphabetszeichen *L*inks, *R*echts oder (*N:*) dasselbe nochmal
^1664633878806

### Notation für Ableitungen: #fc
- Die *Notation einer Konfiguration* einer TM $M$ lautet $\alpha z\beta$ mit $z\in Z,\alpha,\beta\in\Gamma^{Stern},M\curvearrowright\beta[0]$
	-> $M\curvearrowright\alpha[|\alpha|]$ ist genauso möglich, sieht aber vielleicht nicht ganz so schön aus
- Zur Darstellung von Zustandsüberführungen werden Relation '$\vdash$' verwendet
	-> $\vdash^{Stern}:$ Die reflexiver, transitiver Abschluss von $\vdash$
- Abhängig von $X\in\{R,L,N\}$ wird $\delta(z,b_1)=(z',c,X)$ dargestellt als:
	$a_1a_2\dots a_m~\textbf{z}~b_1b_2\dots b_n\quad\vdash\quad a_1a_2\dots a_mc~\textbf{z'}~b_2\dots b_n$ für $X=R$
	$a_1a_2\dots a_m~\textbf{z}~b_1b_2\dots b_n\quad\vdash\quad a_1a_2\dots a_{m-1}~\textbf{z'}~cb_1b_2\dots b_n$ für $X=L$
	$a_1a_2\dots a_m~\textbf{z}~b_1b_2\dots b_n\quad\vdash\quad a_1a_2\dots a_m~\textbf{z'}~b_1b_2\dots b_n$ für $X=N$
- Die von einer beliebigen TM *akzeptierte Sprache* ist definiert als
$$T(M)=\{x\in\Sigma^{Stern}\mid\textbf{z}_\textbf{0}x\vdash^{Stern}\alpha \textbf{z}_\textbf{f}\beta,\quad z_f\in F,\alpha,\beta\in\Gamma^{Stern}\text{ beliebig}\}$$
	-> Wenn $x\notin T(M):M$ *gerät in eine Schleife* ($z_0x\vdash^{Stern}\alpha\textbf{z}\beta\vdash^{Stern}\alpha\textbf{z}\beta$) oder *rechnet* eben *ohne Schleife endlos*
^1664633878808
