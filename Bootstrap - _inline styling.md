###In-line styleing depending on situation

<b>HTML</b>
<pre>
&lt;div <b>color="red"</b>&gt
</pre>

<b>HAML</b>
<pre>
%div<b>{color: 'red'}</b>

%li<b>{style: "border: 1px solid red"}
</pre>

<b>link_to</b>
<pre>
= link_to 'a_link', "#", <b>style: 'border-style:solid;color:red'</b>
= link_to 'a_link', "#", <b>'border-style'=>'solid', 'color'=>'red'</b>
</pre>

<b>Useful Styling</b>
<pre>
<b>border: 1px solid red</b>      <em># shorthand border</em>
</pre>
