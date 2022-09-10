---
tags: explainatory
---

# Style-Guide

## Introduction
This file *serves as a guide* for those, which are *interested in contributing* to this vault, and maybe users, which are *eager to create their own vaults* and are longing for some *more [[Recommendations]] and best practices* to start from. It aims to discussions this projects design decision.

## File-Tree Structure
- `/Uni`: Folders located in this directory should be named after the courses CamelCase *abbreviation*, if necessary with roman digits instead of Latin ones
	-> If you might want to use your vault for other things like a [Zettelkasten](https://en.wikipedia.org/wiki/Zettelkasten), a *cook book* or *summaries of books you read*, you simply can start with separate root folder
- `/Uni/CourseXY`:
	- **Folders** in this directory are meant to structure the courses content on the highest level of abstraction in a *white-space allowing* naming scheme
	-> Sometimes courses offer a basic structure of their content, which may be applied (e.g. the Theo II course: with `Complexity Theory`, `Computabillity`, `Decidabillity`)
	- **Files** in this directory should also follow the *white-space* containing naming scheme and (mostly) must be of the #abstraction type
- Every *subfolder* in a directory should have one or more #abstraction files on the same or further path levels above the folder node, which *explain the relations* between containing *atomic files* (and further contents)
	-> A #abstraction file should generally be pointed out by using the topics name in *plural*, if appropriate
	-> Example given: [[Uni/DSA/Text-Such-Algorithmem|Text-Such-Algorithmen]] file for `/Uni/DSA/Algorithmen/Text/*` sub-files; [[Uni/DSA/Bäume|Bäume]] file for `/Uni/DSA/Bäume/*`, containing a comparison table
- *Non-Markdown Contents* should be located in the `./_Figures` directory and named properly to their purpose
	-> The name of the folder was chosen for the *sake of simplicity* and does *not restrict on image formats*
	-> **Copyright claims** *must be followed* under any circumstance!
	-> Example given:
	[[Uni/DSA/Algorithmen/Text/_Figures/Beispiel Boyer-Moore Anwendung.png]], [[Uni/DSA/Bäume/_Figures/Beispiel Präfix-Baum.png]]

## Document Structure
I mainly used the [Obsidian Linter](https://github.com/platers/obsidian-linter) plugin to maintain a strict structure across different documents. I included my personal setting in this git under `./.obsidian/plugins/obsidian-linter/data.json`. If you are interested in those settings, just install the plugin and the `data.json` file should apply the settings.
However be aware, that there are contents in the provided settings which I may not have added on the git so far, so that you should *observe and adjust it* before being able to apply the rules.

In the following I listed some *ground laying rules* I *tried* to obey:

### Text Formatting
- Just *step down one* heading-level at a time
	-> This is especially important for the [Anki Flashcards Plugin](https://github.com/reuseman/flashcards-obsidian) which creates the flashcard front in the scheme of \<h1\> > \<h2\> > … > \<h6\>
- Use *italics* to *empathize things*
	-> Some documents clearly lack on them, which tracks back on time pressure while creating those documents…
- Use further **==*typographics*==** sparsely, to avoid an "overload" of the files and to increase readability by lowering the general noise of the document
	-> The *Flashcard Plugin* currently just doesn't support ==highlighting== by the way
- *Blockquotes* should only be used for annotations or discussions
- Nobody needs *horizontal rules* (YAML structuring excluded)

### General Structuring
- The \<h1\>-*heading* should be equal to the *files name*
- The following \<hx\> names should most often be picked from the contents of the [[Headings]] file or topic specific stuff
	-> There may be examples where more than on name out of the [[Headings]] file would be appropriate, which may lead to confusion for people which haven't worked on this vault themselves… I have clue so far how so address this issue :(
- The *sorting of sections* should logical and easy to read trough
- *Mathematical definitions* look better, when using the centered \$\$…\$\$ MathJax formatting
	-> E.g.: [[Uni/DSA/Graphen/Fluss|Fluss]], [[Uni/DSA/Nebenläufige Abläufe/Amdahlsches Gesetz|Amdahlsches Gesetz]]
- *Non-text contents* should as far as possible be bind in using *image links*
	-> The extended syntax for external pictures: \!\[A foo-bar picture|size\]\(foo.bar\)
	-> E.g.: [[Uni/DSA/Nebenläufige Abläufe/Philosophenproblem|Philosophenproblem]], [[Uni/DSA/Graphen/Wege & Kreise|Wege & Kreise]]
- For providing important annotation on sparse space like in tables, the [Markdown footnote syntax](https://www.markdownguide.org/cheat-sheet/) might be helpful
	-> E.g.: [[Uni/DSA/Datenstrukturen für Graphen|Datenstrukturen für Graphen]]
- *References to external sources* should, if existent, be linked with the reference syntax located *at the bottom* of the file
	-> **The source** of every very *thesis*, which isn't part of the lecture, should be linked right there!

### YAML Entries
To *speed up* the creation of files with equal [YAML](https://en.wikipedia.org/wiki/YAML) parameters, templates with a basic YAML might be used. I did this by creating the `./_Templates` folder, setting it as my default template folder in the core plugins settings and adding a *shortcut*.
-> For example, one of my template looks like [[/_Templates/DSA|this]]
Templates also play nicely with [Linter](https://github.com/platers/obsidian-linter), when you first lint the file, paste the templates content by hitting the shortcut and then just delete the duplicate declarations.

Here is *my set of YAML entries*:
- `tags`: A *Obsidian native* YAML entry which holds all Obsidian tags of the file
	->  *Linter* can be tricked to automatically remove \#s, which make *adding existent tags* very fast
	-> For further *intel on tags* take a look at the section down below :)
- `cards-deck`: The Anki deck generated flashcards will be sent to
	-> I tried to create an nearly equal naming scheme as present in this project
- `complete`: For displaying the state of incompleteness
	-> You can create a [[!TODO]]-list by making a simple database call with the [Obsidian Dataview](https://github.com/blacksmithgu/obsidian-dataview) plugin (which really is "overkill" for this trivial job)
- `aliases`: A further Obsidian native entry which sums up all names a file shows up when starting to add a wikilink by typing \[\[\]\]
	-> Can be used to speed up the substitution of the full path name reference [[Uni/DSA/Text]] to short ones [[Uni/DSA/Text|Text]] or [[Uni/DSA/Text|custom ones]]
	-> [Linter](https://github.com/platers/obsidian-linter) really works wonders on this entry set by saving space and formatting multiple values
- *linter-yaml-title-alias*: I don't know why this even exists - but as long as Linter works, I wont dare complaining :^)
- *date* & *mod-date*: Kudos to those Linter automations!

## Tag Structure
This field is mainly relevant for *database and search queries*, a *overall-structuring* in the vault and the *coloring* of the *graph view*. It also might satisfy someones perfectionism.
This might be the *most taste-based section* of this guide, nevertheless I want to give a quick sum up of my (kind of thoughtful created) system. In my mind, there exists no such thing as a "best system", and for example the used one isn't the best one for [Obsidian Dataview](https://github.com/blacksmithgu/obsidian-dataview) queries on it (or at least I can't imagine some nice tough). If you came over a enhancement, please let me know: [E-Mail](mailto:jannikb@posteo.de).

I used a modified *snake-case* (without \_s) with English as a naming scheme, because I think this suits the YAML formatting the most:
- *General Type(s)*: #abstraction
	-> I wrested with myself if I also should add a \#atomic tag, but I then came over the thought, that this may rather *lead to bloating* in the YAMLs tag section, because nearly every file in this vault my fits that trait…
	-> I also concluded that a separate \#MOC (=[Map of Content](https://www.youtube.com/watch?v=7GqQKCT0PZ4)) tag is part of that maybe bloating thing too - so I specified, that \#MOC-typed files are a subset of the files marked as #abstraction
- *Basic categories*: #theoretical-cs,  #techincal-cs, #practical-cs
	-> You could argue, that simple course tags might be enough, but I wanted to catch up those #addition files which are no part of a course itself, on which at least one of the named tags should be a good fit
- *Courses*: #dsa,  #ro-1, #theo-2, …
	-> To complete inconsistency I decided to use *Latin numbers* here, to enhance readability in the tags section - e.g.: you're short-sighted and looking into the tags section of your super small mobile device to view a topics course name and have to divide between `theo-i`, `theo-ii` and `theo-iii` :(
- *Sub-Topics*: #algorithm, #paradigm, #prog (-gramming), #java, …
- *Topics*: #halteproblem, #bipartit, #sort, #cpu, #linux, …
