---
tags: uni practical-cs syskon distributed-systems networking
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Remote Procedure Call
  - RPC
linter-yaml-title-alias: Remote Procedure Call
date-of-creation: 2023-01-06
mod-date: 2023-01-07
---

# Remote Procedure Call
→ [[Remote Method Invocation|RMI]]

## Ablauf eines Funktionsaufrufs #fc
- Gegebene Methode wird durch einen Instruction Description Language (*IDL*) "Compiler" als Skeleton in den Client bzw. Server "reindeklariert"
	→ Siehe [[Remote Method Invocation#Service/ "Stub"-Implementierung fc|RMI]]
1. Methodenaufruf beim Client
2. *Marshalling*: Parameter werden mit Konvertierungsinformationen verpackt und transportiert
3. Vom "Compiler" eingefügte Endlos-Schleife auf der Server-Seite:
	- Erhalten der Anfrage → "Unmarshaling" → Prozeduraufruf (Call-by-Value/Reference) → "Marhsalling" → Senden des Ergebnisses an den Klient
	 → Call-by-Reference erfolgt in einem Remote-Adressraum ([[#Copy/Restore|Copy/Restore]])
^1673051886645

## Eigenschaften
- Zielt auf die Abgleichung der Abstraktion des lokalen Systems mit der eines entfernten System ab
	→ Soll Verbindungstransparenz für Aufruf, Binden, Ausführungsort, Migration, etc. herstellen
- Stellt eine synchrone Kommunikation zwischen [[../Verarbeitungsmodelle/Client-Server|Client & Server]] her
- Nutzt Dienstspezifizierung wie eine Interface Definition Language (*IDL*) oder schon bestehende API Definitionen
- *Feature-RMI*: Unterstützung vom Feature-Datentyp

## Parameterübergabe

### Copy/Restore
- (V.6, F.68 ff.)
- "Call by value zum Übergeben von Parametern und lokalen Verweisen auf diese Kopien verwendet"
- "Speichermanagement wird umständlich"
	- "Sperren oder Referenzzählung zur Vermeidung von Nebenwirkungen"
	- Weitergabe einer Referenz von Aufrufer → Aufgerufenen → Aufrufer und jeweils Freigabe der Referenz bei Weitergabe
- Kopieren auch von komplexen Datenstrukturen
	- "Verbieten?"
	- "Sende vollständige Kopie?"
	- "Daten nach Bedarf senden?"
	- "Speichermanagement? Datenzyklen?, etc."
