---
template: moc
---
![tp.web.random_picture](https://images.unsplash.com/photo-1533168461629-51f6f8061c68?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjg3NTc0OTgy&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

JMeter is an open-source software from the Apache Foundation. It is primarily used for performance testing by simulating concurrent load on a target system.

## 🌐 Bookmarks
---
- [Introduction to open-source test tool - JMeter](https://www.emqx.com/en/blog/introduction-to-the-open-source-testing-tool-jmeter)
- [Introduction to JMeter Test Components](https://dev.to/emqx/introduction-to-jmeter-test-components-h42)

## 📚 Books & Courses
---
```dataview
TABLE WITHOUT ID 
	link(file.path, file.aliases[0]) AS Title,
	template AS Type,
	progress AS Progress,
	link(url, "Open File↗️") AS File,
	elink(url, "View in Browser↗️") AS URL
FROM [[JMeter]] 
WHERE 
	contains(template,"book") OR 
	contains(template,"course")
```

## 👨🏻‍🏫 People
---
```dataview
LIST FROM [[JMeter]] WHERE contains(template,"people")
```

## 📚 Notes
---
```dataview
TABLE WITHOUT ID
	link(file.path, file.aliases[0]) AS Title,
	dateformat(file.cday, "yyyy-MM-dd") AS Created,
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
	FROM [[JMeter]] AND -"Assets"
	WHERE contains(template, "note")
	SORT file.cday ASC
```

---
#### Internal Links
