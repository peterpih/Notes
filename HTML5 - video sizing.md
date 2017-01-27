https://css-tricks.com/NetMag/FluidWidthVideo/Article-FluidWidthVideo.php

Including Google fonts, this line needs to go in &lt;head&gt; using the **style_sheet_tag**
<pre>
&lt;link href='//fonts.googleapis.com/css?family=Sofia' rel='stylesheet'&gt;
</pre>
for HAML
<pre>
= stylesheet_link_tag   'https://fonts.googleapis.com/css?family=Sofia', 'application'
</pre>

<pre>
&lt;h3 style="font-family:'Sofia'; font-style:italic;font-size:22px;text-transform:none;"&gt;&lt;center&gt;&lt;i&gt;In Memory of&lt;/i&gt;&lt;/center&gt;&lt;/h3&gt;
&lt;style&gt;
  .sofia {font-family: 'Sofia';font-size: 22px; text-transform:none;}
  .italic {font-style: italic;}
&lt;/style&gt;
</pre>
