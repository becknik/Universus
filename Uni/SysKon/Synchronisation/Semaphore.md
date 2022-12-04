---
tags: uni practical-cs syskon parallel sync
cards-deck: Uni::Courses::SysKon
complete: true
aliases: Semaphore
linter-yaml-title-alias: Semaphore
date: 2022-12-03
mod-date: 2022-12-03
---

# Semaphore

## Annahmen: #fc
- [[../Korrektheitskriterien|Fairness]] (=FIFO) in der [[../../DSA/Datenstrukturen/Queue|Queue]]
	- Queues können auch als Mengen ohne Garantie der Fairness oder als Heap (unfair) implementiert werden
- Fairness im [[../Betriebssystem/Scheduling|Scheduling]]
	-> *Prioritäteninversion*, was durch *Prioritätenvererbung* aufgehoben werden kann
^1670107430671

## Funktionsweise #fc
- Gemeinsame Zustandsvariablen werden vom OS z.B. über die Verwendung von [[../Korrektheitskriterien|fairen]] [[Spin-Locks|Spin-Locks]] (z.B. Fetch & Add) verwaltet
	-> Stellt eine atomare Veränderung sicher
- Der Zugriff erfolgt über [[../Betriebssystem/Komponenten/System Calls|System Calls]]
- `wait()` ($\neq$`await`):
	- Dekrementiert die Passier-Variable `value`
	- Falls `value` negativ wird, wird der [[../Betriebssystem/Prozesse/Threads|Thread]] auf *Blocked* gesetzt und in die [[../../DSA/Datenstrukturen/Queue|Queue]] des Semaphors eingereiht
		-> Die Queue von dem OS verwaltet
- `signal()`:
	- Signalisiert den wartenden Threads durch die Inkrementierung von `value`, dass die Ausführung des *kritischen Abschnitts* beendet ist
^1670107430678

### Pseudocode: #fc
```
integer sem_wait(Semaphore S)
{
	/* Kontextwechsel in Kernel-Modus */
	S.lock.acquire(); // faires aktives Warten … aber nur kurz!
	S.value--;
	if (S.value < 0)
		/* blockiere und platziere Thread in S.queue */
		state(current) ← BLOCKED;
		append(S.queue, current);
	}
	S.lock.release();
}
```
```
integer sem_wait(Semaphore S)
{
	/* Kontextwechsel in Kernel-Modus */
	S.lock.acquire(); // faires aktives Warten … aber nur kurz!
	S.value--;
	if (S.value < 0)
		/* blockiere und platziere Thread in S.queue */
		state(current) ← BLOCKED;
		append(S.queue, current);
	}
	S.lock.release();
}
```
^1670107430681

## Eigenschaften: #fc
- Das Betriebssystem kann faire [[Spin-Locks]] mit [[Spin-Locks|RMW-Operationen]] für eine konsistente nebenläufige Aktualisierung des Semaphors nutzen
	-> Semaphore können nicht für die nebenläufige Implementierung von Semaphoren verwendet werden
^1670107430683
