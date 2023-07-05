<%*
let fileName = await tp.system.prompt("Book Title")
let author = await tp.system.prompt("Author's Name")
await tp.file.rename(fileName)
-%>
---
template: book
progress: 0%
url:: 
author: <% author %> 
---
# <% fileName %>
###### [[|Read the book]]


## 📚 Linked Notes
```dataview
LIST 
	FROM [[<% fileName %>]] 
WHERE contains(template, "note")
```

---
#### Internal Links
[[Books]]
