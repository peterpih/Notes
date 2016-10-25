[Integrating Rails and Bootstrap, Part 1 - the Installation](https://launchschool.com/blog/integrating-rails-and-bootstrap-part-1)

[Bootstrap Grid Examples](http://getbootstrap.com/examples/grid/)

###Column Setup
<pre>
%body
  .container.container-fluid      <em># allow for flowing</em>
    .row
      #sidebar.col-xs-5          <em># each .col-x-x indent group must add to 12</em>
      .container.col-xs-7
        .row             <em># aligns the following columns</em>
          .dev.col-xs-6   
          .dev.col-xs-6
</pre>
