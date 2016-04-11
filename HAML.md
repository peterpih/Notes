[HAML Main Site](haml.info)
[HAML Yardoc](http://haml.info/docs/yardoc/  )
[Sitepoint: Introduction to HAML](http://www.sitepoint.com/an-introduction-to-haml/)

HAML does not use <b><tag> ... </tag></b>, it uses indentation instead  
'''
    &lt;a href="www.example.com"&gt;Button Text</a>
'''
<pre>
In HTML:
&lt;div&gt;
  &lt;a href="www.example.com"&gt;Button Text&lt;/a&gt;
&lt;/div&gt;

in HAML:
%div
  %a{ href: "www.example.com"}
    = "Button Text"
</pre>

<b>%p</b> <em>This is a paragraph</em>
<b>-</b>  <em>( dash - for code to be executed )</em>

<b>=</b>  <em>( equals sign - for code to be executed / displayed )</em>
<pre>
<b>=</b> button(...)
<b>=</b> link_to (...)
</pre>

<b>%p=</b>  <em> ( for code to be displayed in a paragraph )</em>
<pre>
%p= "This is some text"

= button(...)
  = "Some text to go in a button
</pre>
