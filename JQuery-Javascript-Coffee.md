###JQuery
[Change Button Function](http://stackoverflow.com/questions/15543482/change-the-buttons-function-with-jquery)

####JQuery is a library of javascript routines
####Coffee is the rails lightweight version of javascript

**jQuery UI**: http://jqueryui.com  

***for rails***
<pre>
# standard jQuery:
$(document).ready();

<b>$(document).ready(function(){</b>
  <em>code goes here</em>
<b>});</b>

# for rails use:
<b>$(document).on("page:change", -> </b>
</pre>

#JQuery
File extension is <b>.js</b> since it is <b><em>javascript</em></b>
Used for making effects (ie animations)  
https://pragmaticstudio.com/blog/2015/3/18/rails-jquery-ajax  

<pre>
<b>//</b> This is a comment

"cake"<b>.length</b>  #=> 4
</pre>

<pre>
&ltdiv id='green'&gt      # in HTML
&ltdiv class='red'&gt

#green {              # in .css
}
.red{
}

<b>$("</b>#green<b>")</b>           # in .js, '#' is for id's
<b>$('</b>.red<b>')</b>		# '.' is for class
</pre>

###Generalized jQuery setup
<pre>
<b>$(document).ready(function() {</b>
    $('<b>thingToTouch</b>').event(function() {
        $('<b>thingToAffect</b>').effect();
    });
<b>});</b>

$(<b>document</b>).ready(function() {
    $('<b>thingToTouch</b>').event(function() {
        $('<b>thingToAffect</b>').effect();
    });
});

where:
<b>document</b> is the entire document (focus)
<b>thing to touch</b> is the HTML element you'll click on, hover over, or otherwise interact with
<b>thing to affect</b> is the HTML element that fades away, changes size, or undergoes some other transformation
</pre>

###jQuery events
```
$('element').click();
	.dblclick();
	.hover();
	.keydown();
	.fadeTo('speed', delay);
	.animate({action}, time);
	.mouseover();
	.mouseenter();
	.mouseleave();
	
$(this).addClass('active');
	.hide();
```
###jQuery UI events
```
	.effect('explode');
	.accordion({collapsible: true, active: false);
	.effect('bounce', {times:3}, 500);
	.resizable();
	.selectable()
	.sortable()			# can move elements in a list around
```

###Example of form input
**html**
```
<!DOCTYPE html>
<html>
    <head>
    	<title>To Do</title>
        <link rel="stylesheet" type="text/css" href="stylesheet.css"/>
        <script type="text/javascript" src="script.js"></script>
	</head>
	<body>
		<h2>To Do</h2>
		<form name="checkListForm">
			<input type="text" name="checkListItem"/>
		</form>
		<div id="button">Add!</div>
		<br/>
		<div class="list"></div>
	</body>
</html>
```
**stylesheet.css**
```
h2 {
    font-family:arial;
}

form {
    display: inline-block;
}

#button{
    display: inline-block;
    height:20px;
	width:70px;
	background-color:#cc0000;
	font-family:arial;
	font-weight:bold;
	color:#ffffff;
	border-radius: 5px;
	text-align:center;
	margin-top:2px;
}

.list {
	font-family:garamond;
	color:#cc0000;
}
```
**script.js**  
```
$(document).ready(function(){
    $('#button').click(function(){
        var toAdd = $('input[name=checkListItem]').val();
        $(".list").append('<div class="item">'+ toAdd + '</div>');
    });
    $(document).on('click', '.item', function(){
        $(this).remove();
    });
});
```
###Example of getting keyboard input
**html**
```
<!DOCTYPE html>
<html>
    <head>
    	<title>Super Mario!</title>
        <link rel='stylesheet' type='text/css' href='stylesheet.css'/>
		<script type='text/javascript' src='script.js'></script>
	</head>
	<body>
        <img src="http://i1061.photobucket.com/albums/t480/ericqweinstein/mario.jpg"/>
	</body>
</html>
```
**stylesheet.css**
```
img {
    position: relative;
    left: 0;
    top: 0;
}
```
**script.js**
```
$(document).ready(function() {
    $(document).keydown(function(key) {
        switch(parseInt(key.which,10)) {
			// Left arrow key pressed
			case 37:
				$('img').animate({left: "-=10px"}, 'fast');
				break;
			// Up Arrow Pressed
			case 38:
				$('img').animate({top:"-=10px"}, 'fast');
				break;
			// Right Arrow Pressed
			case 39:
				$('img').animate({left:"+=10px"},'fast');
				break;
			// Down Arrow Pressed
			case 40:
				$('img').animate({top:"+=10px"},'fast');
				break;
		}
	});
});
```
