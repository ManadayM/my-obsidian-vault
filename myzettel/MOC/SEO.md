---
template: moc
---
![tp.web.random_picture](https://images.unsplash.com/photo-1562577309-2592ab84b1bc?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjg0MjQ4ODIw&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# SEO

Search Engine Optimisation is a continual process to optimize your SERP ranking by optimizing your content.

## 📰 SEO Blogs
1. [Learning SEO](https://learningseo.io/)
2. [Reddit SEO](https://www.reddit.com/r/SEO/)
3. [Ahrefs Blog](https://ahrefs.com/blog/)
	1. [Ahrefs Academy](https://ahrefs.com/academy)
4. [Backlink O](https://backlinko.com/blog)
5. [The Moz Blog](https://moz.com/blog)
6. [RankMath SEO Course](https://rankmath.com/my-account/seo-course)

## 📚 Notes
```dataview
TABLE WITHOUT ID
	link(file.path, file.aliases[0]) AS Title,
	dateformat(file.cday, "yyyy-MM-dd") AS Created,
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
	FROM [[SEO]] AND -"Assets"
	WHERE contains(template, "note")
	SORT file.cday ASC
```

## 📚 Books & Courses
```dataview
TABLE WITHOUT ID 
	link(file.path, file.aliases[0]) AS Title,
	template AS Type,
	progress AS Progress,
	link(url, "Open File↗️") AS File,
	elink(url, "View in Browser↗️") AS URL
FROM [[SEO]] 
WHERE 
	contains(template,"book") OR 
	contains(template,"course")
```

## 👨🏻‍🏫 People
```dataview
LIST FROM [[SEO]] WHERE contains(template,"people")
```



---
#### Internal Links
