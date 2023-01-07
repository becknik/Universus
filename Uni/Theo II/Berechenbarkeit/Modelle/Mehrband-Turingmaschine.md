---
tags: uni theo-2 theoretical-cs computability
cards-deck: Uni::Courses::Theo-II
completed: true
aliases: Mehrband-Turingmaschine
date-of-creation: 2022-08-06
mod-date: 2022-08-20
linter-yaml-title-alias: Mehrband-Turingmaschine
---

# Mehrband-Turingmaschine

## Definition:
- Eine [[../../../Theo I/Turingmaschinen|Turingmaschine]] mit einem Schreib-/Lesekopf pro Band
- Übergangsfunktion $\delta: Z \times \Gamma^k \rightarrow Z \times \Gamma^k \times \{L,R,N\}^k$

## Eigenschaften:
- Zu jeder Mehrband-Turingmaschine $M$ gibt es eine 1-Band-TM $M'$, sodass $T(M) = T(M')$ oder beide TMs dieselbe Funktion berechnen
	→ Beweis über Definition einer 1-Band-TM mit mehreren Spuren durch $\Gamma_n=\Gamma' \times \Gamma' \text{mit} \Gamma'=\Gamma \cup \{\hat{\gamma}\mid\gamma \in \Gamma\},$ wobei $\hat{\gamma}$ die virtuelle Kopfposition simuliert
	→ Für jeden Schritt der Mehrband-TM muss die Simulation das komplette Eingabeband abfahren um die notwendigen Informationen zu sammeln und wieder zurückfahren, um die Konfiguration dementsprechend anzupassen

## Notation: #fc
- *Zustandsüberführung*: $M(i,k): \delta(z,c_1,\dots,c_{i-1},a,c_{i+1},\dots,c_k) =$
		$(z', c_1,\dots,c_{i-1},b,c_{i+1},\dots,c_k, N,\dots,N,y,N,\dots,N)$
	 → Wenn die Anzahl der Bänder $k$ uninteressant ist, dann schreibt man $M(i)$
- *Initialisierung*: $\text{Band } i := 0$
- *In- und Dekrement-Funktion*: $\text{Band }i:= \text{Band }i \pm 1/\text{Band}:= \text{Band} \pm 1$
- *Kopieren*: $\text{Band }i:= \text{Band }j$
	→ Vorausgesetzt, dass der Kopf immer wieder an den Anfang zurückgesetzt wird (=*disziplinierte* Verwendung)
- $M_1;M_2 = (M = (Z_1 \cup M_2, \Sigma, \Gamma_1 \cup \Gamma_2, \delta, z_1, \square, E_2)$ mit
			$\delta=\delta_1 \cup \delta_2 \cup \{(z,a,z_2,a,N)\mid z\in E_1, a\in \Gamma_1\})$ o.B.d.A $Z_1 \cap Z_2 = \emptyset$
- *Verzeigungen*/*Schleifen*: Mit $z \in Z$ als Bedingung beschriftete Pfeile
^1660502630780

## Beispiel: #fc
- Erzeugen der Konstante 5 auf Band 3, sowie 6 auf Band 5:
	- $M := (\text{Band } := \text{Band}+1)$
	- $\hat{M}:\quad \text{start} \rightarrow M \rightarrow M \rightarrow M \rightarrow M \rightarrow M \rightarrow \text{stop}$
	→ $\text{Band 3}:=0; \hat{M}(3); \text{Band 5}:=0; \hat{M}(5);M(5)$
^1664742270812
