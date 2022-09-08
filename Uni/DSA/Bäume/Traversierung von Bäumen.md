---
tags: uni dsa practical-cs tree algorithm
cards-deck: Uni::Courses::DSA
status: 
aliases:
  - Traversierung Von Bäumen
  - Levelorder
  - Preorder
  - Inorder
  - Postorder
linter-yaml-title-alias: Traversierung Von Bäumen
date: 2022-07-22
mod-date: 2022-09-03
---

# Traversierung Von Bäumen

## Kategorien #fc
- [[../Graphen/Algorithmen/Tiefensuche|Tiefensuche]]:
	- **Preorder**: Zuerst der Knoten, dann der linke, danach der rechte Teilbaum
		-> Erzeugt die normale [[Polnische Notation]]/ Präfixschreibweise
	- **Inorder**: Zuerst der der linke Teilbaum, dann der Knoten und dann der rechte Teilbaum
		-> Erzeugt die Infix-Schreibweise ohne Klammerung
	- **Postorder**-Traversierung: Zuerst der Linke, dann der rechte Teilbaum und dann der Knoten
		-> Erzeugt die umgekehrte [[Polnische Notation]]/ Postfixschreibweise
		-> Erlaubt mit *Preorder* zusammen eine Rekonstruktion des Baums
- [[../Graphen/Algorithmen/Breitensuche|Breitensuche]]:
	- **Levelorder**-Traversierung: Die Knoten werden Niveau-weise durchlaufen
^1651410159125

## Code Der DFS-Varianten: #fc
```java
Preorder:
if (n != nullNode) {
	System.out.println(n.toString());
	printPreorder(n.getLeft());
	printPreorder(n.getRight());
}
```
```java
Postorder:
if (n != nullNode) {
	printPostorder(n.getLeft());
	printPostorder(n.getRight());
	System.out.println(n.toString());
}
```
```java
Inorder:
if (n != nullNode) {
	printInorder(n.getLeft());
	System.out.println(n.toString());
	printInorder(n.getRight());
}
```
^1658939069053
