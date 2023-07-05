---
template: weekly
calendar: https://calendar.google.com/calendar/r/week/<%moment().startOf('isoWeek').format("YYYY/M/D")%>
week_id: <%moment().startOf('isoWeek').format('YYYY')%>-W<%moment().format('WW')%>
week_starts: <%moment().startOf('isoWeek').format('YYYY-MM-DD')%>
week_ends: <%moment().endOf('isoWeek').format('YYYY-MM-DD')%>
summary: "👍 👎"
productivity_score: 
---
<% tp.web.random_picture("900x300", "tree,landscape,water,mountain") %>

[[<%moment().startOf('isoWeek').add(-7,'days').format('YYYY')%>-W<%moment().format('WW')-1%>]] | [[<%moment().startOf('isoWeek').format('YYYY-MM')%>|<%moment().startOf('isoWeek').format('MMM YYYY')%>]] | [[<%moment().startOf('isoWeek').add(7,'days').format('YYYY')%>-W<%moment().format('WW') - -1%>]]  | [This week's calendar](https://calendar.google.com/calendar/r/week/<%moment().startOf('isoWeek').format("YYYY/M/D")%>) | (date:: <%tp.date.now("YYYY-MM-DD")%>)

## ✅ TODO List
---
- [ ]
- [ ]
- [ ]
- [ ]

## 🌐 Bookmarks
---
- 
- 

## ✍️ Daily Summary
---
```dataview
TABLE WITHOUT ID 
	link(file.path, dateformat(file.day,"dd-MM")) AS Day,
	productivity_score AS "Prod Score",
	summary AS "Summary" 
FROM "Calendar/Daily Notes"
WHERE 
file.day >= date(<%moment().startOf('isoWeek').format('YYYY-MM-DD')%>) AND
file.day <= date(<%moment().endOf('isoWeek').format('YYYY-MM-DD')%>)
```


## 💪 Fitness Summary
---
```dataview
TABLE walked AS Walked, sleep AS "Sleep Duration" 
FROM "Calendar/Daily Notes"
WHERE 
file.day >= date(<%moment().startOf('isoWeek').format('YYYY-MM-DD')%>) AND
file.day <= date(<%moment().endOf('isoWeek').format('YYYY-MM-DD')%>)
SORT file.day ASC
```
