---
tags: uni dsa practical-cs tree indexstruct
cards-deck: Uni::Courses::DSA
completed: true
aliases: B-Baum
linter-yaml-title-alias: B-Baum
date-of-creation: 2022-07-22
mod-date: 2022-09-10
---

# B-Baum

## Eigenschaften: #fc
- Wurden von Bayer und McCreight entworfen
- **B-Baum-Kriterium**: Für jede **Seite** $v_i \in V \setminus \{v_0\}$ muss $m \leq |Schlüsselwerte~\in v_i| \leq 2m$ gelten
	→ Jede *Seite* muss $i+1$ Nachfolger haben
	→ $m$ = Maintaince-Wert/ *Ordnung* des B-Baums
- Die *Baumhöhe* von B-Bäumen ist vollständig ausgeglichen
	→ Die Anzahl der *Verzeigungen variiert* hingegen
^1652806311892

## Einfügen: #fc
- Eine geeignete Blattseite wird gesucht
	→ Das Element wird *zuerst* an der Stelle *eingefügt* und dann wird das B-Baum-Kriterium ausgeglichen[^1]
- Ein *Überlauf* wird durch das *Bottom-Up* hochziehen vom abgerundeten *mittleren Schlüsselelement* behandelt
	→ Der Baum nimmt zur Wurzel hin zu, bis er dort einen Split durchführen muss
^1652806754246

## Löschen: #fc
- Suche das zu löschende Element…
- Wenn das zu löschend Element auf einer Blattseite liegt:
	- Gegebenenfalls den *Unterlauf* behandeln
- Wenn das zu löschende Element nicht auf einer Blattseite liegt:
	- Das gelöschte Element wird durch den [[Traversierung|Inorder Vorgänger]] (=nächstkleinere Element) wird von einer Blattseite ersetzt
	- Gegebenenfalls muss hier der *Unterlauf* behandelt werden
^1652806896817

## Unterlaufbehandlung: #fc
- "*Durchtauschen*": Das äußerste Element einer mindestens $m+1$-elementigen Nachbarseite des selben Niveaus steigt zur Elternseite auf
	→ Das vorherige Element der Elternseite wird zu einem anderen Knoten verdrängt
	→ Kann über eine Reihe von Seiten fortgesetzt werden
- "*Zusammenlegen*": Der aktuelle Knoten wird mit einem höchstens $m$-elementigen Knoten auf demselben Niveau und dem obsoleten Schlüsselelement der Elternseite zusammengefügt
	→ Kann sich rekursiv auf ein höheres Niveau fortpflanzen
^1662497235724

## Anwendung: #fc
- Weisen eine Hohe Anzahl an Schlüsselwerten auf
	→ Die Anzahl von lesenden Seitenzugriffen ist mit $\log_mn$ gering
	→ Eigenen sich zum Einsatz auf Medien mit einer großen Menge von persistenten gehaltenen Daten
- Kommen in Dateiensystemen wie btrfs, ext4, HFS oder NTFS
	→ z.B. bei einer praxisnahen Seitengröße von 4kB mit ca. 32 Byte pro Schlüssel und 8 Byte pro Referenz mit $m \approx 50$ sind bei 10⁸ Elementen nur etwa 4-5 Block-Zugriffe notwendig
- Werden in Datenbanksystemen wie SQLite, Oracle oder DB2 verwendet
^1652807320238

[^1]: Sandro Speth bei einer Hörsaal-Übung
