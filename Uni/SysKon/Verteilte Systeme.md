---
tags: uni practical-cs syskon distributed-systems
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Verteilte Systeme
linter-yaml-title-alias: Verteilte Systeme
date-of-creation: 2023-01-05
mod-date: 2023-01-06
---

# Verteilte Systeme

## Definitionen
- “A distributed system is a collection of independent computers that appear to the users of the system as a single computer.” ~ Tanenbaum, van Renesse
- “A distributed system consists of a collection of autonomous computers linked by a computer network and equipped with distributed systems software” ~ Courlouris, Dollimore, Kindberg
- "\[…\] A system in which I cannot get any work done because some machine that I have never heard of has crashed." ~ Leslie Lamport

## Definition #fc
- Eine Menge von autonomen, inhomogenen Computer-Systemen (=*Knoten*), die über ein Netzwerk (=*Kanten*) miteinander verbunden sind und dem Nutzer gegenüber systematisch agieren
- *Kanten*: Bestehen aus verwendeten Medien (IEEE 802.11, Bluetooth, Ethernet, etc.) und den zugehörigen Protokollen ([[Verteilte Systeme/Protokolle/TCP|TCP]], [[Verteilte Systeme/Protokolle/UDP|UDP]], X.25, etc.)
- Es existiert kein gemeinsamer Speicher zwischen den Knoten
^1668080764562

## Eigenschaften (3) #fc
- Es existieren Fehlerpunkte und Bottlenecks
- Sind heterogen bezüglich der Netzwerkarten und -Knoten
- Verteilte Systeme haben keine globale Ansicht und Zeit
	→ Zeitliche Annahmen zur Befehlsordnung ist aufgrund von der *Heterogenität der Rechnersysteme* und *variierender Übertragungszeit* von Nachrichten kaum treffbar
^1667834439570

## Anforderungen
- Unterschiedliche Nutzungsarten
	→ Arbeitsauslastung, verfügbare Ressourcen, Dienstqualitätsanforderungen, etc.
- Systemanforderungen
	→ Heterogenität, unterschiedliche Größen
- Interne Probleme
	→ Nicht synchronisierte Uhren, wiedersprüchliche Datenzugriffe, Hardware-/Softwarefehler
- Externe Bedrohungen

## Designaspekte

### Architekturmodell #fc
- Definiert die *Struktur* verteilter Systeme mit verschiedenen Komponenten
- Abstrahiert die Funktionen einzelner Komponenten unter Berücksichtigung deren…
	- Platzierung im Netz
		→ Wird zur Findung einer Daten- & Workloadverteilung verwendet
	- Zusammenhänge inklusive Rollen und Kommunikationsmuster
 - Beispiele: [[Verteilte Systeme/Architektur/Multi-Tier|Multi-Tier]], [[Verteilte Systeme/Architektur/Peer-to-Peer|Peer-to-Peer]]
^1673030840610

### Interaktionsmodell für Prozesse #fc
- Bestehen aus Rollen (*abstrakte Einheiten*) und Interaktionen/ Beziehungen
	→ Zugewiesene Rollen bestimmen den Kommunikationspartner
	→ Interaktion definiert die ausgetauschten Daten und Synchronisationsmuster
- Durch die Zuordnung von *Computer-Ressourcen* werden aus Modellen Architekturen
	→ z.B. Aus Client-Server Architektur für Web-Clients & -Server
- Beispiele: [[Verteilte Systeme/Verarbeitungsmodelle/Client-Server|Client-Server]], [[Verteilte Systeme/Verarbeitungsmodelle/Producer-Consumer|Producer-Consumer]], [[Verteilte Systeme/Verarbeitungsmodelle/Pipeline|Pipeline]]
^1673030840613
