---
aliases: [Courses]
---
# Courses Overview
```dataview
TABLE WITHOUT ID
	link(file.link, file.aliases[0]) AS "Course Title",
	progress AS Progress, 
	priority AS Priority,
	elink(url, "View↗") AS "🏡"
FROM "" AND -"Assets"
WHERE contains(template, "course")
SORT priority DESC
```

