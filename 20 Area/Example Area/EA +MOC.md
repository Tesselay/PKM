---
parent: "[[Area Dashboard]]"
title: Example Area
area: Example Area
date-created: 2023-11-17T20:35:12+01:00
date-modified: 2024-03-08T11:39:40+01:00
---

# Example Area

An area of life which will get continuous work on it done, for example "My Health", "Family" or similar. Similar to a project encompassing many parts only that it can't be finished.

### Files

```dataviewjs
for (let group of (dv.pages('"20 Area/Example Area"').where(p => p.file.name != "MOC")).groupBy(p => p.file.folder)) {
	dv.header(
		5, 
		(group.key).slice(group.key.lastIndexOf('/')+1)
	)
	dv.list(group.rows .map(k => k.file.link))
};
```
