https://css-tricks.com/NetMag/FluidWidthVideo/Article-FluidWidthVideo.php

#[Sample Google fonts here](http://www.w3schools.com/howto/howto_google_fonts.asp)
Including Google fonts, this line needs to go in &lt;head&gt; using the **style_sheet_tag**
<pre>
&lt;link href='//fonts.googleapis.com/css?family=Sofia' rel='stylesheet'&gt;
</pre>
for HAML
<pre>
= stylesheet_link_tag   'https://fonts.googleapis.com/css?family=Sofia', 'application'
</pre>

Transform this complicated line
<pre>
&lt;h3 style="font-family:'Sofia'; font-style:italic;font-size:24px;"&gt;&lt;center&gt;&lt;i&gt;In Memory of&lt;/i&gt;&lt;/center&gt;&lt;/h3&gt;
</pre>
to this .scss
<pre>
&lt;style&gt;
  .sofia {font-family: 'Sofia';font-size: 24px; text-transform:none;}
  .italic {font-style: italic;}
  .pt24 {font-size: 24px;}
&lt;/style&gt;
</pre>
and this "magic" line
<pre>
&lt;h3 class="sofia italic pt24"&gt;In Memory of&lt;/h3&gt;
</pre>
