---
template: moc
---
![tp.web.random_picture](https://images.unsplash.com/photo-1616469832301-ffaeadc68cf3?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjg3ODA1MzQw&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)


## 🌐 Bookmarks
---
- 

## 📚 Books & Courses
---
```dataview
TABLE WITHOUT ID 
	link(file.path, file.aliases[0]) AS Title,
	template AS Type,
	progress AS Progress,
	link(url, "Open File↗️") AS File,
	elink(url, "View in Browser↗️") AS URL
FROM [[WordPress]] 
WHERE 
	contains(template,"book") OR 
	contains(template,"course")
```

## 👨🏻‍🏫 People
---
```dataview
LIST FROM [[WordPress]] WHERE contains(template,"people")
```

## 📚 Notes
---
```dataview
TABLE WITHOUT ID
	link(file.path, file.aliases[0]) AS Title,
	dateformat(file.cday, "yyyy-MM-dd") AS Created,
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
	FROM [[WordPress]] AND -"Assets"
	WHERE contains(template, "note")
	SORT file.cday ASC
```

---
#### Internal Links
[[CMS]]