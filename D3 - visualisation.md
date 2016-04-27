
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

####Ellipse
In HTML
<pre>
  &lt;svg width="50" height="50"&gt;
    &lt;ellipse cx="25" cy="25" rx="15" ry="10" fill="red" /&gt;
  &lt;/svg&gt;
  
  
//Make an SVG Container
var svgContainer = d3.select("body").append("svg")
                                    .attr("width", 200)
                                    .attr("height", 200);

//Draw the Ellipse
var circle = svgContainer.append("ellipse")
                         .attr("cx", 50)
                         .attr("cy", 50)
                         .attr("rx", 25)
                         .attr("ry", 10);
                         
</pre>

####Straight Line
<pre>
  &lt;svg width="50" height="50"&gt;
    &lt;line x1="5" y1="5" x2="40" y2="40" stroke="gray" stroke-width="5"  /&gt;
  &lt;/svg&gt;

//Make an SVG Container
var svgContainer = d3.select("body").append("svg")
                                    .attr("width", 200)
                                    .attr("height", 200);

//Draw the line
var circle = svgContainer.append("line")
                         .attr("x1", 5)
                         .attr("y1", 5)
                         .attr("x2", 50)
                         .attr("y2", 50);
                         .attr("stroke-width", 2)
                         .attr("stroke", "black");
</pre>

####Polyline
<pre>
&lt;svg width="50" height="50"&gt;
  &lt;polyline fill="none" stroke="blue" stroke-width="2"
    points="05,30
            15,30
            15,20
            25,20
            25,10
            35,10" /&gt;
&lt;/svg&gt;
</pre>

####Polygon
<pre>
  &lt;svg width="50" height="50"&gt;
    &lt;polygon fill="yellow" stroke="blue" stroke-width="2"
      points="05,30
              15,10
              25,30" /&gt;
  &lt;/svg&gt;
</pre>

####Linear Interpolators
<pre>
linear - piecewise linear segments, as in a polyline. 
step-before - alternate between vertical and horizontal segments, as in a step function. 
step-after - alternate between horizontal and vertical segments, as in a step function. 
basis - a B-spline, with control point duplication on the ends. 
basis-open - an open B-spline; may not intersect the start or end. 
basis-closed - a closed B-spline, as in a loop. 
bundle - equivalent to basis, except the tension parameter is used to straighten the spline. 
cardinal - a Cardinal spline, with control point duplication on the ends. 
cardinal-open - an open Cardinal spline; may not intersect the start or end, but will intersect other control points. 
cardinal-closed - a closed Cardinal spline, as in a loop. 
monotone - cubic interpolation that preserves monotonicity in y. 
</pre>

###D3 Generators
<pre>
<b>d3.svg.line</b> - <em>create a new line generator</em>  
<b>d3.svg.line.radial</b> - <em>create a new radial line generator</em>  
<b>d3.svg.area</b> - <em>create a new area generator</em>  
<b>d3.svg.area.radial</b> - <em>create a new radial area generator</em>  
<b>d3.svg.arc</b> - <em>create a new arc generator</em>  
<b>d3.svg.symbol</b> - <em>create a new symbol generator</em>  
<b>d3.svg.chord</b> - <em>create a new chord generator</em>  
<b>d3.svg.diagonal</b> - <em>create a new diagonal generator</em>  
<b>d3.svg.diagonal.radial</b> - <em>create a new radial diagonal generator</em>  
</pre>
