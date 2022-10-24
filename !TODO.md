---
complete: true
---

# !TODO

## Non-complete:
```dataview
LIST
WHERE complete = false 
SORT date DESC
```

## Orphans:
```dataview
list
from ""
where length(file.inlinks)=0 and length(file.outlinks)=0
```
[Source: Obsidian.md](https://forum.obsidian.md/t/find-orphan-notes/817/15)

## Dangling Links:
```dataviewjs
let r = Object.entries(dv.app.metadataCache.unresolvedLinks) .filter(([k,v])=>Object.keys(v).length) .flatMap(([k,v]) => Object.keys(v).map(x=>dv.fileLink(x)))  
dv.list([...new Set(r)])  
```
[Source: Reddit](https://www.reddit.com/r/ObsidianMD/comments/sdtjl8/is_there_a_way_to_list_all_dangling_links_aka/)