---
template: moc
---
![tp.web.random_picture](https://images.unsplash.com/photo-1531161983442-376992e671e7?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwODI0NTE0&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# Data Structure
In [[Software Engineering]], the data structure is a way to store and organize data.

## 📚 Books & Courses
```dataview
TABLE WITHOUT ID 
	link(file.path, file.aliases[0]) AS Title,
	template AS Type,
	progress AS Progress,
	link(url, "View ↗️") AS "Link"
FROM [[Data Structure]] 
WHERE 
	contains(template,"book") OR 
	contains(template,"course")
```

## 👨🏻‍🏫 People
```dataview
LIST FROM [[Data Structure]] WHERE contains(template,"people")
```

## 📚 Notes
```dataview
TABLE WITHOUT ID
	link(file.path, file.aliases[0]) AS Title,
	dateformat(file.cday, "yyyy-MM-dd") AS Created,
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
	FROM [[Data Structure]] AND -"Assets"
	WHERE contains(template, "note")
	SORT file.cday ASC
```

---
#### Internal Links
