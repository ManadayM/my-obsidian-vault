---
template: moc
---
![tp.web.random_picture](https://images.unsplash.com/photo-1511286148459-914c6179993e?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwODQwMjk3&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# Java
Java is an Object Oriented Programming Language. It was developed by James Gosling at Sun Microsystems. Sun Microsystems was acquired by Oracle, so now Oracle owns Java.

It is not just a programming language. There are many other parts and concepts that make the Java ecosystem. They are Java Language, [[Java Bytecode]], [[Java Virtual Machine (JVM)]], [[Java APIs]], [[Java Runtime Environment (JRE)]], [[Java Development Kit(JDK)]], [[Java Standard Edition (JSE)]], [[Java Enterprise Edition (JEE)]], [[JavaFx]], and much more.

## 📚 Books & Courses
```dataview
TABLE WITHOUT ID 
	link(file.path, file.aliases[0]) AS Title,
	template AS Type,
	progress AS Progress,
	link(url, "Open File↗️") AS File,
	elink(url, "View in Browser↗️") AS URL
FROM [[Java]] 
WHERE 
	contains(template,"book") OR 
	contains(template,"course")
```

## 👨🏻‍🏫 People
```dataview
LIST FROM [[Java]] WHERE contains(template,"people")
```

## 📚 Notes
```dataview
TABLE WITHOUT ID
	link(file.path, file.aliases[0]) AS Title,
	dateformat(file.cday, "yyyy-MM-dd") AS Created,
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
	FROM [[Java]] AND -"Assets"
	WHERE contains(template, "note")
	SORT file.cday ASC
```

---
#### Internal Links
[[Programming Language]]