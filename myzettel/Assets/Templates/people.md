<%*
let title = await tp.system.prompt("Person Name")
await tp.file.rename(title)
-%>
---
template: people
blog: 
youtube: 
twitter: 
github: 
email: 
linkedin: 
---
# <% title %>
> [!NOTE] Encounter
> How did you find or connect with this person?


## 📚 Linked Publications
```dataview
TABLE WITHOUT ID 
	link(file.path, file.aliases[0]) AS Title,
	template AS Type,
	progress AS Progress,
	link(url, "View ↗️") AS "Link"
FROM [[<% title %>]] 
WHERE 
	contains(template, "book") OR 
	contains(template, "course") OR 
	contains(template, "article")
```

---
#### Internal Links
[[<%tp.date.now("YYYY")%>]]