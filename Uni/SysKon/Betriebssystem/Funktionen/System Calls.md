---
tags: uni practical-cs syskon os
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - System Calls
  - SysCall
  - Interrupt Service Routine
  - ISR
  - Interrupt Handler Routine
  - IHR
linter-yaml-title-alias: System Calls
date-of-creation: 2022-11-12
mod-date: 2023-01-02
---

# System Calls

## Funktionsweise #fc
- Anwendung ruft eine Funktion von `libc` auf
	→ Zum Beispiel: `open(sonst char *pathname, int flags)`
- Die Systembibliothek setzt die zugehörigen SysCall Parameter in [[../../../Ro I/CPU/X86_64|x86]]-CPU-[[../../../Ro I/RISC-V/Register|Registern]]
	→ Der Register `EAX` speichert die zum System Call passende Nummer
	→ Übrige Register: EBX*: `*pathname`, *ECX*: `flags`, *EDX*: `mode`
- Durch die Assembly Instruktion `INT _` wird ein [[../Unterbrechungen|Software-Interrupt]] ausgelöst
- Der Kernel findet die zur *SysCall-Nummer* passende *Interrupt Service Routine* & führt sie aus
- Das Ergebnis der *ISR* wird über `libc` an den *Userspace* zurückgegeben
	→ Beispiel: `int (Dateideskriptor)` im Register *EAX*
	→ "UNIX: *Everything is a file descriptor*"
^1668287538676

## Eigenschaften #fc
- Verfügbare *SysCalls* entsprechen der Funktionsspezifikationen aus der *Systembibliothek* `libc`
	→ Beispiel: `open(const char[] *pathname, int flags)`
- Alle Programme [[../../../Ro I/OS & Environment/Linking|linken]] gegen `libc`
^1672682242203

## Beispiele

### POSIX SysCalls #fc
- `fork`, `exeve`: Startet [[../Prozess|Prozesse]]
- `wait4`, `waitpid`: Warte auf Kind-Prozess
- `open`, `close`: Dateien öffnen/ schließen
- `read`, `write`: Lese-/ Schreibzugriffe auf geöffnete/ allokierte Dateien
- `man syscalls` für 180 Weitere…
^1672676183650
