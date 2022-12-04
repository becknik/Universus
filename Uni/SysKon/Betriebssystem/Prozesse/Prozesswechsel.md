---
tags: uni practical-cs syskon os
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - Prozesswechsel
  - Präemption
  - Kontextwechsel
  - Moduswechsel
linter-yaml-title-alias: Prozesswechsel
date: 2022-10-31
mod-date: 2022-11-17
---

# Prozesswechsel

## Funktionsweise: #fc
1. Das System sichert den Zustand des aktiven [[Prozess|Prozesses]]
2. Das System wählt den nächsten Prozess $P_\text{next}$
3. $P_\text{next}$ wird die benötigten Systemressourcen zugewiesen
4. Die Kontrolle wird an $P_\text{next}$ übergeben
^1667235136536

## Ursprung

### Freiwillig: #fc
- Prozess wartet auf zur Fortsetzung des Programmcodes notwendige I/O Ressourcen
- Prozess wartet auf durch andere Prozesse gesetzte Sperre
- [[../Komponenten/System Calls|System Calls]]: `sleep`
^1668289114276

### Präemption: #fc
-> Durch OS
- Nach Ausreizen eines Zugriffsslots auf dem Prozessor, induziert durch eine Time-[[Unterbrechungen|UBR]]
	-> [[OS-Echtzeitfähigkeit]] erfordert eine geringe Antwortzeit aller interaktiven Prozesse
- Prozess mit höherer Priorität wird bereit zur Ausführung
^1668289050502

### Allgemein: #fc
- Präemtiver Prozesswechsel
- I/O-UBR
- Speicherfehler: Daten befinden sich nicht im [[../../../Ro I/Speicher/DRAM|RAM]]
- [[../Komponenten/System Calls|System Calls]]
- [[Unterbrechungen|Exceptions]] bei der Programmausführung
^1668874269460

## Kontextwechsel
1. Speichere Kontext von Prozess $A$ im [[Prozesse/Prozesskontrollblock|PCB]]$(A)$
	 -> Beenden des Ausführungszyklus, Speichere PC & PSW, Lade IHR, Sichere PC & PSW, Sichere CPU-Register
2. Setzte den [[Prozess|Prozesszustand]] von $PCB(A)$ auf blockiert
3. Verschiebe eine Referenz auf $PCB(A)$ in die entsprechende Queue
4. Wähle anderen Prozess $B$ aus Bereit-Queue zur Ausführung
5. Aktualisiere den *Prozesszustand* in $PCB(B)$ auf *aktiv*
6. Aktualisiere Datenstruktur zur Speicherverwaltung
7. Stelle den Kontext von $B$ im Prozessor her

## Funktionsweise

### Beispiele

#### Timer-[[../Unterbrechungen|Interrupt]] #fc
1. Beende *Ausführungszyklus*: führe aktuellen Befehl von *[[../Prozess|Prozess]] $A$* zu Ende aus
2. Speichere *PC & Process-Status-Word* auf den Stack und sperre [[../Unterbrechungen|Interrupts]]
3. Lade *Interrupt-Service-Routine*-Adresse in den PC
	 -> *Moduswechsel*: Aufruf von Interrupt-Handler-Routine im *Kernel-Space*
4. Lade *PC & PSW von Stack* und sichere sie in [[../Prozesse/Prozesskontrollblock|PCB]]$(A)$
5. Sichere weitere CPU-[[../../../Ro I/RISC-V/Register|Register]] in $PCB(A)$
6. Setze den *Zustand in $PCB(A)$* auf "bereit“ & reihe Prozess $A$ in die *Ready-[[../../../DSA/Datenstrukturen/Queue|Queue]]* ein
7. Wähle einen anderen bereiten *Prozess $B$* aus der Ready-Queue
8. Setze den Zustand von $B$ in [[../Prozesse/Prozesskontrollblock|PCB]]$(B)$ auf "aktiv“
9. Stelle CPU-Register von $B$ aus $PCB(B)$ wieder her
10. Lade PC und PSW aus $PCB(B)$ und pushe die Werte auf den Stack
11. Führe `RETI` - "Return from Interrupt" aus
	-> Stellt das Status Word und den PC wieder her
	-> *Moduswechsel* mit Sprung in den User Space
12. Setze Prozess $B$ fort
^1668290489876

#### Waiting for I/O #fc
1. [[../Prozess|Prozess]] $A$ will von Festplatte lesen (`read(fd,buffer,256)`)
	-> *`read()` ist blockiert* bis die von $A$ angefragten Daten verfügbar sind
2. [[../Komponenten/System Calls|System Call]] wird durch *(g)libc* im *User Space* durchgeführt (`sys_read(fd,buffer,256)`)
	-> *Moduswechsel* in den Kernel-Mode
3. Kernel sendet einen *read-Request* an eine Festplatte
4. Kernel setzt Zustand von A in [[Prozesskontrollblock|PCB]]($A$) auf "blockiert" und reiht $A$ in
*Event-[[../../../../DSA/Datenstrukturen/Queue|Queue]]* „*Wait for Disk I/O*“ ein
	 -> $A$ ist nicht "*Busy Waiting*" und hat "freiwillig“ die CPU abgegeben
5. Der Kernel wählt einen *anderen bereiten Prozess* $B$ aus *Ready-Queue*
6. Kernel stellt Zustand von $B$ wieder her, setzt PCB($B$) auf aktiv und übergibt $B$ die CPU
7. Die Festplatte schließt schließlich die I/O-Operation ab
	-> Sendet [[../Unterbrechungen|Hardware-Interrupt]]
	-> Kernel überprüft die Event-Queue „*Wait for Disk I/O*“
8. Kernel setzt den PCB($A$) auf bereit
	-> Entnimmt $A$ aus Event-Queue „Wait for Disk I/O“ und reiht ihn in die *Ready-Queue* ein
- Alternative *Fortsetzungen* des Szenarios:
	- Kernel unterbricht $B$, weil …
		- … Zeitquantum von $B$ abgelaufen ist (Timer-[[../Unterbrechungen|Interrupt]])
		- … $A$ eine höhere Priorität als $B$ hat
	- Warten bis $B$ selbst freiwillig CPU abgibt, wenn $B$ zum Beispiel …
		- … ein I/O ausführt und selbst blockiert wird
		- … $\bot$
^1668292219102

## Eigenschaften: #fc
- Sind transparent für die Anwendung
- Zustandssicherungen eines Prozesses (inklusive Stack-Verwaltung) funktionieren vollständig in Hardware
^1668292366126
