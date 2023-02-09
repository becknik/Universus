---
tags: uni practical-cs syskon networking protocol
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - SMTP
  - Simple Mail Transfer Protocol
linter-yaml-title-alias: SMTP
date-of-creation: 2023-01-07
mod-date: 2023-01-07
---

# SMTP

## Eigenschaften
- Definition des Standards & Formats in *RFC 821* & *822*
- Wird zum Upload von zu versendenden Mails verwendet
- Plain Text Protocol

## Aufbau
- Envelope (für Message Transfer Server)
- Header (für Mail User Agents)
- Verwendung von zusätzlichen Headern (X-…)
- Leerzeile
- Nachrichtentext in 7-Bit ASCII

### Envelope & Header Parameter #fc
- To: Adresse des Empfängers
- Cc: Carbon Copy
- Bcc: Blind Carbon Copy
- From: Adresse des Senders/Mailing Liste
- Reply-To: Adresse für Antwort
	→ Antwort auf Kommentar der Mailing Liste
- Subject
^1673094258338

## Probleme #fc
- Eine Mail ohne Erweiterungen darf (in 7-Bit-ASCII) höchstens 64kB groß sein
	→ Wurde nach dem maximalen RAM eines Computers bei der Erstellung des Protokolls festgelegt
	→ Verbesserung: Extended SMTP
- Keine Authentifizierung
	→ Verbesserung: SMTP Auth
- Unendliche Schleifen zwischen Mail Transfer Agents durch DNS-Einträge (Mailstorms)
- Timeouts für die Zustellung
	→ Mails können schon vor der Zustellung sterben
- Verbesserung: Multipurpose Internet Mail Extensions
^1673094258345
