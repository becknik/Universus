---
tags: uni practical-cs syskon distributed-systems
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - Push-Pull Modelle
  - Event-Kanal
linter-yaml-title-alias: Push-Pull Modelle
date-of-creation: 2023-01-06
mod-date: 2023-01-07
---

# Push-Pull Modelle

## Voraussetzungen
- *Supplier* und [[../Verarbeitungsmodelle/Producer-Consumer|Consumer]] müssen gegenseitig registriert sein
	→ Lösung: [[Push-Pull Modelle#Events Event Kanal|Event-Kanäle]]
- "Keine Entkopplung bei der Aktivierung"

## [[Events|Event]] Kanal

### Funktionsweise #fc
- Stellt Events bereit, für die er Persistenz, Ordnung, ein Gedächtnis oder Zeitbeschränkungen schaffen kann (aber nicht muss)
- Verwendung des [[Push-Pull Modelle|Push-Pull Modells]] hängt vom individuellen *Suppier*/ [[../Verarbeitungsmodelle/Producer-Consumer|Consumer]] ab
^1673090995787

### Konfigurationen (4) #fc
- *Push*: Events werden vom Event-Kanal simpel von den *Suppliern* zu den [[../Verarbeitungsmodelle/Producer-Consumer|Consumern]] weitergegeben
	→ Max-Airflow-Konfiguration
- *Pull*: Der Kanal fordert Events von den *Suppliern* an und hält sie für *Consumer* bereit, wenn diese sie anfordern
	→ *Staubsauger Konfiguration*
- *Push/Pull*: Der Event-Kanal bekommt Events von den *Suppliern* und lässt sie von *Consumern* anfordern
- *Pull/Push*: Der Kanal fordert Events von den *Suppliern* an und verteilt sie an die *Consumer*
^1673091004111

### Beispiele
- CORBA Event Dienst (V.6, F.24)

## Publisher/ Subscriber System

### Prinzip #fc
- $m$ Subscriber interessieren sich nur für [[Events]] eines bestimmten Typs
- $n$ *Publisher* geben Events aus
	→ $n:m$-Kommunikation
- *Themenbasiert*: Kanäle sind Themenbasiert & werden von den Pubishern dementsprechend gefüllt
	→ Subscriber abonnieren bestimmte Kanäle
- *Inhaltsbasiert*: Abonnieren verläuft über beliebige Abfrage des Event-Inhalts
^1673091010887
