---
template: moc
---
![tp.web.random_picture](https://images.unsplash.com/photo-1502943693086-33b5b1cfdf2f?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwODAyMjk0&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

# Courses
```dataview
TABLE 
	progress AS Progress, 
	priority AS Priority,
	link(url, "Course↗") AS "🏡"
FROM "" AND -"Assets"
WHERE contains(template, "course")
SORT priority DESC
```

---
#### Internal Links
