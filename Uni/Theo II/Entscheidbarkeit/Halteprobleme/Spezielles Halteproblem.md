---
tags: uni theo-2 theoretical-cs halteproblem
cards-deck: Uni::Courses::Theo-II
complete: true
aliases:
  - Spezielles Halteproblem
  - Selbstanwendungsproblem
  - K
linter-yaml-title-alias: Spezielles Halteproblem
date: 2022-07-03
mod-date: 2022-10-02
---

# Spezielles Halteproblem
-> [[Gödelisierung|Gödelisierung]]

## Definition #fc
$$K = \{w \in \{0, 1\}^{Stern}\mid M_w\text{ hält auf der Eingabe }w\}$$
- **Aussage**: *Hält ein Algorithmus in endlicher Zeit, wenn man ihm seinen eigenen Text übergibt?*
	-> Ein Compiler in [[../../../../Softwareentwicklung/Prog/Java|Java]] kann auch selber in Java programmiert sein
^1660502831481

### Beweis: $K$ ist nicht entscheidbar #fc
- $K$ entscheidbar $=\chi_K$ berechenbar $\Rightarrow \exists$ [[../../../Theo I/Turingmaschinen|TM]] $M$, die nach endlicher Zeit 1 ausgibt, wenn $M_w$ auf $w$ hält oder 0 ausgibt, wenn $M_w$ auf $w$ nicht hält
-> Konstruiere nun $M' = M_{w'}$:
```
INPUT w
REPEAT
	Simuliere M auf Input w
UNTIL M gibt 0 aus;
OUTPUT 1
```
- Zu zeigen: $w'\in K$, als auch $w'\notin K$ ist nicht möglich $\Rightarrow$ Widerspruch
- Angenommen, $w' \in K:$
	- $M$ gibt auf dem Input $w'$ nach endlicher Zeit eine 1 aus
	- Die Ausgabe von $M'=M_{w'}$ auf $w'$ ist undefiniert (-> Abbruchbedingung der Schleife)
	- $M' = M_{w'}$ hält nicht auf $w'$, also $w' \notin K\Rightarrow$Widerspruch
- Angenommen, $w' \notin K:$
	- $M$ gibt auf $w'$ nach endlicher Zeit eine 0 aus
	- $M'=M_{w'}$ gibt nach endlicher Zeit eine 1 aus
	- $w'\in K,$ also Widerspruch zur Annahme $w'\notin K$
- $K\text{ ist unentscheidbar }\quad\square$
^1664742856536

$\Uparrow$ Anschauliche Darstellung S.191[^1]

## Alternativer Beweis:[^1]
- Sei $x\in A^*$ ein *beliebiger Algorithmus* (bestehend aus Text), dessen berechnete Funktion mit $\varphi_x$ notiert wird
	-> Wenn $x$ nicht sinnvoll ist, dann ist $\varphi_x=\Omega$ die *nirgends definierte Funktion*
- Sei $f:A^*\rightarrow A^{Stern}$ eine partielle Funktion und $dom~f$ ihr definierter Urbereich ("domain")
- Die totale Funktion $h:A^*\rightarrow A^*,h(x)=\varepsilon,\text{ falls }x\in dom~\varphi_x,~\text{sonst beliebig }a\in A$ ist nicht [[../../Berechenbarkeit|berechenbar]]
	-> $\varepsilon,a\in A$ übernehmen hier die Aussagen `true` und `false`
- Unter der Annahme, $h(x)$ sei berechenbar, muss aufgrund der [[../../Berechenbarkeit/Church-Turing-These|Church-Turing-These]] auch $g:A^*\rightarrow A^*$ berechenbar sein mit $g(x)=\varphi_x(x)a,\text{ falls }h(x)=\varepsilon,~\text{sonst }\varepsilon$
	-> Aufgrund der Definition $\forall x\in A^*:g(x)\neq\varphi_x(x)$
	-> Da $g$ berechenbar ist, $\exists$ Algorithmus $y\in A^*$, der $g$ berechnet ($\equiv g=\varphi_y$)
$$\Rightarrow\varphi_y(y)=g(y)\neq\varphi_y(y)$$
- Dieser *Widerspruch* lässt sich nur lösen, indem man die Annahme aufgibt, dass $h$ berechenbar sei (was ein Diagonalbeweis (?) ist)

## Eigenschaften:
- Wird auch als "*Selbstanwendungsproblem*" bezeichnet

[^1]:Saake, G., Sattler, K.: Algorithmen und Datenstrukturen: Eine Einführung mit Java. 6. Auflage dpunkt-Verlag, 2021.
