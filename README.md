# UNIversus
An **universitary knowledge collection** of a ambitious CS students using the wonderful [Obsidian.md](https://obsidian.md/) Markdown tool with it's extending syntax and graph-view. This project is aiming to **sum up** all (essential) parts of taught subjects of the [University of Stuttgart](https://www.uni-stuttgart.de/) *CS bachelor degree* course in a cross-(Wiki-)linking approach.

This git also holds some of my *tips for Obsidian interested peoples*.
![](https://raw.githubusercontent.com/jarnnk/UNIversus/main/.example-figures/current-vaults-graph-view.png)

However, be aware that the summaries were *initially created for myself* and therefore are sensitive to *my personal* way of thinking and understanding - which does not mean, that contributions or enhancements aren't welcome!

Note, that *this README*, the [[Recommendations]] and the [[Style-Guide]] file are written in *English* to make my gathered *recommendations* and *best practices* for Obsidian understandable for *international readers*. However the summaries are written in my native language, **German**.

## But WHY?? / Motivation:
…may be the question coming up to your mind. Indeed the effort put in creating, extending and correcting those summaries is huge.
> (Besides I have no idea (at this point) how to coordinate a project like this with multiple people, especially during the writing phase.)

But even considering this, I think this project offers many benefits which overcome my personal doubts:
- The best structure of a summary a human being (literally) could wish for, due to the *graph structure*
- The best way to create *neat and noiseless* files (lets just call it "$\text{Design}\in\overline{\text{THEO}}$"), which you might just *learn better* with (Obsidians theming is customizable to every extend)
- No more *lectures PDF scrolling* to find a topics or theorems definition - Just type it in Obsidians search bar (which might be supporting with doing exercises or writing exam sheets)
	
	-> Keep in mind nevertheless, that *depending on this collection* to much instead of laboring through the courses materials yourself will - without questioning - result in **failing the exam** :)
- A long lasting, *wiki-like* knowledge pool, which eventually make some topics faster graspable my providing examples or a more extensive explanation
- The best way I (so far) came across to share *Anki flashcard decks* and keep them *up-to-date* with *additions and corrections* (see "Flashcards for Everyone" section below)
- Maybe: a better learning curve by discovering links between topics of different courses
- Files can easily be shared or exported to short PDFs (or, considering software like [Pandoc](https://pandoc.org/), even more formats)
---
## Getting Started:
All files are formatted in a (extended) *Extended Markdown-Syntax*, so you could browse this collection with any MD-compatible text-editor.
To get the *most fluent experience* of Obsidian's MD-flavor it's recommend to install Obsidian from the [Official Webiste](https://obsidian.md/) (and maybe watch a Tutorial).

### Some basic functions:
- Switch between *Editing*- and a more pleasing *Reading-Mode* by clicking the right top corner icon or *Ctrl+e*
- View the *graph view* select the icon on the left side bar or just hit *Ctrl+g*

### Recommendations on starting your own vault:
If you should find liking in what you see and you might want to *start your own* private Obsidian vault, I would recommend you to read through my Obsidian [[Recommendations]], the more extensive [[Style-Guide]]. The later contain "low-level" tips and best practices, which might save you some time .

### Contributing:
If you should be interested in *contributing or enhancing* this vault, consider writing me an [private E-Mail](mailto:jannikb@posteo.de), contact me somewhere else or just [open an issue](https://github.com/jarnnk/UNIversus/issues)/ [pull request](https://github.com/jarnnk/UNIversus/pulls) on GitHub :^)

### Flashcards for Everyone:
Currently I use this *Obsidian vault* in combination with the Anki [Flashcards Plugin](https://github.com/reuseman/flashcards-obsidian). Unfortunately, this plugin only works for one person at the same time. So I came over the idea to mirroring my generated [Anki](https://apps.ankiweb.net/)-decks for the courses in this repo on [AnkiWeb](https://ankiweb.net/shared/decks/).
Currently available decks:
- [Datenstrukturen & Algorithmen](https://ankiweb.net/shared/info/1023735405)
- [Systemkonzepte & Programmierung](https://ankiweb.net/shared/info/1702498575) *(IN PROGRESS)*
- [Uni Stuttgart: Mathe 1 für Inf,SWT & MSV](https://ankiweb.net/shared/info/1863940268) *(IN PROGRESS)*
- [Theoretische Informatik I](https://ankiweb.net/shared/info/1096330501)
- [Theoretische Informatik II](https://ankiweb.net/shared/info/729716890) (**WORK NEEDED**)
---
## Notes on repositories structure:
I do not sync the full `/.obsidian` folder due to the *Obsidian's plugin system* (which simply downloads all plugins locality into a subfolder) to allow local *individual customization* and plugin choices.
Here's a list of the contents of `/.obsidian` I decided to include:
- `app.json` for the default settings
> Yes, I somehow manage to make use of this buggy implementation of VIM - Just turn it off in the settings or don't forget to 'a'/'A' and 'Esc' :D
- `core-plugins.json`: `backlink.json`, `switcher.json` & `templates.json` for the minimal intersect of core plugin settings
- `graph.json` for a personally eye-candy customized view of the graph
- My settings example for the [Obsidian Linter](https://github.com/platers/obsidian-linter) plugin, on which choices you can read more in the community plugin [[Recommendations]] section
---
> This project's name was inspired by my friend and fellow student [Anton Sproll](https://github.com/fewpews) and this [UNIverum](https://github.com/fewpews/UNIversum) project. Also, I just took notice of Obsidian's existence because of this great guy :^)
