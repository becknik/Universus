---
tags: uni practical-cs syskon distributed-systems
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Multi-Tier
linter-yaml-title-alias: Multi-Tier
date-of-creation: 2023-01-06
mod-date: 2023-01-06
---

# Multi-Tier
→ [[../../Verteilte Systeme#Architekturmodell fc|Verteilte Systeme]]

## Eigenschaften #fc
- Ein Ansatz für ein *allgemeines Architekturmodell*
	- Anwendung werden unter Berücksichtigung der Funktionalitäten in größere Komponenten eingeteilt
	- [[#Aufteilung in allgemeine Komponenten fc|Aufteilung in allgemeine Komponenten]]
		 → Die Platzierung und Relevanz von Komponenten entscheidend für die Fehlertoleranz für Punkte, Leitungsängpässe
- Die unterschiedlichen Ebenen lassen sich an verschiedenen Punkten "anschneiden", um Daten auslesen zu können
^1673030847410

## Aufteilung in allgemeine Komponenten (3) #fc
1. Benutzerinteraktion/ Presentation
2. Verarbeitung
	 → Realisiert den dem jeweiligen Presentation-Layer zugrunde liegenden Workflow
3. Datenspeicherung
- 3 Ebenen sind populär, allerdings lassen sich auch mehr oder weniger Ebenen realisieren
^1673030847418

## Ebenen

### Präsentation
- Für die Interaktion mit den Benutzern zuständig
	→ Spielen eine Rolle in einem Workflow
	→ Absturz hat nur begrenzte Auswirkungen

### Verarbeitung
- Realisiert den der Anwendung zugrunde liegenden Workflow
	→ Bedient eine Reihe von Präsentationsebenen
- Repräsentiert typischerweise die Einheiten des Organisation
	→ Absturz wirkt sich auf das Geschäft einer Organisations-Abteilung aus

### Datenbank-/Speicherebene
- Für die persistente Datenspeicherung zuständig
- Typischerweise unternehmensweit
	→ Crash wirkt sich auf das Geschäft des gesamten Unternehmens aus

## Use Cases
- SAP Net Weaver
	- Presentation Layer: SAP GUIs
	- Application Layer: ABAP Application Server, die mit Message Servern in Verbindung stehen
	- Database Layer: Database management system
- Enterbrise JavaBeans (EJB)
	- Aufteilung in 3 vertikale, modulare Ebenen
		→ Die Präsentation-Ebene spaltet sich in Client & Server Sides
