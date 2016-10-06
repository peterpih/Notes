##[Sankey Example](http://bl.ocks.org/d3noob/5028304)

###[Sankey Diagrams: A Description of the d3.js Code](http://www.d3noob.org/2013/02/sankey-diagrams-description-of-d3js-code.html)
###[Sankey diagram with horizontal and vertical node movement](http://bl.ocks.org/d3noob/5028304)

##[D3 Wiki](https://github.com/mbostock/d3/wiki)
[Short Javascript Tutorial](https://www.dashingd3js.com/lessons/introduction-to-javascript)

###[D3.org](https://d3js.org)  
###<a href="https://github.com/d3/d3/wiki/Tutorials" target="_blank">D3.org Tutorials</a>  

###<a href="https://www.dashingd3js.com/table-of-contents" target="_blank">Dashing D3 Tutorial</a>  

###[Dashing D3 Tutorials](https://www.dashingd3js.com/table-of-contents+target=")   

###[City of Oakland Cashflow Sankey](http://openbudgetoakland.org/2015-17-adopted-budget-flow.html)

From  Exaptive Talk  
[Geographic Maps](https://www.jasondavies.com)  
[SVG Beyond Mere Shapes — Nadieh Bremer](https://www.youtube.com/watch?v=AwlA3SaChHE)  
[Drawing on canvas - how computers read pixels — Mariko Kosaka](https://www.youtube.com/watch?v=-6REd8lLsPM)  
[Open Vis Conf Videos](https://openvisconf.com)



###[Combining R and D3](http://blog.ae.be/combining-the-power-of-r-and-d3-js/)

###The following 3 code blocks are equivalent (method chaining)
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

These shapes seem to come from HTML definitions.

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

###Dynamic SVG Coordinate Space
<pre>
var jsonRectangles = [
  { "x_axis": 10, "y_axis": 10, "height": 20, "width":20, "color" : "green" },
  { "x_axis": 160, "y_axis": 40, "height": 20, "width":20, "color" : "purple" },
  { "x_axis": 70, "y_axis": 70, "height": 20, "width":20, "color" : "red" }];

var max_x = 0;
var max_y = 0;

for (var i = 0; i < jsonRectangles.length; i++) {
  var temp_x, temp_y;
  var temp_x = jsonRectangles[i].x_axis + jsonRectangles[i].width;
  var temp_y = jsonRectangles[i].y_axis + jsonRectangles[i].height;

  if ( temp_x >= max_x ) { max_x = temp_x; }

  if ( temp_y >= max_y ) { max_y = temp_y; }
}

var svgContainer = d3.select("body").append("svg")
                                    .attr("width", max_x)
                                    .attr("height", max_y)

var rectangles = svgContainer.selectAll("rect")
                             .data(jsonRectangles)
                             .enter()
                             .append("rect");

var rectangleAttributes = rectangles
                          .attr("x", function (d) { return d.x_axis; })
                          .attr("y", function (d) { return d.y_axis; })
                          .attr("height", function (d) { return d.height; })
                          .attr("width", function (d) { return d.width; })
                          .style("fill", function(d) { return d.color; });
</pre>

###Scaling
<pre>
var linearScale = d3.scale.linear()
                           .domain([0,10000])  // original
                           .range([0,100]);    // transform
</pre>

####d3.max
<pre>
var maxInitialData = d3.max(initialScaleData);
</pre>

####d3.min
<pre>
var maxInitialData = d3.min(initialScaleData);
</pre>

####Scaling types
<pre>
<b>Identity</b>: a special kind of linear scale, 1:1, good for pixel values. input == output  
<b>Linear</b>: transforms one value in the domain interval into a value in the range interval  
<b>Power and Logarithmic scales</b>: sqrt, pow, log – used for exponentially increasing values  
<b>Quantize and Quantile scales</b>: for discrete sets of unique possible values for inputs or outputs  
<b>Ordinal</b>: for non quantitative scales, like names, categories, etc.  
</pre>

###SVG Group Elements
<pre>
  &lt;g&gt;
  ...
  &lt;/g&gt;
</pre>
