---
tags: uni dsa practical-cs tree digital-tree indexstruct
cards-deck: Uni::Courses::DSA
completed: true
aliases: Tries-Baum
linter-yaml-title-alias: Tries-Baum
date-of-creation: 2022-07-22
mod-date: 2022-09-02
---

# Tries-Baum
→ [[Digitalbäume]]

## Eigenschaften: #fc
- Der Name kommt von "Text Re*trie*val"
- Jeder Knoten speichert eine Menge an indizierte Referenz, die dem zugrunde liegenden Alphabet $\Sigma$ entsprechen
	→ Tries können lange, gemeinsame Teilworte aufweisen
	→ Sie funktionieren nur auf Wörtern, die nur aus Alphabetszeichen bestehen
	→ Weisen redundante Buchstabenkombinationen auf, die nie vorkommen
	→ Unausgeglichenheit: Knoten können so gut wie keine ausgehenden Kanten haben
- Bestehen aus *TrieNode* (=innere Knoten) und *LeafNode*, an denen ein Wort endet, was sie nicht unbedingt zu Blattknoten macht
^1652810480336

## Beispiel:
![[_Figures/Beispiel Tries-Baum.png]]
