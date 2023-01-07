---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Nebenläufigkeit
linter-yaml-title-alias: Nebenläufigkeit
date-of-creation: 2022-10-24
mod-date: 2022-10-31
---

# Nebenläufigkeit

## Definitionen
- Die Eigenschaften eines Systems verschiedene Aktivitäten gleichzeitig ausführen zu können
	→ Keine kausale Abhängigkeiten zwischen Aktivitäten
- *Nebenläufiges Programm* ::: Eine Menge sequenzieller Programme, die parallel ausgeführt werden können ^1667421522470
- *Parallelität*: Echt parallel
- *Nebenläufig*: [[Systemarchitekturen|Quasi-Parallelität]]
	→ Nützliche Abstraktion

## Vorteile
- *Verbesserter Durchsatz*: Die potentielle gesamte Kapazität kann genutzt werden
	→ Auch bei Einprozessorsystemen lässt sich durch [[Systemarchitekturen|quasi-Parallelität]] der Durchsatz erhöhen

## Herausforderungen #fc
- Eine fehlerfreie Kommunikation und Synchronisation zwischen Prozessen
	→ "Kinokarten-Problem"
- Entstandene Probleme sind oft situations- und zeitabhängig und daher schwer zu reproduzieren
^1666630985565

### Race Conditions #fc
- Bei gleichzeitigen Starten von $p,q$ hängt das Ergebnis einer Berechnung vom zeitlichen Verhalten der Operationen ab
```
Procedure p:
	temp < n;
	n < temp + 10
Procedure q:
	temp < n;
	n < temp + 100
```
^1666631339162

### Deadlocks #fc
- Eine Menge von Prozessoren blockieren sich zyklisch gegenseitig
```
Procedure p:
	wantp < true;
	await wantq = false;
	temp < n;
	n < temp + 10;
	wantp < false
Procedure q:
	wantq < true;
	await wantp = false;
	temp < n;
	n < temp + 100;
	wantq < false
```
^1666631339165

### Lost-Update-Problem #fc
- Mehrere Prozesse schreiben "gleichzeitig" ein Update in einen Zustandsspeicher
	→ Das Update des zufällig letzten Prozesses bestehen bleibt bestehen, das andere geht verloren
^1667421610647

## Lösungen

### Atomic Road Modify Unit Method #fc
- Es wird direkt nach der *Lese-Bestätigung* geschrieben
- Man verlässt sich auf (Hardware-beschleunigte) atomare Schreib-Operationen
	→ Die Platform-Unabhängigkeit ist nicht garantiert
^1666630985567
