###[CodeAcademy Javacript Tutorial](https://www.codecademy.com/courses/objects-ii/0/1?curriculum_id=506324b3a7dffd00020bf661)

####Operators
<pre>
<b>+, -, /, *, %</b> <em>standard unary operators</em>
<b>+=</b> <em>plus equals</em>
<b>-=</b> <em>minus equals</em>
<b>&&</b> <em>logical AND</em>
<b>||</b> <em>logical OR</em>
<b>//</b> <em>comment</em>

<b>&gt;</b>
<b>&lt;</b>
<b>===</b> <em>equal to</em>
<b>!==</b> <em>not equal to</em>
<b>&gt;=</b>  
<b>&lt;=</b>  
</pre>

####Methods
<pre>
<em>string</em>.<b>length</b>  <em>length of the string</em>
<em>string</em>.<b>substring</b>(<em>start, length</em>)

</pre>

####Messages
<pre>
<b>alert</b>( <em>message</em> );  
<b>confirm</b>( <em>message</em> );  
<b>prompt</b>( <em>message</em> );  
<b>var</b> inputName = <b>prompt</b>("What is your name?");
</pre>

####Output
<pre>
    <b>console.log</b>( ... );
</pre>


####Object Construction

<pre>
// literal construction
var james = {
    // add properties to this object!
    job: "programmer",
    married: false
};

// constructor construction
function Person(job, married) {
    this.job = job;
    this.married = married;
}

// create a "gabby" object using the Person constructor!
var gabby = new Person("student", true);
</pre>

####Branching
<pre>
<b>if</b> ( <em>boolean</em> ){  
    ...
}
<b><em>else if</b> ( <em>boolean</em> ){
    ...
{</em>
<b>else</b>{
    ...
}
</pre>
