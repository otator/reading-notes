# <%= EJS %>
 **EJS** is a simple templating language that lets you generate HTML markup with plain JavaScript. No religiousness about how to organize things. No reinvention of iteration and control-flow. It's just plain JavaScript. [link](https://ejs.co/)

  * To install EJS using node package manager *npm*.
    * `npm install ejs`

  * Require Ejs in code
    * `const ejs = require('ejs')`

**if** statement using EJS:

```javascript
<% if (user) { %>
  <h2><%= user.name %></h2>
<% } %>
```

adding **for** loop using EJS:

```javascript
<% for( var i=0; i < name.length; i++) { %>
     <li>
          <%= names[i] %>
    </li >
<% } %>
```


  

