---
tags: uni practical-cs syskon distributed-systems
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Message Queues
  - Eventually Consistency
linter-yaml-title-alias: Message Queues
date-of-creation: 2023-01-06
mod-date: 2023-01-06
---

# Message Queues
→ [[../../Betriebssystem/Funktionen/Message Passing Interface|Interprozesskommunikation]]

## Funktionsweise #fc
- Verwendung von [[../../../DSA/Datenstrukturen/Queue|Queues]] zum Austausch von Nachrichten zwischen Prozessen
	→ Asynchrone Entkopplung der Kommunikation mit Queues als Zwischenglieder
- Die Queues dienen als *persistent speichernde* Datenbanken für Nachrichten
^1673097739212

## Eigenschaften
- "Aber: Nachrichtenabstraktion – Bruch mit lokaler Programmstruktur"
- Anwendungsbeispiel: Sicherstellung von Konsistenz bei verteilter Koordination (*Eventually Consistency*)
- Anwendungsbeispiel Banking:
	- Tagsüber werden die Queues mit Buchungen befüllt
	- Nachts werden die Transaktionen durch die Leerung der Warteschlangen durchgeführt
