---
tags: uni practical-cs syskon os
cards-deck: Uni::Courses::SysKon
complete: true
aliases: OS-Struktur
linter-yaml-title-alias: OS-Struktur
date: 2022-11-10
mod-date: 2022-11-12
---

# OS-Struktur

## Modelle

### Monolithisch: #fc
-> Die heute vorherrschende [[../OS|Kernel]]-[[OS-Organisation|Organisation]]
- Zusammengesetzt aus einer Menge von Prozeduren, von alle sich gegenseitig aufrufen können
- Teilfunktion sind in Kernel-Module ausgelagert:
	-> Bessere Wartbarkeit, Erweiterbarkeit, kleiner Kern & Konfiguration zur Laufzeit
	-> Module führen im Kern-Modus aus
^1668285780154

### Micro Kernel: #fc
- Der (sehr kleine) Kern gesteht aus…
	- Prozessmanagement
	- I/O- und [[Unterbrechungen|UBR]]-Verwaltung
	- [[Scheduling]]
	- Einfaches Speicher Management
-> [[../OS|Kernel]] lässt sich gut verifizieren, da er wenig Code umfasst
- Viele essentielle Dienste im Benutzer-Modus
	-> Gerätetreiber, Dateisysteme, Virtueller Speicher, Window Manager, Sicherheitsdienste
^1668285770227

## Hierarchie: #fc
1. *Ring 0*: Der OS [[../OS|Kernel]] läuft hier
2. Ring 1
3. Ring 2: Hier können Treiber laufen
4. *RIng 3*: Anwendungen
^1668285780152
