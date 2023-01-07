---
tags: uni practical-cs syskon distributed-systems networking
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Client-Server
  - Klient-Server
  - Klient
  - Server
  - Service
linter-yaml-title-alias: Client-Server
date-of-creation: 2022-10-24
mod-date: 2023-01-07
---

# Client-Server

## Prinzip #fc
- Ein *Server* bietet einen *Dienst* einer unbekannten Anzahl von *Klienten* an
- Server selbst können Klienten von anderen Diensten sein, um auf anderen Servern/Knoten verteilte Daten oder Funktionen anzufordern
	→ Service be auf mehreren Knoten
	→ Zum Beispiel Datenbanken-Diensten
- Server *warten auf Anfragen* von Klienten, *verarbeiten* diese & senden das Ereignis zurück an den Klienten
- Ein *Klient* nutzt angebotene Dienste durch das *aktive* Senden von Anfragen
^1666630139937
