# Components 
### Partials
Partials are  pieces  of code that can be used across the website without the need to rewrite them.

such as footer and header and since they should be on each page, using partials will solve the problem

of repeating the code over and over. Instead, we write in one place and render it whenever we need to

and when you need to update the content, you do it in one place which leads to saving time, and less code.

```html 
  <!-- views/partials/navbar.ejs -->
  <div class="header clearfix">
      <nav>
          <ul class="nav nav-pills pull-right">
              <li role="presentation"><a href="/">Home</a></li>
          </ul>
          <h3 class="text-muted">Node.js Blog</h3>
      </nav>
  </div>
```

in the above example we see that the header nav bar code has been added inside partials folder with the views folder.

so when ever you need this piece of code, you can include it as shown below

```html
.
.
.
<body>
  <header>
    <!-- including the nav bar in the header -->
    <%- include('partials/navbar') %>
      .
      .
      .
  </header>
</body>

```