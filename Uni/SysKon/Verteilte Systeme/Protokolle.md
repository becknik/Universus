---
tags: uni practical-cs syskon abstraction distributed-systems networking
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Protokolle
linter-yaml-title-alias: Protokolle
date-of-creation: 2023-01-06
mod-date: 2023-01-07
---

# Protokolle

## Definition #fc
- Eine Kommunikationsvereinbarung (Nachrichten & Regeln) zwischen zwei Parteien des gleichen [[Layered Networks|Layer]] auf verschiedenen Maschinen
	→ *Nachrichten* = Inhalt der Interaktion, hängen vom Anwendungszweck ab
	→ *Regeln* = Beziehung zwischen Nachrichten
- Die Schnittstelle definiert welche *Service Primitive* der darüber liegenden Schicht angeboten wird
^1673037299696

## Protocol Stacks

### Eigenschaften #fc
- Es besteht eine klare Trennung zwischen generischen und anwendungsspezifischen Diensten
	→ Generisch: [[OSI Referenzmodell#3. Network Layer|OSI-Layer <4]]
	→ Anwendungsspezifisch: Datenkodierung, Kommunikationsmodell
- [[../OS|OSes]] bieten i.d.R. eine Abstraktionen bis einschließlich *Layer 4*
	→ Auswahl der des Servicetyps (*verbindungslos* oder *-orientiert*) bleibt beim Anwender
^1673037299703

### Dienstprimitive
| Primitiv   | Bedeutung                            |
| ---------- | ------------------------------------ |
| LISTEN     | Warten auf eingehende Verbindungen   |
| CONNECT    | Verbindungsaufbau mit wartenden Peer |
| RECEIVE    | Warten auf eingehende nachricht      |
| SEND       | Senden einer Nachricht zum Peer      |
| DISCONNECT | Beenden der Verbindung               |

## Instanzen
- [[OSI Referenzmodell#7. Application Layer|Application Layer:]]
	- [[Protokolle/Anwendungsschicht/HTTP|HTTP]]
	- [[Protokolle/Anwendungsschicht/SMTP|SMTP]]
- [[OSI Referenzmodell#4. Transport Layer|Transport Layer:]]
	- [[Protokolle/TCP|TCP]]
	- [[Protokolle/UDP|UDP]]
