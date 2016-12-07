':something' is a string

'something:' is a symbol  
Whenever you would use a quoted string, use a symbol instead.

'=>' is a hash operator
<pre>
{ :minimum => 5 }
h = {'dog' => 'canine', 'cat' => 'feline', 'donkey' => 'asinine', 12 => 'dodecine'}  
h = {:dog => 'canine', :cat => 'feline', :donkey => 'asinine', 12 => 'dodecine'}   
h = {dog: 'canine', cat: 'feline', donkey: 'asinine', 12: 'dodecine'}  
</pre>
is a has with 'minimum' as its key and a value of 5.
