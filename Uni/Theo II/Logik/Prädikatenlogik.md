---
tags: uni theo-2 theoretical-cs logic
cards-deck: Uni::Courses::Theo-II
completed: true
aliases:
  - Prädikatenlogik
  - Logik erster Stufe
  - Logik zweiter Stufe
linter-yaml-title-alias: Prädikatenlogik
date-of-creation: 2022-08-05
mod-date: 2022-10-18
---

# Prädikatenlogik
→ Hierbei handelt es sich um [Prädikatenlogik 2. Stufe](https://de.wikipedia.org/wiki/Pr%C3%A4dikatenlogik_zweiter_Stufe)

## Definition
→ [[Belegung|Belegung]]

### Terme: #fc
- *Term* $=\{$Variablen, $f(t_1,\dots,t_k)$, wenn $t_1,\dots,t_k$ auch Terme sind$\}$
	→ $f^0_i \in$ Terme und wird Konstante genannt
^1661245610620

### Formeln: #fc
- Eine *Formel* der Prädikatenlogik besteht aus folgenden *Objekten*:
	- *Variablen*: $x_i \text{ mit Index } i\in \mathbb{N}_{\not0}$
	- *Prädikatsymbole*: $P^k_i \text{ mit Index } i \in \mathbb{N}_{\not0} \wedge \text{Stelligkeit } k \in \mathbb{N}_0$
		→ Zeigt Eigenschaften, Sortierungen oder relationale Begriffe an[^1]
		→ *Stelligkeit* = Anzahl der Elemente
	- *Funktionssymbolen*: $f^k_i \text{ mit Index } i \in \mathbb{N}_{\not0} \wedge \text{Stellenzahl } k \in \mathbb{N}_0$
^1664741938385

### Weitere Formel-Typen: #fc
- *Atomare Formel*: $P^k_i(t_1,\dots,t_k)$ und $t_1,\dots,t_k$ sind Terme
- Weitere *Formeln*:
	- [[Aussagenlogik|Aussagenlogische]] Operanden auf Formeln
	- $\exists/\forall xF$, wenn $F$ ist eine Formel und $x$ eine Variable ist
^1664741938389

### Struktur: #fc
- Eine *Struktur* gibt den benutzten Variablen, Funktions- und Prädikatsymbolen einen realen Sinn: $\mathcal{A}(U_\mathcal{A}, I_\mathcal{A})$
	→ Entspricht mit einer Interpretation einer [[Belegung]] der [[Aussagenlogik]]
- $U_\mathcal{A}$ = Die Menge aller *Individuen*, die auch *Universum* genannt wird
	→ $I_\mathcal{A}(x_i) \in U_\mathcal{A}$
	→ Für $U_\mathcal{A}$ wählt man häufig $\mathbb{N}$
- $I_\mathcal{A}$: Ordnet jedem *Prädikaten*- ($P^k_i$) und *Funktionssymbol* ($f^k_i$) ein *passendes Prädikat* und eine *passende Funktion* zu und ordnet jeder *benutzten Variable* $x_i$ ein Wert aus dem *Universum* $U_\mathcal{A}$ zu
	→ $f^k_i(t_1,\dots,t_k), \quad \forall t: \mathcal{A}(t_i) = u_i \in U_\mathcal{A} \Rightarrow \quad I_\mathcal{A}(f^k_i)(u_1, \dots, u_k) \in U_\mathcal{A}$
	→ $F = P(T_1,\dots,t_k)$ ist wahr ($\mathcal{A}(F) = 1$), falls $(\mathcal{A}(t_1),\dots,\mathcal{A}(t_k)) \in P^\mathcal{A}$
^1661245610622

### Wahrheitswerte von *Quantoren*: #fc
- $F = \forall xG: \mathcal{A}(F) = 1,$ falls $\forall \alpha \in U_\mathcal{A}: \mathcal{A}_{[x/\alpha]}(G)=1,$ sonst $\mathcal{A}(F)=0$
	→ $[x/\alpha] \triangleq x \leftarrow \alpha$
- $F=\exists xG: \mathcal{A}(F)=0,$ falls $\forall \alpha \in U_\mathcal{A}: \mathcal{A}_{[x/\alpha]}(G)=0,$ sonst $\mathcal{A}(F)=1$
	→ An Quantoren gebundene Variablen mit unterschiedlichen Bezeichnern müsse nicht auf unterschiedliche Individuen zeigen!
^1664741938392

### Belegung

#### Fachtermini: #fc
- $\mathcal{A}=(U_\mathcal{A}, I_\mathcal{A})$ ist zu $F$ **passend**: Alle in $F$ vorkommenden Variablen $x_i$, Prädikat- $P^k_i$ und Funktionssymbole $f^k_i$ kommen als *Variable* in $U_\mathcal{A}$ und als *$k$-stelliges Prädikat* oder*Funktion* in $I_\mathcal{A}$ vor
- $\mathcal{A}$ ist ein **Modell** zu $F$: $\mathcal{A}(F)=1 \Leftrightarrow F$ gilt in $A \Leftrightarrow A \vDash F$
- $F$ ist **erfüllbar**: $\exists$ Modell für $F$
- $F$ ist **allgemeingültig**: $\forall$ passende *Strukturen* zu $F$ sind *Modelle* für $F$
	→ Man schreibt auch: $\vDash F$ bzw. $\not \vDash F$, wenn $F$ nicht allgemeingültig ist
^1661245610625

### Fachtermini: #fc
- *Logik erster Stufe*: Alternativer Bezeichner für die Prädikatenlogik
- *Gebundene Variable*: Alle Vorkommen einer Variable sind an einen *Operator* verbunden
- *Freie Variable*: Die Variable ist nirgends ( oder doch mindestens einmal (?)) mit einem *Operator* versehen und somit frei wählbar[^2]
	→ Abhängig von der Klammerung und der damit Verbundenen Gültigkeit von Operanden wie Quantoren können auch beide Eigenschaften für eine Variable in einer Formel gelten
- *Geschlossene Formel*: Eine Formel ohne freie Variablen
- *Offene Formel*: Eine Formel mit mindestens einer freien Variable
- Aussage
- Matrix
^1661245610627

## Ein Beispiel: #fc
$F = \forall x \exists y \exists y'((P(x, y ) \wedge P(x, y' )) \wedge \forall z(\neg P(x, z) \vee (Q(y , z) \vee Q(y' , z)))$
Sei $G=(V,E)$ ein [[../../DSA/Graphen/Ungerichtete Graphen|ungerichteter Graph]]
- $U_\mathcal{A} = V$
- Kantenrelation: $I_\mathcal{A}(P) = P^\mathcal{A} = \{(u,v)~|~ u,v \in V \wedge \{u,v\} \in E\}$
- Gleichheit: $I_\mathcal{A}(Q) = Q^\mathcal{A} = \{(u,u) ~|~ u \in V\}$
→ Durch $\mathcal{A} = (U_\mathcal{A}, I_\mathcal{A})$ können nun allen Termen Werte aus $U_\mathcal{A}$ zugewiesen werden
^1661245610629

[^1]: [Wikipedia: Prädikatenlogik](https://de.wikipedia.org/wiki/Pr%C3%A4dikatenlogik#Pr%C3%A4dikate) (06.08.2022)
[^2]: [Wikipedia: Freie und gebundene Variable](https://de.wikipedia.org/wiki/Freie_Variable_und_gebundene_Variable)
