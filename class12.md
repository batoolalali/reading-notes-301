# EJS Partials
functions, they make large websites easier to maintain as you don’t have to go and change a piece of text in every page it appears in.

Creating and including partials is very straightforward with EJS.

### EJS Partials 
- footer.ejs 
- head.ejs
- header.ejs

######  footer.ejs


```HTML
{
<!-- views/partials/footer.ejs -->
    <footer class="footer">
        <p>© 90210 Lawyer Stuff.</p>
    </footer>
}
```

######  head.ejs

```HTML{
<!-- views/partials/head.ejs -->
<meta charset="UTF-8">
<title>Super Awesome</title>

<!-- CSS (load bootstrap from a CDN) -->
<link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css">
<style>
    body    { padding-top:50px; }
</style>
}
```

###### header.ejs 

```HTML{
    <!-- views/partials/header.ejs -->

<nav class="navbar navbar-default" role="navigation">
<div class="container-fluid">

    <div class="navbar-header">
        <a class="navbar-brand" href="#">
            <span class="glyphicon glyphicon glyphicon-tree-deciduous"></span>
            EJS Is Fun
        </a>

        <ul class="nav navbar-nav">
            <li><a href="/">Home</a></li>
            <li><a href="/about">About</a></li>
        </ul>
    </div>

</div>
</nav>
}
```