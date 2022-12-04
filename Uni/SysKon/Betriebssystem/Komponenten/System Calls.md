---
tags: uni practical-cs syskon os
cards-deck: Uni::Courses::SysKon
complete: true
aliases: System Calls
linter-yaml-title-alias: System Calls
date: 2022-11-12
mod-date: 2022-11-12
---

# System Calls

## Prinzip: #fc
- Setzt sich aus Funktion und Parameter zusammen
	-> Programm A: `open(const char[] *pathname, int flags) - "foo.txt",n`
- (g)libc setzt den *Syscall Parameter* in *User Space*
	-> [[../Unterbrechungen|Software-Interrupt]] `INT 0x80`
- Kernel findet und führt die zur Syscall Nummer passende *Interrupt-Service-Routine* aus
- Ergebnis wird zurück zum Userspace gegeben
	-> `int` (Dateideskriptor) im [[../../../Ro I/CPU/X86_64|x86]]-Register `EAX`
	-> "UNIX: Everything is a file descriptor"
^1668287538676
