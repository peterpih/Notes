<b>Tips:</b>   
[Organizing CSS & Sass in Rails](http://www.mattboldt.com/organizing-css-and-sass-rails/)

[<h2>W3.org Cascading Style Sheets - home page</h2>](https://www.w3.org/Style/CSS/)

[<h2>W3 Tryit Editor</h2>](http://www.w3schools.com/html/tryit.asp?filename=tryhtml_default)

[HTML Code Table](http://www.ascii.cl/htmlcodes.htm)   
[Table of Special Escape Characters](http://www.degraeve.com/reference/specialcharacters.php)   
[Color Shades](http://www.w3schools.com/colors/colors_shades.asp)   

###Some Useful Tags  
<pre>
<b>&lt;sup&gt;</b> - superscript, like <sup>this</sup>  
<b>&lt;sub&gt;</b> - subscript, like <sub>this</sub>  
<b>placeholder=</b> - for that greyed out text inside form fields
<red>Hello</red>
</pre>
```{html}
<input label: "input form">
```
<html>
<input type="text" id="name" name="name"/>
</html>

[How to make a button look like a link](http://stackoverflow.com/questions/1367409/how-to-make-button-look-like-a-link) *Has info on default button styling*

[SASS vs SCSS which sytax is better](http://thesassway.com/editorial/sass-vs-scss-which-syntax-is-better)

[Display Operator Playground different types](http://quirksmode.org/css/css2/display.html)

###Tutorials
http://learn.shayhowe.com/html-css/
http://learnlayout.com


https://css-tricks.com/scale-svg/  
**reference:** http://www.w3schools.com/css/default.asp  
http://tutorials.jenkov.com/svg/image-element.html  

###General HTML layout
Always starts with `<!DOCTYPE html>`  
Always has `<html>...</html>` as first and last tags  
Always has `<head>...</head>`, and `<body>...</body>` which go inside `<html>..</html>`  
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
    &lt;head&gt;
      &lt;title&gt;<em>Title of the webpage here, shows on the browser tab</em>&lt;title&gt;
      &lt;style&gt;
          <em>CSS styling can go here, but is in a separate file in RoR</em>
      &lt;/style&gt;
      <em>Google Analytics tags usually go here, just before the closing &lt;/head&gt;</em>
    &lt/head&gt;
    &lt;body&gt;
      <em>The main webpage goes here</em>
    &lt;body&gt;
&lt;/html&gt;
</pre>

Example:  
```
<!DOCTYPE html>
<html>
    <head>
        <title>
        </title>
        <h1>This is a big heading</h1>
    <head>
    <body style="background-color:red">
        <p>This is a paragraph</p>
        <ol>
            <li style="color:blue">first item in ordered list</li>
            <li style="font-size:20px">second item in ordered list</li>
            <li style="font-family:Arial">third item in ordered list</li>
            <li style="font-size=30px; color:orange; font-family:Verdina">fourth item in ordered list</li>
        </ol>
        <ul>
            <li>first item in unordered list</li>
            <li>second item in unordered list</li>
        </ul>
    </body>
</html>
```
**Include a link**
```
<a href="put url here">"some label here"</a>

In the .css can format the link:
a {
  text-decoration: none   <!-- will not show the underline -->
  color: red              <!-- change the color of the text -->
}
```
**Include an image**
```
<img src="image url here">
```
**Text Alignment**
```
style="text-align:center"
style="text-align:right"
stype="text-align:left"
```
**Bold**
```
<strong>
</strong>
```
**Italics**  
```
<em>
</em>
```
**Tables**  
table header area `<theader>...</theader>`  
table header `<th>...</th>`  
table rows `<tr>...</tr>`  
table data `<td>...</td>`  
```
<table>
  <theader>
    <tr>
      <th colspan="3">Title across 3 columns</th>
    </tr>
  </theader>
    <tr>
      <td>creates column 1</td>
      <td>creates column 2</td>
      <td>creates column 3</td>
    </tr>
    </tr>
    
</table>
```
```
<table style="border-collapse:collapse>

table { <!-- in css -->
  border: 1px dashed blue;
}
```
###CSS  
`selector`s are any HTML element  
```
selector {
  property: value;
}
```
**Include CSS stylesheets**  
```
<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
```

###Making a Button
```
div {
    height: 50px;
    width: 120px;
    border-color: #6495ed;
    background-color: #bcd2ee;
    border-style: dashed;
    border-width: 2px;
    border-radius: 5px;  <!--- detemines how rounded the corners are --->
    margin: auto;
    text-align: center;
}
```
#Choose All Elements  
```
* {
}
```
**Nesting Elements**  
```
body ul li{
}
body ul li p {
}
```

###id=  
Use for when **one** element needs a certain styling  
```
<body id="myid">...</body>
<p id="myid">...</p>

<!--- in the .css --->
#myid {
  selector: property;
}
```

###class=  
Use when several different elements have the same styling  
```
<body class="mystyle">...</body>
<p class="mystyle">...</p>

<!--- in the .css --->
.mystyle {
  selector: property;
}
```
###pseudo-class selectors for links  
`a:link`  
`a:visited`  
`a:hover`  

`p:first-child`  
`p:nth-child(n)`  

###HTML block layout   
`block:block` the default, blocks take up an entire line  
`block:inline-block` blocks can sit next to each other  
`block:inline` they all sit on top of each other on the same line  
`block:none` they all disappear  

**margin**  
To center:  `margin: auto`  
`margin-top: 10px`  
`margin-right: 20px`  
`margin-bottom: 30px`
`margin-left: 40px`  
Can also be specified on one line, going counter-clockwise as:  
`margin: 10px 20px 30px 40px`  
Can also be done for:  
`padding`  


**Floating Boxes**  
`float: right`  
`float: left`  
`clear: right` makes sure no floating elements to the right   
`clear: left` makes sure no floating elements to the left  
`clear: both` makes sure no floating elements either side  

**Position**  
`position: relative` position relative to html (the page) not what it's in  
`position: absolute`  position relative to what it's in ie body  
`position: fixed`  does not scroll

