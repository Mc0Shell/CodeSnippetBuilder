# <p align="center"><img src="https://github.com/Mc0Shell/CodeSnippetBuilder/assets/55066055/8297b366-7714-4b47-ad62-ab3b44214d7b" alt="Image" width="450" height="450"></p>

<p align="center">
  <h2><b>CodeSnippetBuilder is a powerful software tool designed to simplify web development by generating code blocks in various languages such as HTML, JavaScript, and CSS.</b>
  </h2>
</p>
<br>
## STATUS: Under developing


CodeSnippetBuilder serves as a versatile framework for both general graphical elements and seamless inter-page processes, including complex logical operations.

With this software, developers can easily streamline their workflow, accelerate development time, and create dynamic and visually appealing web applications without the need for extensive backend programming knowledge. 

Experience the convenience and efficiency of CodeSnippetBuilder and bring your web projects to life with ease.

<br><br><hr><br>

# Docs
<b> <h3>How to start </h3></b>
To generate a page you must first import the CSS style and the two JS files.<br>
The first JS file creates the webBuilder structure, the second file initializes it, furthermore it is necessary to create a further script to insert all the commands which will then generate the page.

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="/CodeSnippetBuilder/css/style.css"></style>
    <link rel="icon" href="/img/logo/logo.png" type="image/x-icon">
  </head>
  <body id="generatedPage">   
    <script src="/CodeSnippetBuilder/WebBuilder.js"></script>
    <script src="/CodeSnippetBuilder/main.js"></script>
    <script>
      // Initialize the WebBuilder
      const webBuilder = initWebBuilder();

      // Add a navbar block
      webBuilder.addHTMLBlock("navbar", "topbar", {
        'Logo':'/img/logo/logo.png', 
        'Home':'/', 
        'Docs':'/docs',
        'Downloads':'/downloads',
        'About':'/about'
      });
           
      // Render the page with the added and/or modified blocks
      webBuilder.insertGeneratedPage('generatedPage');
    </script>
  </body>
</html>
```

In development mode you need to force the reload of the css and js files adding the timestamp in the file url

    ?timestamp=<?php echo time(); ?>

```html
<link rel="stylesheet" href="/CodeSnippetBuilder/css/style.css?timestamp=<?php echo time(); ?>"></style>
<script src="/CodeSnippetBuilder/WebBuilder.js?timestamp=<?php echo time(); ?>"></script>
<script src="/CodeSnippetBuilder/main.js?timestamp=<?php echo time(); ?>"></script>
```
    
<hr>

<h2> Navbar / Topbar </h2>

<h3> Add a new navbar block </h3>

```
webBuilder.addHTMLBlock(<id>, <blockName>, {<Label>:<url>})
```

```javascript
webBuilder.addHTMLBlock("navbar", "topbar", {
    'Logo':'/img/logo/logo.png', 
    'Home':'/', 
    'Docs':'/docs',
    'Downloads':'/downloads',
    'About':'/about'
});
```
<h3>Calls</h3>

```
Switch navbar block colors (<id_navbar>, <navbar_background>, <navlink_color>, <navlink_color_hover>)
```

```javascript
webBuilder.editNavbarColors('navbarB', 'navlink', "blue", "white", "blue");
```
