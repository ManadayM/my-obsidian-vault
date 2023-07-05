---
template: moc
---
![tp.web.random_picture](https://images.unsplash.com/photo-1590328890650-1c94261ff33e?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwODE2Njg1&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# Microservice

## 📚 Books & Courses
```dataview
TABLE WITHOUT ID 
	link(file.path, file.aliases[0]) AS Title,
	template AS Type,
	progress AS Progress,
	link(url, "View ↗️") AS "Link"
FROM [[Microservice]] 
WHERE 
	contains(template,"book") OR 
	contains(template,"course")
```

## 👨🏻‍🏫 People
```dataview
LIST FROM [[Microservice]] WHERE contains(template,"people")
```

## 📚 Notes
```dataview
TABLE WITHOUT ID
	link(file.path, file.aliases[0]) AS Title,
	dateformat(file.cday, "yyyy-MM-dd") AS Created,
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
	FROM [[Microservice]] AND -"Assets"
	WHERE contains(template, "note")
	SORT file.cday ASC
```

---
#### Internal Links
