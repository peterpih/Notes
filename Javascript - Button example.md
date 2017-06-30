
<pre>
&lt;!DOCTYPE html&gt;
  &lt;html&gt;
    &lt;body&gt;
      &lt;script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"&gt;&lt;/script&gt;
      
      &lt;script&gt;
        var buttonpress = function(){ alert('hello'); };

        $(document).ready(function(){
	        $("#first").click(function(){
	        alert('qwe');
	        });
        });
      &lt;/script&gt;

      &lt;h2>My First JavaScript&lt;/h2&gt;

      &lt;button type="button" onclick="document.getElementById('demo').innerHTML = Date()"&gt;First button</button&gt;

      &lt;button type="button" id='first'>Third button&lt;/button&gt;

      &lt;button type="button" onclick="buttonpress()">Second button&lt;/button&gt;

      &lt;p id="demo"></p&gt;

    &lt;/body&gt;
  &lt;/html&gt;
&lt;/pre>
