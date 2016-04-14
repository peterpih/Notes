[Ruby Tutorials: Regexp](http://www.tutorialspoint.com/ruby/ruby_regular_expressions.htm)

General pattern is delimited
<pre>
<b>/</b><em>pattern</em><b>/</b>   
<b>!</b><em>pattern</em><b>!</b>

<em>can be prefixed by:</em>
<b>%r</b>  
<b>%r</b>/st/.match('this is a test') <em>=> #&lt;MatchData "st"&gt;</em>
</pre>

Options can be specified
<pre>
<em>/pattern/option</em>
</pre>

where option is

Control Characters are
<pre>
+ ? . * ^ $ ( ) [ ] { } | \
</pre>

Methods
<pre>
<b>.match(</b><em>string</em><b>)</b> <em>( match the entire string )</em>
<b>.sub(</b><em>regexp</em><b>,</b><em>substitute-string<em><b>)</b>  <em>( substitute string )</em>
<b>.sub!(</b><em>regexp</em><b>,</b><em>substitute-string<em><b>)</b>  <em>( substitute string with replace )</em>
<b>.gsub(</b><em>regexp</em><b>,</b><em>substitute-string<em><b>)</b>  <em>( globally replace a string )</em>
<b>.gsub!(</b><em>regexp</em><b>,</b><em>substitute-string<em><b>)</b> <em>( globally replace a string with replace )</em>
</pre>
