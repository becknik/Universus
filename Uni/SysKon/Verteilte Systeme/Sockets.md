---
tags: uni practical-cs syskon distributed-systems networking
cards-deck: Uni::Courses::SysKon
completed: true
aliases: Sockets
linter-yaml-title-alias: Sockets
date-of-creation: 2023-01-06
mod-date: 2023-01-06
---

# Sockets

## Eigenschaften ($\frac{9}{2}$) #fc
- Wurde das erste mal im Berkeley Software/ Standard Distribution (*BSD*) Unix System als API implementiert
	→ Spezifikation findet sich in UNIX man, nicht in ISO RFCs
- Ermöglicht eine Kommunikation von Anwendungen über das [[OSI Referenzmodell#4. Transport Layer|Layer 4]]
	→ Ist grundsätzlich Protokoll-unabhängig
- Weit verbreitete API für [[TCP-IP|TCP/IP]]
	→ Bieten verbindungslose und -orientierte Dienste an
- Stellen die Grundlage für viele [[../Middleware|Middleware-Systeme]] dar
- Bricht aufgrund der Übermittlung von Bytes die Programmiersprachen-interne Kodierung/ Abstraktion von Datentypen
^1673097875763

## Primitive (7) #fc
| Primitive | Bedeutung                                                                                                                |
| --------- | ------------------------------------------------------------------------------------------------------------------------ |
| Socket    | Erstellt einen [[../Betriebssystem/UNIX & Linux/UNIX-Philosophie\|UNIX]]-like File-Descriptor als Kommunikationsendpunkt |
| Bind      | Socket-File-Descriptor wird einer lokalen Adresse mit Port zugewiesen                                                    |
| Listen    | Server wartet auf Eingehen einer Verbindung                                                                              |
| Accept    | Blockiert den Klienten, bis eine Verbindungsanforderung eingeht                                                          |
| Connect   | Stellt eine Verbindung zum Socket her                                                                                    |
| Read      | Liste einen Strom von Daten                                                                                              |
| Write     | Schreibt einen Datenstrom                                                                                                |
| Close     | Schließt die Verbindung                                                                                                  |
- Hostende Programme benötigen zwei Socket-File-Deskriptoren
	→ Einer spezifiziert Adresse & Port des Hosts, der andere Socket wird zur Kommunikation mit dem Klienten benutzt
^1673037643295
