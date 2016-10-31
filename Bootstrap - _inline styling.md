###In-line styleing depending on situation

<b>HTML</b>
<pre>
&lt;div <b>color="red"</b>&gt
</pre>

<b>HAML</b>
<pre>
%div<b>{color: 'red'}</b>
</pre>

<b>link_to</b>
<pre>
= link_to 'a_link', "#", <b>'border-style'=>'solid', 'color'=>'red'</b>
</pre>
