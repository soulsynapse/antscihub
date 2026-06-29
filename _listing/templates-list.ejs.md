```{=html}
<ul class="list template-list">
<% for (const item of items) { %>
<li <%= metadataAttrs(item) %>><a href="<%- item.path %>" class="no-external"><%= item.title %></a>: <% if (item.description) { %><%= item.description %><% } %></li>
<% } %>
</ul>
```