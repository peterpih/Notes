[HAML Main Site](haml.info)
[HAML Yardoc](http://haml.info/docs/yardoc/  )
[Sitepoint: Introduction to HAML](http://www.sitepoint.com/an-introduction-to-haml/)


###In-line styling
<pre>
put a smaller button on the same line as a headline

%h1 Users #{link_to button_tag('New User'), new_user_path, class:'small_label'}
</pre>

###Multi-line
End the line with either a ","(comma) or " |"(space bar)


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
