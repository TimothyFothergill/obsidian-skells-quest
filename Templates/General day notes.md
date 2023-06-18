<% await tp.file.move("Tasks/" + tp.date.now("M") + "." + tp.date.now("DD-MM-YY") + "/" + tp.file.title) %>
<% await tp.file.rename("General day notes") %>
Date: <% tp.date.now("DD-MM-YYYY") %>
**Work timings**

Start: <% tp.date.now("HH\:mm") %>
End: <% tp.date.now("HH\:mm") %>

**Notes:**
