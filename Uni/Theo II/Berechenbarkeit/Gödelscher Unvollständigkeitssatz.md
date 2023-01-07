---
tags: uni theo-2 theoretical-cs theorem
cards-deck: Uni::Courses::Theo-II
completed: false
aliases: Gödelscher Unvollständigkeitssatz
date-of-creation: 2022-08-09
mod-date: 2022-08-14
linter-yaml-title-alias: Gödelscher Unvollständigkeitssatz
---

# Gödelscher Unvollständigkeitssatz
!!! Es existieren 2

## Definiton: #fc
- Jedes (feste) [[Beweissysteme|Beweissystem]], das nur [[Wahre Arithmetische Formeln|wahre Formeln der Arithmetik]] beweist, muss *unvollständig* sein, wenn es korrekt ist
	→ Für ein Beweissystem $(B,F), F(B)\subseteq WA: Bew(B,F)\subsetneq WA$
	→ $Bew(B,F)=$ Bildmenge von $F$
	→ Die nicht beweisbaren Formeln sind dafür in anderen Beweissystemen beweisbar
- Jedes [[Modelle/WHILE|WHILE-Programm]] lässt sich über Formeln der ersten Stufe formulieren !!! Ist das wirklich so?
	→ Es lässt sich nicht entscheiden, ob eine solche Formel wahr ist oder nicht
- *Aussage*: Jedes Verhalten lässt sich als Formel beschreiben
	→ Das Verhalten jedes Programm lässt sich als durch [[../Logik/Prädikatenlogik|Prädikatenlogik]] über der verwendeten Datentypen ($\mathbb{N}$, Strings…) beschreiben
^1660502744058

### Formal:
- *Terme*:
	- $n\in\mathbb{N}_0$ ist ein Term
	- $\forall i\in\mathbb{N}:x_i$ ist ein Term
	- Wenn $t_1,t_2$ Terme sind, dann sind $(t_1+t_2)$ und $(t_1*t_2)$ Terme
- *Formeln*:
	- Wenn $t_1,t_2$ Terme sind, dann ist auch $(t_1=t_2)$ eine *atomare Formel*
	- $\wedge,\vee,\neg$ von Formeln sind Formeln
	- $\exists x_iF$ und $\forall x_iF$ sind Formeln
- Variablen sind *frei*, wenn vor ihnen an keiner Stelle ein Quantor steht
- Eine Formel $F$ ist wahr, wenn für alle passenden [[Logik/Belegung|Belegungen]] $\Phi:V\rightarrow\mathbb{N}$ gilt, dass $\Phi(F)$ wahr ist

## Semantische Interpretation:
- $\Phi:V=\{x_i\mid x\text{ kommt in } F \text{ vor }\}\rightarrow\mathbb{N}$
- $\Phi(n\in\mathbb{N})=n$
- $\Phi(x_i)$ wie oben definiert
- $\Phi(t_1+t_2)=\Phi(t_1)+\Phi(t_2)$
- $\Phi(t_1*t_2)=\Phi(t_1)\cdot\Phi(t_2)$
- $\Phi(t_1=t_2)$ ist wahr, wenn $\Phi(t_1)=\Phi(t_2)$ in $\mathbb{N}$ gilt
- [[Logik/Aussagenlogik|Aussagenlogische Verknüpfungen]]
- [[Logik/Prädikatenlogik|Prädikatenlogische Verknüpfungen]]
- Fehlt hier was !!!
