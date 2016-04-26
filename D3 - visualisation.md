
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
d3.select("body")
  .append("svg")
  .attr("width", 50)
  .attr("height", 50)
  .append("circle")
  .attr("cx", 25)
  .attr("cy", 25)
  .attr("r", 25)
  .style("fill", "purple");
 </pre>
 
Best:
<pre>
var bodySelection = d3.select("body");

var svgSelection = bodySelection.append("svg")
      .attr("width", 50)
      .attr("height", 50);

var circleSelection = svgSelection.append("circle")
      .attr("cx", 25)
      .attr("cy", 25)
      .attr("r", 25)
      .style("fill", "purple");
</pre>
