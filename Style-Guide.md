# Style-Guide

## Introduction
This file *serves as a guide* for those, which are *interested in contributing* to this vault, and maybe users, which are *eager to create their own vaults* and are longing for some *more [[Recommendations]] and* (my) *best practices* to start from. It aims to discussions this projects design decision.

## File-Tree Structure
- `./Uni`: Folders located in this directory should be named after the courses CamelCase *abbreviation*, if necessary with roman digits instead of Latin ones
- `./Uni/CourseXY`:
	- **Folders** in this directory are meant to structure the courses content on the highest level of abstraction in a *white-space allowing* naming scheme
	-> Sometimes courses offer a basic structure of their content, which may be applied (e.g. the Theo II course: with `Complexity Theory`, `Computabillity`, `Decidabillity`)
	- **Files** in this directory should also follow the *white-space* containing naming scheme and (mostly) must be of the #abstraction type
- Every *subfolder* in a directory should have one or more #abstraction files on the same or further pathlevels above the folder node, which *explain the relations* between containing *atomic files* (and further contents)
	-> Example given: [[Uni/DSA/Text-Such-Algorithmem|Text-Such-Algorithmen]] file for `./Uni/DSA/Algorithmen/Text/*` sub-files; [[Uni/DSA/Bäume|Bäume]] file for  `./Uni/DSA/Bäume/*`, containing a comparison table
- *Non-Markdown Contents* should be located in the `./_Figures` directory and named properly to their purpose
	-> The name of the folder was chosen for the *sake of simplicity* and does *not restrict on image formats*
	-> **Copyright claims** *must be followed* under any circumstance!
	-> Example given:
	[[Uni/DSA/Algorithmen/Text/_Figures/Beispiel Boyer-Moore Anwendung.png]], [[Uni/DSA/Bäume/_Figures/Beispiel Präfix-Baum.png]]

## Document Structure
I mainly used the [Obsidian Linter](https://github.com/platers/obsidian-linter) plugin to maintain a strict structure across different documents. I included my personal setting in this git under `./.obsidian/plugins/obsidian-linter/data.json`. If you are interested in those settings, just install the plugin and the `data.json` file should apply the settings.
However be aware, that there are contents in the provided settings which I may not have added on the git so far, so that you should *observe and adjust it* before being able to apply the rules.

In the following I listed some *ground laying rules* I tried to obey:
### Text Formatting
- Just *step down one* heading-level at a time
	-> This is especially important for the [Anki Flashcards Plugin](https://github.com/reuseman/flashcards-obsidian) which creates the flashcard front in the scheme of \<h1\> > \<h2\> > ... > \<h6\>
- Use *italics* to *empathize things*
	-> Some documents clearly lack on them, which tracks back on time pressure while creating those documents...
- Use further **==*typographics*==** sparsely, to avoid an "overload" of the files and to increase readability by lowering noise
	-> The *Flashcard Plugin* currently does not support ==highlighting== too by the way
- *Blockquotes* should only be used for annotations or discussions
- Nobody needs horizontal rules (YAML structure excluded)

### General Structuring
- The \<h1\>-*heading* should be equal to the *files name*
- The following \<hx\> names should most often be picked from the contents of the [[Headings]] file
	-> There may be examples where more than on name would be appropriate, which may lead to confusion for people which have not worked on this vault themselves... No clue how so solve this issue.
- The *sorting of sections* should logical and easy to read trough
- *Mathematical definitions* look better, when using the centered \$\$...\$\$ MathJax formatting
- *Non-text contents* should as far as possible be bind in using *image links*
	-> \!\[A foo-bar picture|size\]\(foo.bar\)
- *References to external sources* should be located at the bottom of a Markdown file
	-> **The source** of every very *thesis* should be linked right there!

### YAML Entries
To *speed up* the creation of files with equal YAML parameters, templates with a basic YAML might be used. I did this by creating the `./_Templates` folder, setting it as my default template folder in the core plugins settings adding a *shortcut*.
-> For example, one of my template looks like [[/_Templates/DSA|this]]

Here is *my set of YAML entries*:
- *tags*: A *Obsidian native* YAML entry which holds all Obsidian tags of the file
  -> [Linter](https://github.com/platers/obsidian-linter) can be tricked to automatically remove \#s, which make *adding existent tags* very fast
  -> For further intel take a look at the section down below :)
- *cards-deck*: The Anki deck generated flashcards will be sent to
- *complete*: For displaying the state of incompleteness
	-> You can create a [[!TODO]]-list by making a simple database call with the [Obsidian Dataview](https://github.com/blacksmithgu/obsidian-dataview) plugin
- *aliases*: A further Obsidian native entry which sums up all names a file shows up when starting to add a wikilink by typing \[\[\]\]
	-> Can be used to speed up the substitution of the full path name reference [[Uni/DSA/Text]] to short ones [[Uni/DSA/Text|Text]] or [[Uni/DSA/Text|custom ones]]
	-> [Linter](https://github.com/platers/obsidian-linter) really works wonders on this entry set by saving space and formatting multiple values
- *linter-yaml-title-alias*: I don't know why this even exists - but as long as Linter works, I wont dare complaining :^)
- *date* & *mod-date*: Kudos to the Linter automations!

## Tag Structure
This field is mainly relevant for *database and search queries*, a *overall-structuring* in the vault and the *coloring* of the *graph view*. It also might satisfy someones perfectionism.
This might be the *most taste-based section* of this guide, nevertheless I want to give a quick sum up of my (kind of thoughtful created) system. In my mind, there exists no such thing as a "best system", and for example the used one isn't the best one for using database queries on it (or at least I can't imagine some nice queries tough). If you came over a enhancement, please let me know: [private E-Mail](jannikb@posteo.de).

I used a modified *snake-case* (without \_s) with english as a naming scheme, because I think this fits the most into the YAML formatting.
- *General Type(s)*: #abstraction 
	-> I wrested with myself if I also should add a \#atomic tag, but I then came over the thought, that this may rather *lead to bloating* in the YAMLs tag section, because nearly every file fits those trait...
	-> I also concluded that a separate \#MOC tag is part of that maybe bloating thing too - so I specified, that \#MOC-typed files are a subset of the files marked as #abstraction
- *Basic categories*: #theoretical-cs,  #techincal-cs, #practical-cs 
	-> You could argue, that simple course tags might be enough, but I wanted to catch those #addition files which are no part of a course itself with those tags, on which at least one of those tags is a good fit
- *Courses*: #dsa,  #ro-1, #theo-2, ... 
	-> To complete inconsistency I decided to use *Latin numbers* here, to enhance readability in the tags section - e.g.: you're short-sighted and looking into the tags section of your super small mobile device to view a topics course name and have to divide between `theo-i`, `theo-ii` and `theo-iii` :(
- *Sub-Topics*: #algorithm, #paradigm, #prog (-gramming), #java, ...
- *Topics*: #halteproblem, #bipartit, #sort, #cpu, #linux, ...