
### https://d3js.org  

###[City of Oakland proposed budget](http://openbudgetoakland.org/2015-17-proposed-budget-flow.htm)  

###[D3 Tutorial](https://www.dashingd3js.com/table-of-contents)

###[Combining R and D3](http://blog.ae.be/combining-the-power-of-r-and-d3-js/)

###The following 3 code blocks are equivalent
Kind of long:
<pre>
d3.select("body").append("svg").attr("width", 50).attr("height", 50).append("circle").attr("cx", 25).attr("cy", 25).attr("r", 25).style("fill", "purple");
</pre>

Better readability:
<pre>
d3.<b>select</b>("body")
  .<b>append</b>("svg")
  .<b>attr</b>("width", 50)
  .<b>attr</b>("height", 50)
  .<b>append</b>("circle")
  .<b>attr</b>("cx", 25)
  .<b>attr</b>("cy", 25)
  .<b>attr</b>("r", 25)
  .<b>style</b>("fill", "purple");
</pre>
 
Best:
<pre>
<b>var</b> bodySelection = d3.<b>select</b>("body");

<b>var</b> svgSelection = bodySelection.<b>append</b>("svg")
      .attr("width", 50)
      .attr("height", 50);

var circleSelection = svgSelection.append("circle")
      .attr("cx", 25)
      .attr("cy", 25)
      .attr("r", 25)
      .style("fill", "purple");
</pre>

D3 has functions to read  CSV, XML, JSON data formats

####Binding data
<pre>
  <b>function</b> (d) { <b>return</b> d; }
</pre>

###SVG Objects

####Circles
In HTML
<pre>
  &lt;svg width="50" height="50"&gt;
    &lt;circle cx="25" cy="25" r="25" fill="purple" /&gt;
  &lt;/svg&gt;
</pre>
In D3

<pre>
//Make an SVG Container
var svgContainer = d3.select("body").append("svg")
                                    .attr("width", 200)
                                    .attr("height", 200);

//Draw the Circle
var circle = svgContainer.append("circle")
                         .attr("cx", 30)
                         .attr("cy", 30)
                         .attr("r", 20);
</pre>

####Rectangles
In HTML
<pre>
  &lt;svg width="50" height="50"&gt;
    &lt;rect x="0" y="0" width="50" height="50" fill="green" /&gt;
  &lt;/svg&gt;
  
//Make an SVG Container
var svgContainer = d3.select("body").append("svg")
                                    .attr("width", 200)
                                    .attr("height", 200);

//Draw the Rectangle
var rectangle = svgContainer.append("rect")
                            .attr("x", 10)
                            .attr("y", 10)
                            .attr("width", 50)
                            .attr("height", 100);
</pre>
