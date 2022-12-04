---
tags: uni practical-cs syskon
cards-deck: Uni::Courses::SysKon
complete: true
aliases:
  - Produzent-Konsument
  - Pipeline
linter-yaml-title-alias: Produzent-Konsument
date: 2022-10-24
mod-date: 2022-11-07
---

# Produzent-Konsument

## Prinzip: #fc
- Der *Produzent* erzeugt Daten und sendet sie zum *Konsument*
- Der *Konsument* erhält und verarbeitet die Daten
	-> *Unidirektionale* Kommunikation
^1666630152014

## Pipeline: #fc
-> Eine Verallgemeinerung des Produzenten-Konsumenten-Modells
- *Intermediäre Komponenten* sind sowohl Konsumenten, als auch Produzenten
- Die Prozesse sind über *unidirektionale* Kommunikationskanäle miteinander verbunden
	-> Rückkopplungen/ Schleifen sind erlaubt
- Beispiele: [[../../Ro I/RISC-V/Pipeline|RISC-V Pipeline]]
^1666630152023
