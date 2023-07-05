<%*
let title = await tp.system.prompt("Note Title")
await tp.file.rename(title)
-%>
---
template: note
---
<% tp.web.random_picture("900x300", "tree,landscape,water,mountain") %>

(date:: <%tp.date.now("YYYY-MM-DD") %>) | (time:: <%tp.date.now("HH:mm") %>) | (weather:: <% tp.user.getWeather() %>)

# <% title %>



---
## Internal Links
[[<%tp.date.now("YYYY-MM-DD")%>]]