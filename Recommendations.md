---
tags: explainatory
---

# Recommendations

## Markdown / Obsidian Syntax
When you shouldn't be familiar with the basic *Markdown Syntax*, a good start might be reading trough [this brief Cheat Sheet](https://www.markdownguide.org/cheat-sheet/). Notice however, that things like *sub- and superscript* or *Emojis*, which the sheet lists, aren't supported by Obsidian at the time of writing this file.
Want to know more now? A read through this file or maybe the official [Obsidian documentation](https://help.obsidian.md/Obsidian/Index) might lead you further.

## MathJax
Obsidian supports the TeX-like [MathJax](https://www.mathjax.org/) syntax out of the box. It's great creating some beautiful formulas or just makes your files look more mathematical. $\mathbb{N_0}$!
-> A topic where MathJax shines is the $\mathbfcal{O}$-notation, for example in the [[Uni/DSA/Landau-Notationen|Landau-Notationen]] or [[Uni/DSA/Bäume/AVL-Baum|AVL-Baum]] file

## General Structure/ Philosophy
Because Obsidian aims to *cross-link* everything, it is recommended to split large topics into many *atomic* files, which then are linked together by a #abstraction  file for the sub-topic.
-> For example I made a sub topic [[Uni/DSA/Graphen/Ungerichtete Graphen|Ungerichteter Graph]], [[Uni/DSA/Graphen/Gerichtete Graphen|Gerichteter Graph]] and [[Uni/DSA/Graphen/Gewichteter Graph|Gewichteter Graph]] file, just to link them all in the [[Uni/DSA/Graphen|Graphen]] file.
Because this sometimes can cause more harm than help you out, especially when quickly browsing tough files or creating flashcards, I sometimes *merged minor definitions* and explanations into the sub-topics file and added the topics name as a [YAML front-matter](https://help.obsidian.md/Advanced+topics/YAML+front+matter) alias to still make [Backlinks](https://help.obsidian.md/Plugins/Backlinks) possible.
-> Examples for this behavior is especially the file for [[Uni/DSA/Graphen|Graphen]] or the [[Uni/DSA/Bäume|Bäume]] file
> For further structuring-info take a look at the [[Style-Guide]]

## Community Plugins
Here are some *general recommendations* for *basic plugins* which made things easier for me while editing and annotating files with Obsidian. The [plugin catalog](https://obsidian.md/plugins) is gigantic, but I tried to avoid *wasting much time* on this topic and cherry picked some, which suited me the most and seemed generally useful.
All of the following plugins were used to creating and editing all of the published summaries (and even more private files) and they helped me a lot!

### [Linter](https://github.com/platers/obsidian-linter)
- Takes care of the text and [YAML front-matter](https://help.obsidian.md/Advanced+topics/YAML+front+matter) *formatting* by removing *empty spacing* and adding this '…' satisfying character, *sorting items* and tags, setting the (modification) *timestamps*, adding or removing *blank lines*, etc.
- Helps to *maintain a clear structuring* across the whole vault
- Sadly, the set-up may be really time consuming, so I added an example configuration I use
	-> For further information read the "Document Structure" section of the [[Style-Guide]]

### [Advanced Tables](https://github.com/tgrosinger/advanced-tables-obsidian)
- Helps to dynamically *adjust and format tabular* width and structure when adding new elements
- ==Caution:==
	-> If the *extended Wikilinks* with a \| are causing you trouble in tables, just add a *back-shift* \\ before them
	-> Be careful to substitute *[MathJax](https://www.mathjax.org/)* content with pipes \| to $\mid$, unless you want to die in pain for reformatting the whole table correctly yourself :) (like I had to do in [[Uni/DSA/Landau-Notationen|Landau-Notationen]])

### [Paste URL](https://github.com/denolehov/obsidian-url-into-selection)
- Automatically adds the Markdown *link-syntax* around of pasted URLs and automatically *transforms selected text* into a link when pasting
- ==Might be annoying== due to sometimes detecting file paths or Markdown (URL) formatting as URLs…
	-> I just consider it useful for much link-pasting, like when doing some #addition -al research

### [Anki Flashcards Plugin](https://github.com/reuseman/flashcards-obsidian)
- For manually creating [Anki](https://apps.ankiweb.net/) *flashcards* from sections starting with a *tagged heading* to the next blank line
	-> Its the reason you can read #fc next to nearly every heading across this vault ^^
	-> For more information about my *mirror decks* read the section of the [[README]]
- ==Some Bugs I experienced:==
	- The plugin occasionally does not parse $\text{Math}^{J_a^x}$ topics and normal text separat, so that the \* is replaced to \<em\>\</em\> in a formula due to HTML conversion…
	-> I prevented this by using a $\cdot$ instead of \* in formulas
	- Another problem is, that it does *not obey the Obsidian figure path settings* and therefore currently all figures are missing on the flashcards…
	-> I was able to prevent this behavior by using the external URL link to the file on GitHub. However, the the specified scaling of the figure is gone…
	- Furthermore, there ist indeed a problems with translation Markdown tables to HTML. To fix this, I sometimes added a blank '-' in the line before the tables start
	-> For example at the bottom of the [[Uni/DSA/Algorithmen/Text/Knuth-Morris-Pratt|Knuth-Morris-Pratt]] file

If you aren't [[Uni/Theo II/Komplexitättheorie/Probleme/Satisfiability|satisfied]] yet, please take a look at the more extending [[Style-Guide]] or, as I mentioned some lines above, simply do research/ watch some YouTube videos yourself.