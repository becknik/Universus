---
tags: explainatory
---

# UNIversus
An **universitary knowledge collection** of a ambitious CS students using the woderful [Obsidian.md](https://obsidian.md/) Markdown tool with it's extending syntax and graph-view. This project is aiming to **sum up** all (essential) parts of teached subjects of the [University of Stuttgart](https://www.uni-stuttgart.de/) *CS bachelor degree* course in a cross-(Wiki-)linking approach.
This git also holds some of my *tips for beginners*.

However, be aware that the summaries were *initially created for myself* and therefore are sensitive to *my personal* way of thinking and understanding - which does not mean, that contributions aren't welcome!

Even though, *this*, the [[Recommendations]] and the [[Style-Guide]] file are written in *English* to make my gathered *recommendations* and *best practices* for Obsidian understandable for an *international heading*, the summary is written in my native language, **German**.

## Getting Started:
All files are fully (extended) *Markdown-compatible*, so you could actually browse this collection with any MD-compatible text-editor. To get the best out of the Obsidian MD-flavor and the *most fluent experience* it's recommend to…
- Installing Obsidian from the [Official Webiste](https://obsidian.md/) and read the introduction

	-> Switch between *Editing*- and a more pleasing *Reading-Mode* by clicking the right top corner icon or *Ctrl+e* - view the *graph view* select the icon on the left side bar or just hit *Ctrl+g*
- If you should find liking in what you see and you might want to *start your own* private Obsidian vault, I would recommend you to read through my Obsidian [[Recommendations]], the more extensive [[Style-Guide]] (which contain lower-level tips and best practices, which might save you some time) or just research yourself

	-> Please **first install the application**, to be able to open the Wikilinked files. Also, the *GitHub Markdown flavor* is really restricted to the [basic Markdown syntax](https://www.markdownguide.org/basic-syntax/), which is suboptimal for reading Markdown files created in Obsidian…
- If you should be interested in *contributing or enhancing* my notes, consider writing me an [private E-Mail](mailto:jannikb@posteo.de), contact me somewhere else or [open an Issue](https://github.com/jarnnk/UNIversus/issues)/ [Pull Request](https://github.com/jarnnk/UNIversus/pulls) :^)

### Flashcards for Everyone
Currently I use this *Obsidian vault* in combination with the Anki [Flashcards Plugin](https://github.com/reuseman/flashcards-obsidian). Unfortunately, this plugin only works for one person at the same time. So I came over the idea to mirroring my generated [Anki](https://apps.ankiweb.net/)-decks for the courses in this repo on [AnkiWeb](https://ankiweb.net/shared/decks/).
Currently available are:
- [Datenstrukturen & Algorithmen](https://ankiweb.net/shared/info/1023735405)

## Note, that…
I do not sync the full `.obsidian` folder due to the *Obsidian's plugin system* (which simply downloads all plugins locality into a subfolder) and *individual customization* choices. Here's a list of the contents of `/.obsidian` I decided to include:
- `app.json` for the default settings
> Yes, I somehow manage to make use of this buggy implementation of VIM - Just turn it off in the settings or don't forget to 'a'/'A' and 'Esc' :D
- `core-plugins.json`: `backlink.json`, `switcher.json` & `templates.json` for the minimal intersect of core plugin settings
- `graph.json` for a personally eye-candy customized view of the graph
- My settings example for the [Obsidian Linter](https://github.com/platers/obsidian-linter) plugin, on which choices you can read more in the community plugin [[Recommendations]] section
---
> This project's name was inspired by my friend and fellow student [Anton Sproll](https://github.com/fewpews) and this [UNIverum](https://github.com/fewpews/UNIversum) project. Also, I just took notice of Obsidian's existence because of this great guy :^)
