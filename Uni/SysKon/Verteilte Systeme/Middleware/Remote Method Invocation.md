---
tags: uni practical-cs syskon distributed-systems networking
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Remote Method Invocation
  - RMI
linter-yaml-title-alias: Remote Method Invocation
date-of-creation: 2023-01-07
mod-date: 2023-01-07
---

# Remote Method Invocation
→ [[Remote Procedure Call|RPC]]

## Service/ "Stub"-Implementierung #fc
→ [[Remote Procedure Call|RPC]] für in OOP
1. API Beschreibung durch Instruction Description Language (*IDL*) bereitstellen
	→ IDL-"Compiler" unterstützen allgemeine, schon bestehende [[../Verarbeitungsmodelle/Client-Server|Client-/ Service]]-spezifische Beschreibungen
2. API Beschreibung nach Zielsprache übersetzen
	 → Generiert Vorlage für den Service (=*Skeleton*) mit zugehörigen Service-Implementierungen
3. Hinzufügen von Client- & Service-Code (*Stub*)
	 → *Stub*: Funktionalität durch Nutzung des Dienstes (=lokaler [[Proxy]])
4. Kompalieren, Object Request Broker (*ORB*) binden & ausführen
	 → Der *ORB* stellt zu Laufzeit Anwendungstransparenz (=Konfiguration & Kommunikation) zwischen Anwendungsobjekten des *Stubs* und Skeleton des Services her
^1673052557196

## Fehlersemantiken (4) #fc
→ Werden i.d.R. nicht von der RMI-Implementierung in der Dokumentation erwähnt
- *Maybe*:
	- Der [[../Verarbeitungsmodelle/Client-Server|Klient]] versucht den Aufruf genau einmal zu versenden
	- Keine Deduplizierung, Antwort des [[../Verarbeitungsmodelle/Client-Server|Servers]] erfolgt nach der Bearbeitung
- *At least once*:
	- Der Klient sendet periodisch, bis ein Ergebnis vorliegt
	- Keine Deduplizierung, Antwort des Servers erfolgt nach Bearbeitung
- *At Most Once*:
	- Klient & Server sichern die Aufrufs-Kennung beim Ausgehen/ Empfang des/ der ersten Aufrufs/ Anfrage
		→ Server speichert Ergebnis zur Aufrufs-Kennung volatil zwischen
	- Beide Parteien senden Aufruf/ Ergebnis periodisch, bis das Ergebnis schließlich beim Klient vorliegt
		→ Klient löscht den Request und sendet daraufhin ein ACK zum Server
	- Nach Erhalt des ACKs löscht der Server Kennung & Ergebnis
- *Exactly Once*:
	- Identisch zu *At Most Once*, bis auf dass…
	- Auftragskennung & Antworten werden in non-volatile Memory zwischengespeichert
	- [[../../Atomizität|Atomizität]] beim Speichern & Verwerfen gilt
	- Das Auftreten eines Server-Fehlers vor dem Sichern die Interaktion zurücksetzt
	→ Der Empfänger stellt sicher, dass die Nachricht genau einmal zugestellt wird
^1673052557204

## Beispiele
- CORBA
- DOCM
- Java/RMI
