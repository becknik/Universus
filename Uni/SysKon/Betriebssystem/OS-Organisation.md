---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
complete: true
aliases: OS-Organisation
linter-yaml-title-alias: OS-Organisation
date: 2022-11-12
mod-date: 2022-11-12
---

# OS-Organisation

## Instruction Execution Modes #fc
- *Kernel Mode*: Uneingeschränkter Zugriff auf Hardware, [[Prozess|Prozess-Management]] & [[Unterbrechungen|Unterbrechungs-Routinen]] über [[Komponenten/System Calls]]
- *User Mode*: Kein direkter Zugriff auf *Hardware* und *unbefugte Adressräume*
	-> Zu Zugriff auf Hardware ist ein Schnittstelle zwischen Anwendung und OS nötig
	-> Bei Zugriff über Speicherschutz: Memory Protection/ Management Unit -> OS -> Segmentation Fault Interruption -> Prozess wird beendet
^1668285788401
