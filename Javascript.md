###[CodeAcademy Javacript Tutorial](https://www.codecademy.com/courses/objects-ii/0/1?curriculum_id=506324b3a7dffd00020bf661)

####Operators
<pre>
<b>+=</b> <em>plus equals</em>
<b>-=</b> <em>minus equals</em>
<b>&&</b> <em>logical AND</em>
<b>||</b> <em>logical OR</em>
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
