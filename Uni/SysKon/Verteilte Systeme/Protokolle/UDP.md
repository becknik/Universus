---
tags: uni practical-cs syskon networking protocol
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - UDP
  - User Datagram Protocol
linter-yaml-title-alias: UDP
date-of-creation: 2023-01-05
mod-date: 2023-01-06
---

# UDP

## Bedeutung & Eigenschaften #fc
- *User Datagram Protocol*
	→ Auslieferung, Ankunftszeit und -Ordnung werden nicht vom Netzwerk garantiert
- Verbindungsloses (idempotentes) Protokoll
	→ Angefügter leichtgewichtiger Header besteht im wesentlichen aus der Port Nummer
	→ Analogon: Postsystem
- Datagramme versenden Pakete komplett, ohne Fragmentierung
	→ Für Fragmentierung bedarf es zusätzliche Arbeit
^1673037498021
