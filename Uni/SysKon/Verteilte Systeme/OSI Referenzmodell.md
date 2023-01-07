---
tags: uni practical-cs syskon distributed-systems networking
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - OSI Referenzmodell
  - OSI
  - Open System Interconnections
  - Schicht X
  - Layer X
linter-yaml-title-alias: OSI Referenzmodell
date-of-creation: 2023-01-05
mod-date: 2023-01-07
---

# OSI Referenzmodell
→ [[Layered Networks]]

## Eigenschaften #fc
- OSI: *Open System Interconnections*
- Ging als Vorschlag der Internet Standard Organization (*ISO*) hervor zur klaren Standardisierung von…
	- Protokollen auf Schichten
	- Beziehungen der Schichten durch Schnittstellen & Dienste
- Implementierungen folgen aus Gründen der Performanz dem *Zero-Copy-Buffer*, das ein Array vorinitialisiert, das dann in Referenz-*Slices* an die nächste Schicht weitergegeben wird
	→ Bricht die theoretische Möglichkeit der nahtlosen Austauschbarkeit einzelner Protokolle
- Eignet sich vor Allem zur Didaktik, "By the book"-Implementierungen sind eher selten
^1673037047620

## Kritik
→ "Warum sich OSI nicht durchgesetzt hat"
- Kritik vom Prof. Becker: "Sie wollten kein Modell bauen, sondern ein Protokoll"
- Schlechtes Timing
- Schlechte Technologie
- Fehlerhafte Implementierung
- Schlechte Politik
- “a camel is a horse designed by a committee”
- Das [[TCP-IP|TCP/IP]] Referenzmodell existierte bereits

## Schichten

### 7. Application Layer
- Einheit des Austauschs: *APDU*
- Definiert die für die Anwendung relevanten Meldungen & Daten
	→ Interaktionsmuster

### 6. Presentation Layer
- Einheit des Austauschs: *PPDU*
- Definiert die Darstellungsweise & Repräsentation der Daten des Application-Layers und führt dementsprechende Transformationen durch
	→ [[../../Ro I/CPU/Endianess|Endianess]], Programmiersprachen-spezifische Kodierungen, XML

### 5. Session Layer
- Einheit des Austauschs: *SPDU*
- Verwaltet die Sitzungsstaten einzelner Verbindungen

### 4. Transport Layer
- Einheit des Austauschs: *TPDU*
- Ermöglicht Kommunikation zwischen Prozessen
- Beihaltet eine weitere Instanz der Flusskontrolle
- Verschiedene Servicetypen für verbindungslosen & -orientierten Transport mit unterschiedlicher Philosophie verfügbar
	→ [[TCP]], [[Protokolle/UDP|UDP]],[[QUIC]]

### 3. Network Layer
→ Verwendet ein internes Subnetz Host-Router Protokoll
- Einheit des Austauschs: *Packet*
- Ermöglicht die Kommunikation zwischen beliebigen Stationen über Adressierung
	→ Stellt das eigentliche Netzwerk bereit
- Best Effort Protocol

### 2. Data Link Layer
→ Verwendet ein internes Subnetz Host-Router Protokoll
- Einheit des Austauschs: *Frame*
- Verbindet zwei Stationen
- Zugang zum Übertragungsmedium (media access control *MAC*)
- Sicherungsschicht: Flusskontrolle, Fehlererkennung & Korrektur

### 1. Physical Layer
→ Verwendet ein internes Subnetz Host-Router Protokoll
- Einheit des Austauschs: *Bit*
- Verbindet zwei Stationen
- Kümmert sich um die Übertragung & den Austausch von physischen Signalen
