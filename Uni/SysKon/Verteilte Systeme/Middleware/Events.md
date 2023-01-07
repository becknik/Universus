---
tags: uni practical-cs syskon distributed-systems networking
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Events
linter-yaml-title-alias: Events
date-of-creation: 2023-01-06
mod-date: 2023-01-07
---

# Events

## Prinzip #fc
- Informationen werden asynchron über Events ausgetauscht
- Synchronisationen der Informationen wird über (getaktetes) *pullen* vom oder *pushen* zum [[../Verarbeitungsmodelle/Producer-Consumer|Consumer]]
	→ Ein leichtgewichtiger, unidirektionaler Mechanismus für $1:n$ Kommunikation
	→ Siehe: [[Monitoring]], [[Push-Pull Modelle|Push-Pull Modelle]]
^1673090935837

## Eigenschaften
- Kommt bei der GUI-Entwicklung zum Einsatz
