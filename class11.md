# EJS (Embedded JavaScript templates)
EJS is a simple templating language that lets you generate HTML markup with plain JavaScript.

1. Installation:
`$ npm install ejs`

2. Features
- Control flow with ` <% %> `
- Escaped output with ` <%= %> ` (escape function configurable)
- Unescaped raw output with ` <%- %> `
- Newline-trim mode ('newline slurping') with ` -%> ` ending tag
- Whitespace-trim mode (slurp all whitespace) for control flow with ` <%_ _%> `
- Custom delimiters `<? ?>` instead of `<% %>`
- Includes
- Client-side support
- Static caching of intermediate JavaScript
- Static caching of templates
- Complies with the Express view system

- Layouts
EJS does not specifically support blocks, but layouts can be implemented by including headers and footers, like so:

```JavaScript
{
<%- include('header') -%>
<h1>
  Title
</h1>
<p>
  My page
</p>
<%- include('footer') -%>
}
```


3. Node Setup
```JavaScript
{
    // server.js
// load the things we need
var express = require('express');
var app = express();

// set the view engine to ejs
app.set('view engine', 'ejs');

// use res.render to load up an ejs view file

// index page 
app.get('/', function(req, res) {
    res.render('pages/index');
});

// about page 
app.get('/about', function(req, res) {
    res.render('pages/about');
});

app.listen(8080);
console.log('8080 is the magic port');
}
```

4. Start Up our Server
`$ node server.js`

5. EJS Partials footer.ejs, head.ejs, header.ejs
6. Using EJS Partials

### looping
```JavaScript
{
    <ul>
    <% drinks.forEach(function(drink) { %>
        <li><%= drink.name %> - <%= drink.drunkness %></li>
    <% }); %>
</ul>
}
```