<pre>
&lt;html&gt;
  &lt;head&gt;...&lt;/head&gt;
  &lt;body&gt;
    &lt;input id='<b>eventClick</b>' type='button' value='click me!'&gt;
  &lt;/body&gt;
&lt;/html&gt;

document.getElementById('<b>eventClick</b>')   <em>target the object to listen to </em>

document.getElementById('<b>eventClick</b>').addEventListener('click')

<em> the <b>click</b> is from the on<b>click</b> method associated witht he object, just remove the <em><b>on</b></em>
</pre>
