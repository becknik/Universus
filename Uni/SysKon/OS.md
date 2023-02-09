---
tags: uni practical-cs syskon os abstraction
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - OS
  - Betriebssystem
  - Kernel
  - monolithisch
  - micro-Kernel
  - Ring-0
  - Ring-2
  - Ring-3
linter-yaml-title-alias: OS
date-of-creation: 2022-11-12
mod-date: 2023-01-03
---

# OS

## Aufgaben
- Auswertung von [[Betriebssystem/Funktionen/System Calls|System Calls]]
- [[Scheduling]]
	→ ([[Betriebssystem/Echtzeitfähigkeit|Echtzeitfähigkeit]])
- [[Betriebssystem/Prozesse/Prozesswechsel|Prozesswechsel]]
- Speicherverwaltung
- …

## Eigenschaften des Kernels #fc
- Beinhaltet die am meisten verwendeten OS-Funktionalitäten
	→ Befindet sich im Hauptspeicher
- Enthält die zentralsten Funktionen:
	- Hardware-Schnittstelle
	- [[Betriebssystem/Prozess|Prozess]]-[[Betriebssystem/Scheduling|Scheduling]]
	- Speicherverwaltung
	- [[Betriebssystem/Funktionen/Message Passing Interface|Interprozesskommunikation]]
^1668081294563

## Hierarchie #fc
- Ring 0: [[#Kernel Mode (3) fc|OS-Kernel]]
- Ring 1
- Ring 2: Hier können Treiber laufen
- Ring 3: Anwendungen
	→ Kommunizieren über [[Betriebssystem/Funktionen/System Calls|System Calls]]
^1668285780152

## Organisation

### Monolithisch #fc
→ Die heute vorherrschende [[#Kernel Mode (3) fc|OS-Kernel]]-Typ
- Zusammengesetzt aus einer Menge von Prozeduren, die sich gegenseitig aufrufen können
- Teilfunktion sind in Kernel-Module ausgelagert
	→ Bessere Wartbarkeit, Erweiterbarkeit, kleiner Kern & Konfiguration zur Laufzeit
	→ Module führen im Kernel-Modus/ *Ring-0* aus
^1668285780154

### Micro Kernel #fc
- Ein sehr kleiner haupt-Kernel, bestehend aus…
	- …Prozessmanagement
	- …I/O- und [[Unterbrechungen|UBR]]-Verwaltung
	- …[[Scheduling]]
	- …Einfaches Speicher Management
→[[#Kernel Mode (3) fc|OS-Kernel]] lässt sich gut verifizieren, da er wenig Code umfasst
- Viele essentielle Dienste laufen im Anwendungs-Modus (Ring-3)
	→ Gerätetreiber, Dateisysteme, Virtueller Speicher, Window Manager, Sicherheitsdienste
- Prinzip hat sich (z.B. durch die Auslagerung von Grafikkarten-Treibern in Ring-2) auch auf monolitische Kernels übertragen
^1668285770227

## Instruction Execution Modes

### Kernel Mode (3) #fc
- Uneingeschränkter Zugriff auf Hardware
- Verwaltung von Prozesses ([[Prozess|Prozess-Management]])
- [[Unterbrechungen|Unterbrechungs-Routinen]] über [[Funktionen/System Calls|System Calls]]
^1668285788401

### User Mode #fc
- Kein direkter Zugriff auf *Hardware* und *unbefugte Adressräume* möglich
	→ Für den Zugriff auf Hardware ist ein Schnittstelle zwischen Anwendung und OS nötig
- Speicherschutz ist aktiv, der jeden [[Prozess]] einen privaten Adressraum zusichert
	→ Bei unerlaubten Zugriffen:
	Memory Protection/ Management Unit $\to$ [[OS]] $\to$ Segmentation Fault [[Unterbrechungen|Interrupt]] $\to$ Prozess terminiert
^1672676940799
