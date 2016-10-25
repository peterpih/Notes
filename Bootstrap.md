[Integrating Rails and Bootstrap, Part 1 - the Installation](https://launchschool.com/blog/integrating-rails-and-bootstrap-part-1)

[Bootstrap Grid Examples](http://getbootstrap.com/examples/grid/)

###Column Setup
<pre>
<b>%body</b>
<b>.container.container-fluid</b>      <em># allow for flowing</em>
    <b>.row</b>
    <em>#sidebar</em><b>.col-xs-5</b>          <em># each .col-x-x indent group must add to 12</em>
      <b>.container.col-xs-7</b>
        <b>.row</b>             <em># aligns the following columns</em>
        <b>.dev.col-xs-6</b>   
        <b>.dev.col-xs-6</b>
</pre>
