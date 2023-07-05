<%*
let title = await tp.system.prompt("Article Title")
let author = await tp.system.prompt("Author's Name")
let url = await tp.system.prompt("Article URL")
await tp.file.rename(title)
-%>
---
template: article
progress: 0%
priority: 0.0
url:: <% url %>
author: <% author %> 
---
# [<% title %>](<% url %>)
Published by: [[<% author %>]] 



## 📚 Linked Notes
```dataview
LIST WHERE contains(template, "note") AND contains(source, "<% url %>")
```

---
#### Internal Links
[[Articles]]
