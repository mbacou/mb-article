```{=html}
<div>
  <% for (const item of items) { %>
    <div class="d-flex flex-md-row border-bottom">
      <div>
      <a href="<%- item.path %>">
      <img src="<%- item.thumbnail %>" alt="<%- item.description %>" class="img-fluid"/></a>
      </div>
      <div>
        <h3><a href="<%- item.path %>"><%= item.title %></a></h3>
        <p><%= item.description %></p>
        <ul class="navbar-nav d-flex flex-row gap-3 text-sans text-uppercase">
          <% for (const it of item.categories) %>
            <li class="nav-item fs-3 text-primary fw-bold"><%= it.name %></li>
          <% } %>
        </ul>
      </div>
      <div>
        <p>
          <%= item.date %><br />
          <% for (const it of item.authors) %>
          <%= it.name %><br />
          <% } %>
          <%= item.reading-time %><br />
        </p>
      </div>
    </div>
  <% } %>
</div>
```
