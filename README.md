# <p align="center"><img src="https://github.com/Mc0Shell/CodeSnippetBuilder/assets/55066055/d216011c-32d0-4fa5-861e-281d030728c1" alt="Image" width="300" height="300"></p>

<p align="center">
  <h2><b>CodeBlockBuilder is a powerful software tool designed to simplify web development by generating code blocks in various languages such as HTML, JavaScript, and CSS.</b>
  </h2>
</p>
<br>


CodeBlockBuilder serves as a versatile framework for both general graphical elements and seamless inter-page processes, including complex logical operations.

With this software, developers can easily streamline their workflow, accelerate development time, and create dynamic and visually appealing web applications without the need for extensive backend programming knowledge. 

Experience the convenience and efficiency of CodeBlockBuilder and bring your web projects to life with ease.

<br><br><hr><br>

# Docs
<b> <h3>How to start </h3></b>
<h4> To generate a page you must first import the CSS style and the two JS files.
The first JS file creates the webBuilder structure, the second file initializes it, furthermore it is necessary to create a further script to insert all the commands which will then generate the page.</h4>
```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="/CodeSnippetBuilder/css/style.css ?>"></style>
  </head>
  <body>  		
    <div id="generatedPage"></div>
        
    <script src="/CodeSnippetBuilder/WebBuilder.js"></script>
    <script src="/CodeSnippetBuilder/main.js"></script>
    <script>
      // Initialize the WebBuilder
      const webBuilder = initWebBuilder();

     // Add a navbar block
     webBuilder.addHTMLBlock("navbar", {
       'Logo':'/img/logo/logo2.png', 
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

<b> Is possible to interact with every element in the page, all in JS </b>

<h2>Topbar calls</h2>

- Switch navbar block colors (<id_navbar>, <navbar_background>, <navlink_color>, <navlink_color_hover>)

        webBuilder.editNavbarColors('navbarB', 'navlink', "blue", "white", "blue");
