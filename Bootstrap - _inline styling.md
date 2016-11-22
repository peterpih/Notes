###In-line styling depending on situation

<b>HTML</b>
<pre>
&lt;div <b>color="red"</b>&gt
&lt;div <b>style="{border: 1px solid red}"</b>&gt
</pre>

Some different ways of doing it (beware parens and curlies)
<pre>
%div.some{ :style => "position: absolute; left: 300px; top: 300px;" }
%div.some(style='position: absolute; left: 300; top: 300;')
.some{ style: 'position: absolute; left: 300px; top: 300px;' }
%div{ style: { display: "none", width: "50px" } }
</pre>

<b>HAML</b>
<pre>
%div<b>{color: 'red'}</b>

%li<b>{style: "border: 1px solid red"}</b>
%li<b>{style: "border-style:solid;border-color:red"}</b>
</pre>

<b>link_to</b>
<pre>
= link_to 'a_link', "#", <b>style: 'border:4px solid green'</b>
= link_to 'a_link', "#", <b>:style=>'border:4px solid green'</b>
</pre>

<b>Some Useful Styling</b>
<pre>
<b>border: 1px solid red</b>      <em># shorthand border</em>

<b>list-style: none</b>          <em> # no bullet points in list item</em>
<b>list-style-type: none</b>

<b>width: max-content;</b> 
</pre>
