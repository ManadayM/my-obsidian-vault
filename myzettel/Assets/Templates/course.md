<%*
let title = await tp.system.prompt("Course Title")
let url = await tp.system.prompt("Course URL")
await tp.file.rename(title)
-%>
---
template: course
progress: 0%
priority: 
url: <% url %>
---
<% tp.web.random_picture("900x300", "landscape,water,mountain") %>

# [<% title %>](<% url %>)



## 📚 Linked Notes
```dataview
TABLE file.cday AS Created 
FROM [[<%title%>]]
WHERE contains(template, "note") 
SORT file.cday ASC
```

---
#### Internal Links
[[Courses]]
