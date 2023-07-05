---
template: moc
last_reviewed: "2023-06-24"
---
![tp.web.random_picture](https://images.unsplash.com/photo-1474649111648-d95d30755186?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwODAyNDc2&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

In [[Software Engineering]], an algorithm is a set of instructions for solving a computational problem.

[[Abdul Bari]] nicely differentiates algorithms and programs in his video [Introduction to Algorithms](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=1).

## 📚 Books & Courses
```dataview
TABLE WITHOUT ID 
	link(file.path, file.name) AS Title,
	template AS Type,
	progress AS Progress,
	link(url, "Open File↗️") AS File,
	elink(url, "View in Browser↗️") AS URL
FROM [[Algorithms]] 
WHERE 
	contains(template,"book") OR 
	contains(template,"course")
```

## 👨🏻‍🏫 People
```dataview
LIST FROM [[Algorithms]] WHERE contains(template,"people")
```

## 📚 Linked Notes
```dataview
TABLE 
	dateformat(file.cday, "yyyy-MM-dd") AS Created,
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
	FROM [[Algorithms]] AND -"Assets"
	WHERE contains(template, "note")
	SORT file.cday ASC
```

---
#### Internal Links
[[Software Engineering]]