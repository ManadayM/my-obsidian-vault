---
template: daily
sleep: ""
walked: true
summary: "👍 👎"
productivity_score: 
---
<% tp.web.random_picture("900x300", "tree,landscape,water,mountain") %>

(weather:: <% tp.user.getWeather() %>) | (date:: <%tp.date.now("YYYY-MM-DD")%>) | (time:: <%tp.date.now("HH:mm")%>)

[[<%tp.date.now("YYYY-MM-DD", -1) %>]] | [[<%moment().startOf('isoWeek').format('YYYY')%>-W<%moment().format('WW')%>]] | [[<%tp.date.now("YYYY-MM-DD", 1) %>]] | [Today's Calendar](https://calendar.google.com/calendar/r/day/<%tp.date.now("YYYY/M/D") %>)

## ✅ TODO List
---
- [x] Ensure you have removed all personal content from this Obsidian Vault
- [ ] Do this
- [ ] Do that

## 📅 Events Today
---
![[<% tp.date.now("MM-DD") %>]]

## ✍️ Scratchpad
---


## ⏳ Hourly Log
---
##### 0600 - 0900
- 
- 

##### 0900 - 1200
- 
- 

##### 1200 - 1500
- 
- 

##### 1500 - 1800
- 
- 

##### 1800 - 2100
- 
- 

##### 2100 - 0000
- 
- 

## Today's Notes
---

```dataview
TABLE WITHOUT ID
link(file.link, file.aliases[0]) AS File,
dateformat(file.mtime, "HH:mm") AS Modified,
dateformat(file.ctime, "yyyy-MM-dd") AS Created
FROM "" AND -"Calendar" AND -"Assets"
WHERE
	file.day = date(<%tp.date.now("YYYY-MM-DD")%>)
OR
	file.cday = date(<%tp.date.now("YYYY-MM-DD")%>)
OR
	file.mday = date(<%tp.date.now("YYYY-MM-DD")%>)
SORT file.mtime ASC
```