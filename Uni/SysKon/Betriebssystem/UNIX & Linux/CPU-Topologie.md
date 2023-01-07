---
tags: uni practical-cs syskon cpu os linux scheduling
cards-deck: Uni::Courses::SysKon
completed: true
aliases: CPU-Topologie
linter-yaml-title-alias: CPU-Topologie
date-of-creation: 2022-11-25
mod-date: 2022-11-25
---

# CPU-Topologie
→ [[Linux]]-spezifisch

## Domänen-Einteilung:
→ In der ACPI (Advanced Configuration and Power Interface) *SLIT* (System Locality Distance Information Table) 
1. [[../../../Ro I/Aktuelles/Multithreading/Simultanious Multithreading|SMT]] Cores
2. Kerne auf demselben [[../../../Ro I/Aktuelles/Shared Memory|NUMA]]-Node
3. Direkte Nachbarn im NUMA-Raster (auf und außerhalb des NUMA-Packets (?))
4. Das gesamte NUMA-Package mit Nachbarn außerhalb des NUMA-Packets
