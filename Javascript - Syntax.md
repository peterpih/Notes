<h2>Arrays</h2>
var array = [1,2,3,4];  
<pre>
 [1, 2, 3, 4]
 </pre>
 
array.<b>shift();</b>   
<pre>
&gt; array
(3) [2, 3, 4]
</pre>

array.<b>unshift(9);</b>   
<pre>
4
&gt; array
(4) [9, 2, 3, 4]
</pre>

array.splice(1,2);
<pre>
(2) [2, 3]
</pre>

array.<b>push</b>  - <em>add tot he end of array </em>   
array.<b>splice(<em>start, delete-count, additional-value1, additional-value2, ....</em>);   

<h2Logical operators</h2>
<pre>
<b>20 == "20" </b> - <em>"20" gets converted to a number and then is compared</em>
true

<b>20 === "20"</b> - <em>both value and type must be the same</em>    
false

<b>||</b> - <em>logical OR</em>
<b>&&</b> - <em>logical AND</em>
</pre>

<h2>Operator precedence</h2>   
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence

<h2>Loops</h2>
<pre>
Arrays   
<b>for( var i=0; i<array.length; i++;){ ... }</b>

Hashes  
obj = {color: "read", height: 200, length: 100};   <em> the hash</em>    
k = Object.keys( obj )   <em>get the keys fo the hash</em>    
for (var i=0; i<k.length; i++){    
 console.log( obj[k[i]] );    
}

<b>for in</b>
</pre>

<h2>This keyword</h2>
