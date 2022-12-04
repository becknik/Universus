---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - Unterbrechungen
  - UBR
  - Interrupt
  - Hardware-Interrupt
  - Software-Interrupt
  - Exception
  - Ausnahme
linter-yaml-title-alias: Unterbrechungen
date: 2022-10-31
mod-date: 2022-11-12
---

# Unterbrechungen

## Entstehen: #fc
- … -> I/O-Controller -> UBR-Controller -> UBR -> I/O über Systembus -> …
	-> Ermöglichen Systemsoftware auf Hardwareebene Kontrolle über Ressourcen:
^1667815867540

## Erkennung: #fc
- Der Prozessor überprüft nach jeder Ausführung eines atomaren Befehls, ob eine UBR vorliegt
	- Wenn UBR deaktiviert sind oder keine UBR vorliegt, wird direkt der nächste Befehl ausgeführt
^1668275069121

## Behandlung: #fc
1. Beende *Ausführungszyklus*: Aktueller Befehl wird zu Ende ausgeführt
2. Speichere [[Prozess|Zustand]] des Prozesses ([[../../Ro I/RISC-V/Problem Counter|Problem Counter]], CPU-Status-Word (=Flags)) auf dem [[../../Ro I/OS & Environment/Stack|Stack]] & sperre den Empfang von Interrupts
3. Speichere notwendige [[../../Ro I/RISC-V/Register|CPU-Register]] werden auf dem Stack
	 -> Bis hierher funktioniert alles in Hardware
4. Führe OS-intern spezifizierte UBR-Routine aus
5. Stelle CPU-Register wieder her
6. *Return from Interrupt* `RETI`: Stelle *PC*, *CSW* wieder her
	-> Die Reaktion auf Interrupts ist wieder freigegeben
7. Setze Prozess fort
^1668277642748

### Beispiel: UBR auf Arduino-Microcontroller
```
// Sichere Datensregister:
push r1
push r0
// Sichere CPU Status Word auf Stack
in r0, 0x3f
push r0

eor r1, r1
// Sichere Datenregister
push r24
push r25
...
// Wiederherstellung der gesicherten Register
pop r25
pop r24
...
pop r0
out 0x3f, r0
pop r0
pop r1
// Rücksprungadresse wird geladen
reti
```

## Varianten

### Hardware-/ Asynchrone-Interrupts: #fc
- Meint man, wenn man von Interrupts redet
- Treten asynchron zum Geschehen im Prozessor auf
- Beispiele:
	- Tastendruck auf der Tastatur
	- Festplatten
	- Netzwerk-Interface
^1668275400797

### Synchron (=Trap): #fc
- *Software-Interrupts*:
	- x86 Befehl: `INT`
	- Beipsiele:
		- [[Komponenten/System Calls]]
- *Ausnahmen*/ *Prozessor-Interrupts*:
	- Speicherzugriffsfehler
	- Teilen durch Null
^1668277657498

## Einsatzzwecke

### Allgemein: #fc
- Periodische Zeitgeber
- Treten bei Ereignissen wie Fehlern auf
- Ausführung von privilegierten Befehlen (nach UBRs):
	- Steuerung von Geräten
	- Zuweisung von Ressourcen an Prozesse
	- [[Prozesse/Prozesswechsel|Prozesswechsel]]
^1667234952585

### Durch OS: #fc
- Prozess-Ablaufkontrolle/ [[Scheduling]]
- [[Komponenten/System Calls]] durch Anwendungen
- Interaktion mit I/O-Geräten
- [[../../Ro I/Virtualisierung/Virtueller Speicher|Virtuelle]] Speicherverwaltung
- Fehlerbehandlung (=Ausführung von IHR)
^1668276382096

## Eigenschaften: #fc
- Die Überprüfung eine UBR erfolg über eine Leitung auf dem Mainboard mit Lo/Hi Kodierung
	-> Der Prozessor hat bei Detektion keine Ahnung woher die UBR kommt
- Das OS darf aufgrund von Privilegien maskierbare UBRs maskieren (=deaktivieren) oder demaskieren
	-> `CLI` - *clear interrupt*, `STI` - *set interrupts*
	-> Das gilt nicht für alle UBRs wie z.B. Hardware-Resets oder Speicherparitätsfehler
^1668277742872

## Vermeidung: #fc
- Polling-Modus: Ein *Protokoll*, durch das die CPU in einem festgelegten Intervall einer Menge von Geräte auf eine *Ready-Bit* überprüft[^1]
	-> Wenn das *Ready-Bits* gesetzt ist, stellt die CPU dem Gerät ein Dienst bereit
	-> Verschwendet CPU-Zyklen
- Um Prozesse abarbeiten zu können, werden Interrupts temporär abgestellt
- Da UBRs im Speziellen aufgrund der immer notwendigen *Zustands-Sicherung* des [[Prozess|Prozesses]] sehr problematisch werden können, deaktiviert man UBRs dort
	-> Beispiel: Echtzeitkritische Embends
^1668277742875

[^1]: [Baeldung](https://www.geeksforgeeks.org/difference-between-interrupt-and-polling/)
