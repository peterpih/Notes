[Ruby Tutorials: Regexp](http://www.tutorialspoint.com/ruby/ruby_regular_expressions.htm)
[www.regular-expressions.info](http://www.regular-expressions.info)

StackExchange:  
[Named Parameters](http://stackoverflow.com/questions/15308163/named-parameters-in-ruby-2)  
[Keyword Arguments](http://stackoverflow.com/questions/19945329/rubykoans-113-282-type-mismatchstring-given-how-could-i-have-solved-myself)  
[Possesive Quantifiers](http://stackoverflow.com/questions/1117467/can-someone-explain-possessive-quantifiers-to-me-regular-expressions)  
[What do ++ and *+ mean](http://stackoverflow.com/questions/17064108/what-do-and-mean-in-a-regular-expression/17064242#17064242)  
[Regex Reference](http://stackoverflow.com/questions/22937618/reference-what-does-this-regex-mean/22944075#22944075)  

[Rubular.com](www.rubular.com)

<h2>REGEX for email validation</h2>
<pre>
VALID_EMAIL_REGEX='/\A[\w+\-.]+@[a-z\d\-.]+\.[a-z]+\z/i'
</pre>

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
