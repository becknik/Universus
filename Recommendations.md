# Recommendations

## Markdown / Obsidian Syntax
When you shouldn't be familiar with the basic *Markdown Syntax*, a good start/ *cheat sheet* might be [this](https://www.markdownguide.org/cheat-sheet/)). Notice however, that linked sheet can be considered as "overkill", because Obsidian does at the time of writing not support the whole [extended Syntax](https://www.markdownguide.org/extended-syntax/) (like Sub- and Superscript or Emojis).
Confused now? A read on the official [Obsidian website](https://obsidian.md/) should lead you further.

## MathJax
Obsidian supports the TeX-like [MathJax](https://www.mathjax.org/) Syntax out of the box. It's great creating some beautiful formulas or just makes your files look more mathematical.
-> A topic where MathJax shines is the $\mathbfcal{O}$-notation, for example in the [[Uni/DSA/Landau-Notationen|Landau-Notationen]] or [[Uni/DSA/Bäume/AVL-Baum|AVL-Baum]] file

## General Structure/ Philosophy
Because Obsidian aims to *cross-link* everything, it is recommended to split large topics into many *atomic* files, which then reference a #summarizing file for the sub-topic.
-> For example I made a [[Uni/DSA/Graphen/Ungerichteter Graph|Ungerichteter Graph]], [[Uni/DSA/Graphen/Gerichtete Graphen|Gerichteter Graph]] and [[Uni/DSA/Graphen/Gewichteter Graph|Gewichteter Graph]] file, just to link them all in the [[Uni/DSA/Graphen|Graphen]] file.
Because this sometimes can cause more harm than help you out, especially when quickly browsing tough files or creating flashcards, I sometimes *merged minor definitions* and explanations into the sub-topics file and added the therm as a [YAML](https://en.wikipedia.org/wiki/YAML)/ front-header alias*, to still make backlinks possible.
-> Examples for this behavior is especially the file for [[Uni/DSA/Graphen|Graphen]] or the [[Uni/DSA/Bäume|Bäume]] file
> For further structuring-info take a look at the [[Style-Guide]]

## Community Plugins
Here are some *general recommendations* for *basic plugins* which made things easier for me while editing and annotating files with Obsidian. The [plugin catalog](https://obsidian.md/plugins) is gigantic, but I tried to avoid *wasting much time* on this topic and cherry picked some, which suited me the most and seemed generally useful.
All of the following plugins were used to creating and editing all of the published summaries (and even more private files) and they helped me a lot!

### [Linter](https://github.com/platers/obsidian-linter)
- Takes care of the text and [YAML](https://en.wikipedia.org/wiki/YAML)/ front-header *formatting* by removing *empty spacing* and adding this '…' satisfying character, *sorting items* and tags, setting the (modification) *timestamps*, adding or removing *blank lines*, etc.
- Helps to *maintain a clear structuring* across the whole vault
- Sadly, the set-up may be really time consuming, so I added an example configuration I use
	-> It's based on some contents which might not be available on this git and should not be copy-pasted without adjustments

### [Advanced Tables](https://github.com/tgrosinger/advanced-tables-obsidian)
- Helps to dynamically *adjust and format tabular* width and structure when adding new elements
- ==Caution:==
	-> If the *extended Wikilinks* with a \| are causing you trouble in tables, just add a *back-shift* \\ before them
	-> Be careful to substitute *[MathJax](https://www.mathjax.org/)* content with pipes \| to $\mid$, unless you want to die in pain for reformatting the whole table correctly yourself :) (like I had to do some times in the [[Uni/DSA/Landau-Notationen|Landau-Notationen]] file)

### [Paste URL](https://github.com/denolehov/obsidian-url-into-selection)
- Automatically adds the Markdown *link-syntax* around of pasted URLs and automatically *transforms selected text* into a link when pasting
- ==Might be annoying== due to sometimes detecting file paths or Markdown formatting as URLs…
	-> I just consider it useful for much link-pasting like when doing some #addition -al research

### [Anki Flashcards Plugin](https://github.com/reuseman/flashcards-obsidian)
- For manually creating [Anki](https://apps.ankiweb.net/) *flashcards* from sections starting with a *tagged heading* to the next blank line
	-> Its the reason you can read #fc next to nearly every heading across this vault ^^
- ==Some Bugs I experienced:==
	- The plugin occasionally does not parse $\text{Math}^{J_a^x}$ topics and normal text separat, so that the \* is replaced to \<em\>\</em\> in a formula due to HTML conversion…
	-> I prevented this by using a $\cdot$ instead of \* in formulas
	- Another problem is, that it does *not obey the Obsidian figure path settings* and therefore currently all figures are missing on the flashcards…
	- Furthermore, there ist indeed a problems with translation Markdown tables to HTML. To fix this, I sometimes added a blank '-' in the line before the tables start
	-> For example at the bottom of the [[Uni/DSA/Algorithmen/Text/Knuth-Morris-Pratt|Knuth-Morris-Pratt]] file
