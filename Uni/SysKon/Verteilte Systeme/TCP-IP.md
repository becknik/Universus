---
tags: uni practical-cs syskon distributed-systems networking
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - TCP-IP
  - TCP/IP
linter-yaml-title-alias: TCP-IP
date-of-creation: 2023-01-06
mod-date: 2023-01-06
---

# TCP-IP

## Eigenschaften
- Kam als Architektur des *ARPERNETs* mit 4 Schichten zum Einsatz
- Realisiert keine standardisierte API, [[Sockets]] sind allerdings weit verbreitet

## Schichten #fc
- 4. Application (Telnet, FTP, SMTP, DNS, etc.)
- 3. Transport ([[Protokolle/TCP|TCP]]/ [[Protokolle/UDP|UDP]])
- 2. Internet (= [[OSI Referenzmodell|OSI]] Network Layer)
- 1. Host-to-network (= OSI Physical & Data Link Layer)
^1673037102771

## Kritik
- Es wird nicht zwischen Dienst, Schnittstelle & Protokoll unterschieden
- Es ist kein allgemeines Modell
	→ Die Implementierung als Architektur des ARPERNET existierte zuerst, dann folgte das Modell
- Host-to-Network "Layer" ist nicht wirklich eine Schicht
- Protokolle sind kein und tief verwurzelt, was sie schwer ersetzbar macht
	→ Kein Modell, sondern eher ein Protokoll
