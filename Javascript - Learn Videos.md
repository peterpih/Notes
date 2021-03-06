<h1>Video Code Camps:</h1>  

[How To Add jQuery and Ajax To Your Rails App - Pragmatic Sutdio](https://www.youtube.com/watch?v=K-sns5tNdTY)


https://www.linkedin.com/learning/learning-full-stack-javascript-development-mongodb-node-and-react?storeRef=voyager_feed_cymbii_learning&trk=n-feed-course-learning

[Javascript Mini BootCamp](https://lambdaschool.com/mini-bootcamp/javascript)   
[Javascript Tutorial For Beginners](https://www.youtube.com/watch?v=e57ReoUn6kM&list=PLoYCgNOIyGACnrXwo5HMCfOH9VT05znGv&index=6)

Packet Publishing Book of the Day
Javascript Challenges (tcorral on Github)

Egghead
Nodeschool.io


###Online Tutorials
####[Free Code Camp](https://www.freecodecamp.com)  
####[Javascript for Cats](http://jsforcats.com)

####[Codeacademy Labs](http://labs.codecademy.com)  

####[Code Kata](http://codekata.com)  
####[Project Euler](https://projecteuler.net)  

###Other
####[Javascript Command Line Instructions](http://javascriptplayground.com/blog/2015/03/node-command-line-tool/)
###[CodeAcademy Javascript Tutorial](https://www.codecademy.com/courses/objects-ii/0/1?curriculum_id=506324b3a7dffd00020bf661)

####var vs let  
The scope for 
<pre>
<b>var<b> x = 25;


###Language
####Operators
<pre>
<b>+, -, /, *, %</b> <em>standard unary operators</em>
<b>+=</b> <em>plus equals</em>
<b>-=</b> <em>minus equals</em>
<b>&&</b> <em>logical AND</em>
<b>||</b> <em>logical OR</em>

<b>//</b> <em>comment</em>
<b>++, --</b>

<b>&gt;</b>
<b>&lt;</b>
<b>===</b> <em>equal to</em>
<b>!==</b> <em>not equal to</em>
<b>&gt;=</b>  
<b>&lt;=</b>  

<b>var</b> emptyObject = <b>{}</b>
<b>var</b> emptyArray = <b>[]</b>
</pre>

####Methods
<pre>
<em>string</em>.<b>length</b>  <em>length of the string</em>
<em>string</em>.<b>substring</b>(<em>start, end</em>);
<em>string</em>.<b>split</b>(<em>delimiter, count</em>);
<em>string</em>.<b>toLowerCase()</b>

<b>String.fromCharCode</b>( <em>character</em> );
<b>String.charCodeAt</b>( <em>position</em> );

<em>array</em>.<b>push</b>( ... );

</pre>

###Javascript Events
<pre>
var element = document.getElementById('some-id')   
element.addEventListener("blur", function(){
<em>some code goes here</em>
    alert('hi');
}

click  
mouseenter  
mouseleave  
mousedown  
mouseup  
mousemove  
keydown  
keyup  
blur  
focus  
</pre>

####Number Conversions
<pre>
parseFloat(string,radix) → convert a string (➢ for example: "3.14") to a decimal number. radix defaults to 10.
parseInt("324")  // ⇒ 324

(number).toString(radix) → convert a number to string. radix defaults to 10.
(30).toString()             // ⇒ "30"
</pre>

####Currency Conversions
<pre>
(2500).toLocaleString("en-GB", {style: "currency", currency: "GBP", minimumFractionDigits: 2})
(2500).toLocaleString("en-US", {style: "currency", currency: "USD", minimumFractionDigits: 2})  // $2,500.00
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

<b>var</b> myObject = {
  name: 'Eduardo',
  type: 'Most excellent',
  interests: [1,2,3]
};

// constructor construction
<b>function</b> functionName( <em>arguments</em> ){
    <b>this</b>.<em>key</em> <b>=</b> <em>value</em>
};

<b>function</b> Person(job, married) {
    <b>this</b>.job = job;
    <b>this</b>.married = married;
}

// create a "gabby" object using the Person constructor!
var gabby = new Person("student", true);

<b>var</b> anObject = <b>function<b>( ... ) {
    <b>this</b>.<em>key</em> = <em>value</em>;
    <b>this</b>.<em>method</em> = <b>function</b>( <em>value</em> ) {
        <b>this</b>.<em>key</em> = <em>value</em>;
    };
};
</pre>

Use a function with an object
<pre>
var setAge = function (newAge) {
  this.age = newAge;
};

Bob.setAge(50);


var setAge = function (newAge) {
  this.age = newAge;
};

var susan = new Object();
susan.age = 25;
susan.setAge = setAge;
susan.setAge(35);
</pre>

####Modifying Objects
<pre>
  <b>function</b> <em>objectName</em> ( <em>arguments</em> ) {
    <b>this</b>.<em>key</em> = <em>value</em>;
  };
  
  <b>var</b> myObj = <b>new</b> <em>objectName</em>( <em>arguments</em> );
  myObj.<b>prototype</b>.<em>methodName</em> = <b>function</b>() {
    ...
  };
  myObj.<em>methodName</em>();
</pre>

####Branching
<pre>
<b>if</b> ( <em>condition</em> ){  
    ...
}
<b><em>else if</b> ( <em>condition</em> ){
    ...
{</em>
<b>else</b>{
    ...
}
</pre>

####Functions
<pre>
<b>var</b> <em>functionName</em> = <b>function</b>(<em>argument(s)</em>){
    ...
    <b>return</b>( ... );
};

<em>functionName</em>(<em>argument(s)</em>);  
</pre>

####For Loops
<pre>
<b>for</b> (<b>var</b> i = <em>start</em>; i<10; i++){
    ...
};
</pre>

####Arrays
Start at 0 (zero) index
<pre>
<b>var</b> anArray = [1, 2, 3, 4]; <em>one-dimensional arrays</em>  
<b>var</b> anArray = [[1,1], [2,2], [3,3]]; <em>two-dimensional arrays</em>
<b>var</b> myArray=[1,<b>true</b>, "hello", {name: "Peter"}];  <em>mixed array</em>
<b>var</b> newArray=[[1,1],[2,2,2,2],[3,3], [{word: "hello"}]];
</pre>

###While, Do Loops
<pre>
<b>while</b>(<em>condition</em>){
    ...
};

<b>do</b>{
    ...
}<b>while</b>(<em>condition</e>);
</pre>

####Switch
<pre>
<b>switch</b>(<em>expression</em>) {
    <b>case</b> <em>condition1</em>:
        ...
        <b>break</b>;
    <b>case</b> <em>condition2</em>:
        ...
        <b>break</b>;
    <b>default</b>:
        ...
};
</pre>
