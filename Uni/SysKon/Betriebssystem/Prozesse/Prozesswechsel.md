---
tags: uni practical-cs syskon os
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Prozesswechsel
  - Präemption
  - Kontextwechsel
  - Moduswechsel
linter-yaml-title-alias: Prozesswechsel
date-of-creation: 2022-10-31
mod-date: 2023-01-02
---

# Prozesswechsel
→ [[../Prozess|Prozess]]

## Funktionsweise von Kontextwechsel (5) #fc
1. Sichere den Zustand (=Befehlszähler, Register, PSW, etc.) des aktiven [[Prozess|Prozesses]] $P_\text{cur}$ in [[Prozesskontrollblock|PCB]]$(P_\text{cur})$
	→ Modifikation des Prozess-Statuses
	→ Die Zustandssicherungen eines Prozesses (inklusive Stack-Verwaltung) funktionieren vollständig in Hardware
2. Verschiebe $PCB(P_\text{cur})$ in die *Blocked*-Queue
3. Wähle (durch ein [[../Scheduling|Scheduler]]) den nächsten Prozess $P_\text{next}$ & entnehme sein *PCB* aus der Bereit-Queue
4. Aktualisiere den Prozess-Status & die Datenstrukturen zur Speicherverwaltung in $PCB(P_\text{next})$
	→ $P_\text{next}$ wird die benötigten Systemressourcen zugewiesen
5. Stelle den Kontext von $P_\text{next}$ in der CPU wieder her
^1670777612822

## Einen Prozesswechsel indizierende Ereignisse (5) #fc
- Uhren-[[../Unterbrechungen|Unterbrechung]] (bei [[Prozesswechsel|Präemption]])
- I/O-[[../Unterbrechungen|UBR]]
- Speicherfehler ([[../Unterbrechungen|Exceptions]]) (zum Beispiel*Swapping*)
- Durch [[../Funktionen/System Calls|System Call]] induziertes [[../Unterbrechungen|Software-Interrupt]]
- Fehler/ [[Unterbrechungen|Exceptions]] durch den Programmcode
	→ Führen meistens direkt zur Terminierung des [[../Prozess|Prozesses]]
^1668874269460

## Ursachen

### Freiwillig Abgabe (3) #fc
- Der [[../Prozess|Prozess]] wartet auf benötigte I/O Ressourcen
- Der Prozess wartet auf durch andere Prozesse gesetzte Sperre
	→ [[Wechselseitiger Ausschluss]]
- Der Prozess ruft den [[../Funktionen/System Calls|System Call]] `sleep` auf
^1668289114276

### Präemption (2) #fc
→ [[../Scheduling|Scheduling]]
- Der Zugriffszeitslot/ das Zeitquantum der Prozessor-Nutzung wurde ausgereizt
	→ Induziert durch eine Time-[[../Unterbrechungen|UBR]]
- Ein Prozess mit *höherer Priorität* wird bereit zur Ausführung
^1668289050502

## Beispiele

### [[Prozesswechsel|Präemption]] durch Timer-[[../Unterbrechungen|Interrupt]] (12) #fc
1. Timer-Interrupt
2. Beende *Ausführungszyklus* durch *zu-Ende-Ausführen* des aktuellen Befehls von [[../Prozess|Prozess]] $A$
3. Speichere *[[../../../Ro I/RISC-V/Problem Counter|Problem Counter]] & Process-Status-Word* auf dem Stack
	→ *Sperre [[../Unterbrechungen|Interrupts]]*
4. Lade *Interrupt-Service-Routine*-Adresse aus dem [[../Unterbrechungen|UBR]]-Vektor in den PC
	→ *Moduswechsel* durch Aufrufen der ISR im *Kernel-Space*
5. Lade *PC & PSW von Stack* und sichere sie in [[../Prozesse/Prozesskontrollblock|PCB]]$(A)$
6. Sichere weitere notwendige CPU-[[../../../Ro I/RISC-V/Register|Register]] in $PCB(A)$
7. Setze den *Zustand* in $PCB(A)$ auf "bereit“ & reihe Prozess $A$ in die *Ready-[[../../../DSA/Datenstrukturen/Queue|Queue]]* ein
8. Wähle einen anderen bereiten *Prozess $B$* aus der Ready-Queue
9. Setze den Zustand von $B$ in [[../Prozesse/Prozesskontrollblock|PCB]]$(B)$ auf "aktiv“
10. Stelle CPU-Register von $B$ aus $PCB(B)$ wieder her
11. Lade PC und PSW aus $PCB(B)$ und sie auf den Stack
12. Führe `RETI` - "Return from Interrupt" aus
	→ *Moduswechsel* in den User Space
	→ Stellt das *Process-Status-Word* und den PC wieder her
13. Prozess $B$ wird fortgesetzt
^1668290489876

### Freiwilliger Wechsel bei waiting for I/O #fc
1. [[../Prozess|Prozess]] $A$ fordert Lesezugriff auf die Festplatte
	→ [[../Funktionen/System Calls|System Call]] `read(fd,buffer,256)` *ist global blockiert*, bis die von $A$ angefragten Daten verfügbar sind
2. Die Systembibliothek `libc` verursacht einen [[../Unterbrechungen|Interrupt]]
	→ *Moduswechsel* in den Kernel-Mode
3. Der Kernel sendet einen *read-Request* an eine Festplatte
4. Kernel setzt [[Prozesskontrollblock|PCB]]$(A)$ auf "blockiert" und reiht $A$ in die passende *Event-[[../../../../DSA/Datenstrukturen/Queue|Queue]]* ein
	→ Freiwillige Abgabe der CPU
5. Der Kernel wählt einen *anderen bereiten* Prozess $B$ aus *Ready-Queue*
6. Kernel stellt Zustand von $B$ wieder her, setzt PCB$(B)$ auf aktiv und übergibt die CPU an $B$
7. Die Festplatte schließt schließlich die I/O-Operation ab und sendet [[../Unterbrechungen|Hardware-Interrupt]]
	→ Kernel überprüft die zugehörige *Event-Queue*
8. Kernel setzt den $PCB(A)$ auf *bereit* und verschiebt den Prozess in die *Ready-Queue*
9. Alternative *Fortsetzungen* des Szenarios:
	- Kernel unterbricht $B$ …
		- … durch [[Prozesswechsel|Präemption]]
		- … da$A$ eine höhere Priorität als $B$ hat
	- Kernel wartet, bis $B$ selbst freiwillig CPU abgibt, wenn…
		- … $B$ ein I/O ausführt und selbst blockiert wird
		- … $B\bot$
^1668292219102
