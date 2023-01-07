---
tags: uni dsa practical-cs text
cards-deck: Uni::Courses::DSA
completed: false
aliases:
  - Reguläre Ausdrücke
  - RegEx
  - POSIX RegEx
linter-yaml-title-alias: Reguläre Ausdrücke
date-of-creation: 2022-07-24
mod-date: 2022-10-13
---

# Reguläre Ausdrücke
→ [[../../Theo I/3. Typ - REG/Deterministischer Endlicher Automat|DFA]]

## DSA Syntax: #fc
- Kennzeichnung des String/Zeilen-Starts *\^* und -Endes *?*
- *Konkatenationen*
- *Gruppierungen*, auf die später zugegriffen werden kann: *(ab)*
- *Disjunktion*: *(a|b)*
- *Hüllenbildung*: Wiederholungen durch *+* oder *\**
- *Optionale Teile*: *?*
- Auswahl: *[ab]*
- *Wildcards*: *.*
^1656411674779

## POSIX Extended Syntax: #fc
→ DSA Syntax $\cup\dots$
- "Anti-Auswahl" *[\^ab]* $\equiv\Sigma\setminus\{a,b\}$
- \\n, $n\in[unterschiedlich]$: Eine definierte *Capture Gruppe* (wie zum Beispiel lateinische Buchstaben)
^1663103650554

## Perl & Co. Syntax:
→ [Rust regex crate](https://docs.rs/regex/latest/regex/)

## Einsatzgebiete:
- [[../Text|Textsuche]]
- Festlegung von Datenformaten für Programmeingaben
- Suchmasken für [[../../../Softwareentwicklung/Programmiersprachen|Programmiersprachen]]
