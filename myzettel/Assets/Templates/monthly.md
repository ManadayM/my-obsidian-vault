---
template: monthly
calendar: https://calendar.google.com/calendar/r/month/<%tp.date.now("YYYY/M/1")%>
month_ends: <%moment().endOf('month').format('YYYY-MM-DD')%>
summary: "👍 👎"
productivity_score: 
---
<% tp.web.random_picture("900x300", "tree,landscape,water,mountain") %>

[[<%tp.date.now("YYYY-MM", "P-1M") %>]] | [[<%tp.date.now("YYYY")%>]]  | [[<%tp.date.now("YYYY-MM", "P1M") %>]] | [This month's calendar](https://calendar.google.com/calendar/r/month/<%tp.date.now("YYYY/M/1") %>) | (date:: <%tp.date.now("YYYY-MM-DD")%>)

# <%tp.date.now("MMM YYYY")%>

## 🎯 Focus Areas
- 
- 
- 
- 

## Weekly Summary
```dataview
TABLE WITHOUT ID 
	link(file.path, string(week_id)) AS Week,
	productivity_score AS "Prod Score",
	summary AS "Summary"  
FROM "Calendar/Weekly Notes"
WHERE 
	week_ends >= date(<%tp.date.now('YYYY-MM-01')%>) AND
	week_ends <= date(<%moment().endOf('month').format('YYYY-MM-DD')%>)
```
